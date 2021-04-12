---
description: A comunicação com um dispositivo de rede usando a interface WMI SNMP requer a configuração dos serviços de dispositivo, SNMP e WMI. As informações neste tópico explicam como configurar o ambiente SNMP WMI.
ms.assetid: 8074175a-af66-49b2-9723-dfb38a08fb63
ms.tgt_platform: multiple
title: Configurando o ambiente SNMP WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eeed470b1e38bf853bd6b023fa0f07b01c5df47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297494"
---
# <a name="setting-up-the-wmi-snmp-environment"></a>Configurando o ambiente SNMP WMI

A comunicação com um dispositivo de rede usando a interface WMI SNMP requer a configuração dos serviços de dispositivo, SNMP e WMI. As informações neste tópico explicam como configurar o ambiente SNMP WMI.

As seções a seguir são discutidas neste tópico:

## <a name="installing-the-snmp-provider"></a>Instalando o provedor SNMP

O serviço SNMP não está habilitado por padrão. Você pode habilitar o serviço SNMP e o provedor WMI SNMP por meio do painel de controle. Lembre-se de que o serviço SNMP deve estar habilitado e em execução para que o provedor WMI SNMP funcione.

A partir do Windows Vista, use o procedimento a seguir para instalar o provedor SNMP.

**Para instalar o provedor SNMP**

1.  No **painel de controle**, selecione **programas**.
2.  Em **programas e recursos**, selecione **Ativar ou desativar recursos do Windows**.
3.  Na lista recursos do Windows, role para baixo até o **recurso SNMP** e expanda a lista para que você possa ver o **provedor SNMP WMI**.
4.  Marque a caixa de seleção para o **provedor WMI SNMP**. A caixa de seleção do **recurso SNMP** é selecionada automaticamente porque o provedor requer SNMP.
5.  Clique em **OK**.
6.  Em um prompt de comando ou no menu **Iniciar** , execute Services. msc e verifique se o serviço SNMP foi iniciado.

## <a name="creating-an-snmp-namespace"></a>Criando um namespace SNMP

Um namespace SNMP define uma exibição de um dispositivo de rede.

> [!Note]  
> Para obter mais informações sobre o suporte e a instalação desse componente em um sistema operacional específico, consulte [disponibilidade do sistema operacional de componentes WMI](operating-system-availability-of-wmi-components.md).

 

O procedimento a seguir descreve como criar um [*namespace*](gloss-n.md)SNMP WMI.

**Para criar um namespace SNMP**

1.  Crie uma instância da classe de sistema de [**\_ \_ namespace**](--namespace.md) Compilando um arquivo [*formato MOF*](gloss-m.md) . mof ou usando a [API com para o WMI](com-api-for-wmi.md).

    Para obter mais informações, consulte [Criando hierarquias no WMI](creating-hierarchies-within-wmi.md).

2.  Associe os [*qualificadores*](gloss-q.md) do provedor SNMP à definição do namespace.

    Os qualificadores do provedor SNMP contêm informações de contexto específicas de implementação e propriedades de transporte que definem como o provedor SNMP acessa um dispositivo SNMP. Para obter mais informações, consulte [**qualificadores específicos para o provedor SNMP**](qualifiers-specific-to-the-snmp-provider.md).

3.  Use a ferramenta de linha de comando [Mofcomp](mofcomp.md) para carregar o código MOF no repositório WMI.

    Para obter mais informações, consulte [compilando arquivos MOF](compiling-mof-files.md).

O exemplo de código MOF a seguir define o \\ namespace SNMP com um subconjunto dos qualificadores que podem ser associados a um namespace SNMP.

``` syntax
// Load classes and instances into <\\.\root> namespace

#pragma namespace("\\\\.\\root")               

[ 
  AgentAddress( "localhost" ), 
  AgentReadCommunityName( "public"), 
  AgentWriteCommunityName( "private"), 
  AgentRetryCount( 1 ), 
  AgentRetryTimeout( 500 ), 
  AgentVarBindsPerPdu( 10 ),
  AgentFlowControlWindowSize ( 3 ) 
]

  instance of __Namespace
  {
      Name = "snmp" ;
  };
```

## <a name="inserting-snmp-mib-data-into-wmi"></a>Inserindo dados de MIB SNMP no WMI

