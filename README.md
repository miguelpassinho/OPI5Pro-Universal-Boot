🟠 Orange Pi 5 Pro – Universal Bootloader

📖 About this project

I am not a professional programmer.
I am a father, a curious mind, a student of life.
This project was born during a difficult period of my life, when I had to reinvent myself and embrace learning as a way to move forward. Every command line, every sleepless night, was an effort beyond what I thought I could achieve.
The result is simple but powerful: a universal bootloader for the Orange Pi 5 Pro.
Flash it once to the eMMC, and from then on, just pick the distro you want, write it to the NVMe, and boot. No headaches, no manual tweaks.

⚙️ How to use

1. Prepare the eMMC with the bootloader
Flash the raw image to the eMMC (⚠️ this erases the first MBs of the eMMC):
    sudo dd if=opi5pro-bootloader.img of=/dev/mmcblk0 bs=1M conv=fsync status=progress sync

2. Choose your system
Download the ARM64 distro image you want (Debian Trixie, Armbian, Arch/BredOS, Ubuntu, Fedora ARM, etc).
3. Flash to NVMe
Write the chosen image to the NVMe with dd or BalenaEtcher.
4. Boot
Insert the NVMe into the Orange Pi 5 Pro and power it on.
The bootloader on the eMMC detects the NVMe and boots the system automatically.

🔑 Why use this bootloader image?
The idea of flashing the bootloader directly to the eMMC is to avoid errors.
You don’t need to recompile anything or manually adjust partitions.
Flash this image once, and from then on, any system on the NVMe works automatically.

🔍 eMMC layout after flashing
- mmcblk0p1 (480 KiB) → SPL (DDR init + BL31)
- mmcblk0p2 (3 MiB) → U‑Boot + DTB
- mmcblk0boot0/1 (4 MiB each) → reserved by SoC

  Transparency Note
I did not write the bootloader or UEFI code — they are available on the official project pages.
What I did was figure out and validate the correct way to flash and organize the bootloader on the eMMC, so that any system on the NVMe works out‑of‑the‑box, with no manual tweaks.
I’m a simple man, and my integrity is all I carry with me. This work is the result of effort, learning, and the will to share.
🔗 Official UEFI repo for RK3588: edk2-porting/edk2-rk3588

🤝 Invitation to the Community
This project is not about reinventing code — the bootloader and UEFI come from official sources.
The key here was to find and validate the correct way to flash the bootloader to the eMMC, so that any system on the NVMe works directly, without manual tweaks.
Now, here’s an open invitation:
- If you are a professional developer, or have experience with U‑Boot, UEFI or ARM kernels, feel free to improve, review, and expand this work.
- Contributions of any kind are welcome — code, documentation, testing, or optimizations.
Everything you need is already here. The next step belongs to the community.

🙏 Support
If this work helped you, that’s already enough.
If you’d like to support me so I can keep learning, testing, and sharing, here’s my Ko‑fi:
👉 ko-fi.com/miguelpassinho



🟠 Orange Pi 5 Pro – Bootloader Universal

📖 Sobre este projeto

Eu não sou programador profissional.
Sou pai, curioso, aluno da vida.
Esse projeto nasceu no meio de um período difícil da minha vida, em que precisei me reinventar e agarrar o aprendizado como forma de seguir em frente. Cada linha de comando, cada noite sem dormir, foi um esforço acima do que eu achava que conseguiria.
O resultado é simples, mas poderoso: um bootloader universal para o Orange Pi 5 Pro.
Grave uma vez no eMMC e, a partir daí, basta escolher a distro que você quiser, gravar no NVMe e ligar a placa. Sem dor de cabeça, sem ajustes manuais.

⚙️ Como usar
1. Preparar o eMMC com o bootloader
Grave a imagem crua no eMMC (⚠️ isso apaga os primeiros MB do eMMC):

    sudo dd if=opi5pro-bootloader.img of=/dev/mmcblk0 bs=1M conv=fsync status=progress sync


2. Escolher o sistema
Baixe a imagem da distro ARM64 que você quiser (Debian Trixie, Armbian, Arch/BredOS, Ubuntu, Fedora ARM, etc).
3. Gravar no NVMe
Grave a imagem escolhida no NVMe com dd ou BalenaEtcher.
4. Boot
Conecte o NVMe no Orange Pi 5 Pro e ligue.
O bootloader no eMMC detecta o NVMe e inicia o sistema automaticamente.

🔑 Por que usar esta imagem de bootloader?
A ideia de gravar o bootloader direto no eMMC é justamente evitar erros.
Você não precisa recompilar nada nem ajustar partições manualmente.
Basta gravar esta imagem uma vez e, a partir daí, qualquer sistema no NVMe funciona automaticamente.

🔍 Estrutura do eMMC após gravação
- mmcblk0p1 (480 KiB) → SPL (DDR init + BL31)
- mmcblk0p2 (3 MiB) → U‑Boot + DTB
- mmcblk0boot0/1 (4 MiB cada) → áreas reservadas pelo SoC

    Nota de Transparência
Eu não escrevi os códigos do bootloader ou do UEFI — eles estão disponíveis nas páginas oficiais dos projetos.
O que eu fiz foi descobrir e validar a forma correta de gravar e organizar o bootloader no eMMC, de modo que qualquer sistema no NVMe funcione direto, sem ajustes manuais.
Sou um cara simples, e só tenho minha moral para levar comigo. Esse trabalho é fruto de esforço, aprendizado e vontade de compartilhar.
🔗 Repositório oficial do UEFI para RK3588: edk2-porting/edk2-rk3588

🤝 Convite à Comunidade
Este projeto não é sobre reinventar código — o bootloader e o UEFI vêm das fontes oficiais.
O diferencial aqui foi encontrar e validar a forma correta de gravar o bootloader no eMMC, para que qualquer sistema no NVMe funcione direto, sem ajustes manuais.
Agora, deixo um convite aberto:
- Se você é programador profissional, ou tem experiência com U‑Boot, UEFI ou kernels ARM, sinta-se à vontade para aprimorar, revisar e expandir este trabalho.
- Toda contribuição é bem-vinda — seja código, documentação, testes ou otimizações.
Tudo o que precisa já está aqui. O próximo passo é da comunidade.

🙏 Apoio
Se este trabalho te ajudou, já valeu.
Se você quiser apoiar para que eu continue aprendendo, testando e compartilhando, deixo aqui meu Ko‑fi:
👉 ko-fi.com/miguelpassinho


