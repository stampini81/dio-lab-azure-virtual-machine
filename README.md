

# Laboratório DIO: Criando uma Máquina Virtual no Azure

Este repositório documenta o laboratório prático "Criando uma Máquina Virtual no Azure" da DIO, focado em computação em nuvem e criação de uma VM Windows no portal Azure.

## Pré-requisitos

- Conta ativa no [Microsoft Azure](https://portal.azure.com/)
- Navegador web
- Ferramenta para capturas de tela (Windows: `Win + Shift + S`)

## Passo a Passo

### 1. Acesso ao Portal do Azure
Acesse o [portal do Azure](https://portal.azure.com/) e clique em **Criar um recurso**.

![Acesso ao portal](https://learn.microsoft.com/pt-br/azure/virtual-machines/windows/media/quick-create-portal/instance-details.png)

### 2. Configuração da Máquina Virtual
Preencha os campos conforme o tutorial. Recomenda-se:
- Grupo de Recursos: `dio-lab-vm-rg`
- Nome: `dio-vm-windows`
- Região: `East US`
- Imagem: `Windows Server 2022`
- Tamanho: `Standard_B1s`
- Libere a porta RDP (3389)

![Configuração da VM](https://learn.microsoft.com/pt-br/azure/virtual-machines/windows/media/quick-create-portal/administrator-account.png)
![Regras de porta de entrada](https://learn.microsoft.com/pt-br/azure/virtual-machines/windows/media/quick-create-portal/inbound-port-rules.png)

### 3. Disco e Rede
Mantenha as configurações padrão de disco e rede.

### 4. Revisão e Criação
Revise as configurações e clique em **Criar**.

![Revisão e criação](https://learn.microsoft.com/pt-br/azure/virtual-machines/windows/media/quick-create-portal/review-create.png)
![Validação aprovada](https://learn.microsoft.com/pt-br/azure/virtual-machines/windows/media/quick-create-portal/validation.png)
![Ir para o recurso](https://learn.microsoft.com/pt-br/azure/virtual-machines/windows/media/quick-create-portal/next-steps.png)

### 5. Conexão via RDP
Após a implantação, conecte-se à VM usando o arquivo RDP gerado.

![Conectar via RDP](https://learn.microsoft.com/pt-br/azure/virtual-machines/windows/media/quick-create-portal/portal-quick-start-9.png)

### 6. Instalar servidor Web (opcional)
Na VM, abra o PowerShell e execute:
```powershell
Install-WindowsFeature -name Web-Server -IncludeManagementTools
```
Depois, acesse o IP público da VM no navegador para ver a página padrão do IIS:

![Site padrão do IIS](https://learn.microsoft.com/pt-br/azure/virtual-machines/windows/media/quick-create-powershell/default-iis-website.png)

## Como adicionar capturas de tela próprias

1. Crie uma pasta chamada `images` no repositório.
2. Salve suas capturas de tela nela.
3. Referencie as imagens no README usando:
    `![Descrição](images/nome-da-imagem.png)`

## Links úteis

- [Documentação oficial Azure VMs](https://learn.microsoft.com/pt-br/azure/virtual-machines/)
- [Guia DIO](https://web.dio.me/)

## Conclusão

Este laboratório reforça conceitos de nuvem e mostra como criar e acessar uma VM no Azure. Documente seu processo com capturas de tela para facilitar o aprendizado e compartilhamento.

---
*Imagens oficiais retiradas da [documentação Microsoft Learn](https://learn.microsoft.com/pt-br/azure/virtual-machines/windows/quick-create-portal).*