Como um provedor, o provedor SNMP atua como uma ponte entre os dados SNMP e as classes WMI. Portanto, você deve ter classes no WMI que representem diferentes aspectos de um dispositivo habilitado para SNMP. Para fazer isso, você deve usar o compilador do módulo de informações do SNMP ([smi2smir](smi2smir.md)) para compilar informações de gerenciamento SNMP do formato SNMP nas definições de esquema de CIM equivalentes. Você pode direcionar a saída do compilador de informações para um banco de dados de esquema SNMP chamado de "SMIR (repositório de informações do módulo SNMP)" ou vários tipos diferentes de arquivos MOF.

O compilador é executado no modo de linha de comando, usando um arquivo MIB como entrada. O comando a seguir carrega o arquivo MIB especificado no SMIR.

**smi2smir/a***<MIB file>*

## <a name="setting-up-snmp-communities"></a>Configurando comunidades SNMP

Como medida de segurança, a Comunidade "pública" SNMP não é criada por padrão. Você pode criar a Comunidade conforme descrito em [configurações do registro de comunidades](/previous-versions/windows/embedded/ms907028(v=msdn.10)). Se você não tiver nenhuma comunidade, crie a Comunidade "pública" para acessar o provedor SNMP.

## <a name="generating-mof-files-from-mib-files"></a>Gerando arquivos MOF a partir de arquivos MIB

Os comandos a seguir são um exemplo de como gerar arquivos MOF a partir dos arquivos MIB instalados quando o provedor SNMP é instalado.

**CD** *% windir% \\ System32 \\ WBEM \\ SNMP*

**Smi2smir/g** *.. \\ .. \\ hostmib. MIB* **>** *hostmib. mof*

**Smi2smir/g** *.. \\ .. \\ ipforwd. MIB* **>** *ipforwd. mof*

**Smi2smir/g** *.. \\ .. \\ nipx. MIB* **>** *nipx. mof*

**Smi2smir/g** *.. \\ .. \\ MIB \_ II.* MIB MIB **>** *\_ II. mof*

**Smi2smir/g** *.. \\ .. \\ lmmib2. MIB* **>** *lmmib2. mof*

**Smi2smir/g** *.. \\ .. \\ mcastmib. MIB* **>** *mcastmib. mof*

**Smi2smir/g** *.. \\ .. \\ rfc2571. MIB* **>** *rfc2571. mof*

**Smi2smir/g** *.. \\ .. \\ wfospf. MIB* **>** *wfospf. mof*

**Smi2smir/g** *.. \\ .. \\ DHCP. MIB \\ . \\ .. MSFT. MIB* **>** *DHCP. mof*

**Smi2smir/g** *.. \\ .. \\ WINS \\ . MIB.. \\ . MSFT. MIB* **>** *vence. mof*

**Smi2smir/g** *.. \\ .. \\ mipx. MIB. \\ \\ .. MSFT. MIB* **>** *mipx. mof*

**Smi2smir/g** *.. \\ .. \\ mripsap. MIB. \\ \\ .. MSFT. MIB* **>** *mripsap. mof*

**Smi2smir/g** *.. \\ .. \\ msipbtp. MIB. \\ \\ .. MSFT. MIB* **>** *msipbtp. mof*

**Smi2smir/g** *.. \\ .. \\ msiprip2. MIB. \\ \\ .. MSFT. MIB* **>** *msiprip2. mof*

## <a name="adding-snmp-mof-files-to-the-wmi-repository"></a>Adicionando arquivos MOF SNMP ao repositório WMI

Os comandos a seguir são um exemplo de como adicionar os arquivos MOF que são gerados a partir dos arquivos MIB para o repositório WMI. Se você quiser adicionar os arquivos MOF à lista de arquivos a serem restaurados automaticamente em uma recuperação de [*repositório WMI*](gloss-w.md) , adicione o sinalizador **-AutoRecuperação** ao final de cada comando. Para obter mais informações sobre a ferramenta de linha de comando WMI Mofcomp.exe, consulte [**Mofcomp**](mofcomp.md).

**Mofcomp** *hostmib. mof*

**Mofcomp** *ipforwd. mof*

**Mofcomp** *nipx. mof*

**Mofcomp** *MIB \_ II. mof*

**Mofcomp** *lmmib2. mof*

**Mofcomp** *mcastmib. mof*

**Mofcomp** *rfc2571. mof*

**Mofcomp** *wfospf. mof*

**Mofcomp** *DHCP. mof*

**Mofcomp** *mipx. mof*

**Mofcomp** *mripsap. mof*

**Mofcomp** *msipbtp. mof*

**Mofcomp** *msiprip2. mof*

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Acessando dispositivos SNMP](accessing-snmp-devices.md)
</dt> </dl>

 

 
