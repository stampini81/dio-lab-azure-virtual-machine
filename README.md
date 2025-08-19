# Laboratório DIO: Criando uma Máquina Virtual no Azure

Este repositório documenta a experiência prática do laboratório "Criando uma Máquina Virtual no Azure", parte da formação da DIO. O objetivo deste desafio é aplicar os conceitos de computação em nuvem, especificamente na criação de uma Máquina Virtual (VM) com Windows no portal do Microsoft Azure.

## Resumo dos Conceitos Aprendidos

Durante as aulas, foram abordados os conceitos fundamentais que servem de base para a computação em nuvem e para a utilização de serviços como o Azure. Os principais tópicos foram:

* [cite_start]**Computação em Nuvem:** É a entrega de serviços de computação (como servidores, armazenamento e redes) pela internet[cite: 311]. [cite_start]Este modelo permite inovar mais rápido, ter recursos flexíveis e se beneficiar da economia de escala[cite: 311].
* **Modelos de Nuvem:**
    * [cite_start]**Pública:** A infraestrutura pertence a um provedor (como a Microsoft) e é compartilhada por vários clientes[cite: 328, 329].
    * [cite_start]**Privada:** A infraestrutura é de uso exclusivo de uma única organização[cite: 323].
    * [cite_start]**Híbrida:** Combina as nuvens pública e privada para obter o melhor dos dois mundos, mantendo o controle sobre dados sensíveis enquanto aproveita a escalabilidade da nuvem pública[cite: 336, 355].
* **Benefícios da Nuvem:**
    * [cite_start]**Alta Disponibilidade:** Garante o máximo de tempo de atividade dos serviços, independentemente de falhas[cite: 125].
    * [cite_start]**Escalabilidade:** Capacidade de adicionar recursos para lidar com o aumento da demanda[cite: 137, 138].
    * [cite_start]**Elasticidade:** Habilidade de aumentar ou diminuir recursos de forma automática para atender a picos de demanda[cite: 155, 160].
    * [cite_start]**Modelo de Consumo (OpEx):** Paga-se apenas pelos recursos que são utilizados, transformando despesas de capital (CapEx) em despesas operacionais[cite: 364, 366].

## Passo a Passo da Criação da VM no Azure

A seguir, estão os passos realizados para a criação de uma Máquina Virtual do Windows no portal do Azure, conforme o guia "Início Rápido: Criar uma máquina virtual do Windows no Portal do Azure".

*(**Dica:** Substitua as imagens de exemplo pelas suas próprias capturas de tela. Crie uma pasta `/images` no seu repositório para organizá-las.)*

**1. Acesso ao Portal do Azure e Criação do Recurso**
* Acessei o portal do Azure (`portal.azure.com`).
* No menu, selecionei **"Criar um recurso"**.
* Busquei por **"Máquina Virtual"** e iniciei o processo de criação.

**2. Configurações Básicas**
* **Assinatura e Grupo de Recursos:** Selecionei minha assinatura e criei um novo Grupo de Recursos chamado `dio-lab-vm-rg` para organizar os recursos deste laboratório.
* **Detalhes da Instância:**
    * **Nome da máquina virtual:** `dio-vm-windows`
    * **Região:** `(US) East US` (Leste dos EUA)
    * **Imagem:** `Windows Server 2022 Datacenter: Azure Edition - x64 Gen2`
    * **Tamanho:** `Standard_B1s` (1 vCPU, 1 GiB de memória)
* **Conta de Administrador:** Defini um nome de usuário e uma senha segura para acessar a VM.
* **Regras de Porta de Entrada:** Liberei a porta **RDP (3389)** para permitir a conexão remota.

![Exemplo de captura de tela das configurações básicas](images/configuracao-basica.png)

**3. Configurações de Disco e Rede**
* **Discos:** Mantive o padrão com um Disco do SO do tipo SSD Standard.
* **Rede:** As configurações de rede virtual, sub-rede e IP público foram criadas automaticamente pelo Azure.

**4. Revisão e Criação**
* Revisei todas as configurações na aba "Examinar + criar".
* Após a validação ser aprovada, cliquei em **"Criar"**.
* Aguardei o processo de implantação ser concluído.

**5. Conexão com a Máquina Virtual**
* Com a implantação concluída, naveguei até o recurso da máquina virtual.
* Cliquei em **"Conectar"** e escolhi a opção **RDP**.
* Baixei o arquivo RDP e o executei para iniciar a Conexão de Área de Trabalho Remota.
* Utilizei o usuário e a senha definidos no passo 2 para me conectar à VM com sucesso.

![Exemplo de captura de tela da conexão RDP](images/conexao-vm.png)

## Conclusão

Este desafio foi uma excelente oportunidade para colocar em prática os conceitos teóricos de computação em nuvem. A criação de uma Máquina Virtual no Azure é um processo estruturado e intuitivo, e o portal oferece uma visão clara de todos os recursos envolvidos (computação, rede, armazenamento). Documentar o processo no GitHub reforça a importância de manter um registro claro e compartilhável do trabalho técnico.
