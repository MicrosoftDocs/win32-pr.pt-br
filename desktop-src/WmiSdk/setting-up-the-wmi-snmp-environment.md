---
description: A comunicação com um dispositivo de rede usando a interface WMI SNMP requer a configuração dos serviços de dispositivo, SNMP e WMI. As informações neste tópico explicam como configurar o ambiente WMI SNMP.
ms.assetid: 8074175a-af66-49b2-9723-dfb38a08fb63
ms.tgt_platform: multiple
title: Configurando o ambiente WMI SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a090dab219c589fc8d9084c445e9a69c8d75afefb64400fe3029bfed66ab931
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860406"
---
# <a name="setting-up-the-wmi-snmp-environment"></a>Configurando o ambiente WMI SNMP

A comunicação com um dispositivo de rede usando a interface WMI SNMP requer a configuração dos serviços de dispositivo, SNMP e WMI. As informações neste tópico explicam como configurar o ambiente WMI SNMP.

As seções a seguir são discutidas neste tópico:

## <a name="installing-the-snmp-provider"></a>Instalando o provedor SNMP

O serviço SNMP não está habilitado por padrão. Você pode habilitar o serviço SNMP e o Provedor WMI SNMP por meio do Painel de Controle. Esteja ciente de que o serviço SNMP deve estar habilitado e em execução para que o provedor WMI SNMP funcione.

Começando com Windows Vista, use o procedimento a seguir para instalar o provedor SNMP.

**Para instalar o provedor SNMP**

1.  No **Painel de Controle**, selecione **Programas**.
2.  Em **Programas e Recursos,** selecione **Ativar Windows recursos ou desativar**.
3.  Na lista Windows recursos, role para baixo até o recurso **SNMP** e expanda a lista para que você possa ver Provedor **SNMP WMI**.
4.  Marque a caixa de seleção para **Provedor WMI SNMP.** A caixa de seleção do **recurso SNMP** é selecionada automaticamente porque o provedor requer SNMP.
5.  Clique em **OK**.
6.  Em um prompt de comando ou no menu **Iniciar,** execute Services.msc e verifique se o serviço SNMP foi iniciado.

## <a name="creating-an-snmp-namespace"></a>Criando um namespace SNMP

Um namespace SNMP define uma exibição de um dispositivo de rede.

> [!Note]  
> Para obter mais informações sobre o suporte e a instalação desse componente em um sistema operacional específico, consulte Disponibilidade do sistema operacional [de componentes WMI](operating-system-availability-of-wmi-components.md).

 

O procedimento a seguir descreve como criar um [*namespace*](gloss-n.md)WMI SNMP .

**Para criar um namespace SNMP**

1.  Crie uma instância da classe de sistema [**\_ \_ Namespace**](--namespace.md) compilando um [*arquivo*](gloss-m.md) Managed Object Format .mof ou usando a [API COM para WMI](com-api-for-wmi.md).

    Para obter mais informações, consulte [Criando hierarquias no WMI](creating-hierarchies-within-wmi.md).

2.  Associe [*qualificadores*](gloss-q.md) de provedor SNMP à definição de namespace.

    Os qualificadores do provedor SNMP contêm informações de contexto específicas da implementação e propriedades de transporte que definem como o provedor SNMP acessa um dispositivo SNMP. Para obter mais informações, consulte [**Qualificadores específicos para o provedor SNMP**](qualifiers-specific-to-the-snmp-provider.md).

3.  Use a ferramenta de linha de [comando mofcomp](mofcomp.md) para carregar o código MOF no repositório WMI.

    Para obter mais informações, consulte [Compilando arquivos MOF](compiling-mof-files.md).

O exemplo de código MOF a seguir define o namespace snmp com um subconjunto dos qualificadores que podem ser associados a um \\ namespace SNMP.

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

## <a name="inserting-snmp-mib-data-into-wmi"></a>Inserindo dados MIB SNMP no WMI

Como provedor, o provedor SNMP atua como uma ponte entre os dados SNMP e as classes WMI. Portanto, você deve ter classes no WMI que representam diferentes aspectos de um dispositivo habilitado para SNMP. Para fazer isso, você deve usar o compilador do módulo de informações SNMP ([smi2smir](smi2smir.md)) para compilar informações de gerenciamento SNMP do formato SNMP nas definições de esquema CIM equivalentes. Em seguida, você pode direcionar a saída do compilador de informações para um banco de dados de esquema SNMP chamado "SMIR (Repositório de Informações do Módulo SNMP)" ou para vários tipos diferentes de arquivos MOF.

O compilador é executado no modo de linha de comando, usando um arquivo MIB como entrada. O comando a seguir carrega o arquivo MIB especificado no SMIR.

**smi2smir /a***<MIB file>*

## <a name="setting-up-snmp-communities"></a>Configurando comunidades SNMP

Como medida de segurança, a comunidade "pública" do SNMP não é criada por padrão. Você pode criar a comunidade conforme descrito em [Registro de comunidades Configurações](/previous-versions/windows/embedded/ms907028(v=msdn.10)). Se você não tiver nenhuma comunidade, crie a comunidade "pública" para acessar o provedor SNMP.

## <a name="generating-mof-files-from-mib-files"></a>Gerando arquivos MOF de arquivos MIB

Os comandos a seguir são um exemplo de como gerar arquivos MOF dos arquivos MIB instalados quando o provedor SNMP é instalado.

**cd** *%windir% \\ system32 \\ wbem \\ SNMP*

**Smi2smir /g** *.. \\ .. \\ hostmib.mib* **>** *hostmib.mof*

**Smi2smir /g** *.. \\ .. \\ ipforwd.mib* **>** *ipforwd.mof*

**Smi2smir /g** *.. \\ .. \\ nipx.mib* **>** *nipx.mof*

**Smi2smir /g** *.. \\ .. \\ mib \_ ii.mib* **>** *mib \_ ii.mof*

**Smi2smir /g** *.. \\ .. \\ lmmib2.mib* **>** *lmmib2.mof*

**Smi2smir /g** *.. \\ .. \\ mcastmib.mib* **>** *mcastmib.mof*

**Smi2smir /g** *.. \\ .. \\ rfc2571.mib* **>** *rfc2571.mof*

**Smi2smir /g** *.. \\ .. \\ wfospf.mib* **>** *wfospf.mof*

**Smi2smir /g** *.. \\ .. \\ dhcp.mib.. \\ .. \\ msft.mib* **>** *dhcp.mof*

**Smi2smir /g** *.. \\ .. \\ wins.mib.. \\ .. \\ msft.mib* **>** *wins.mof*

**Smi2smir /g** *.. \\ .. \\ mipx.mib.. \\ .. \\ msft.mib* **>** *mipx.mof*

**Smi2smir /g** *.. \\ .. \\ mripsap.mib.. \\ .. \\ msft.mib* **>** *mripsap.mof*

**Smi2smir /g** *.. \\ .. \\ msipbtp.mib.. \\ .. \\ msft.mib* **>** *msipbtp.mof*

**Smi2smir /g** *.. \\ .. \\ msiprip2.mib.. \\ .. \\ msft.mib* **>** *msiprip2.mof*

## <a name="adding-snmp-mof-files-to-the-wmi-repository"></a>Adicionando arquivos MOF SNMP ao repositório WMI

Os comandos a seguir são um exemplo de como adicionar os arquivos MOF gerados dos arquivos MIB ao repositório WMI. Se você quiser adicionar os arquivos MOF à lista de arquivos a serem restaurados automaticamente em uma recuperação de repositório [*WMI,*](gloss-w.md) adicione o sinalizador **-AUTORECOVER** ao final de cada comando. Para obter mais informações sobre o WMI Mofcomp.exe de linha de comando, consulte [**mofcomp**](mofcomp.md).

**mofcomp** *hostmib.mof*

**mofcomp** *ipforwd.mof*

**mofcomp** *nipx.mof*

**mofcomp** *mib \_ ii.mof*

**mofcomp** *lmmib2.mof*

**mofcomp** *mcastmib.mof*

**mofcomp** *rfc2571.mof*

**mofcomp** *wfospf.mof*

**mofcomp** *dhcp.mof*

**mofcomp** *mipx.mof*

**mofcomp** *mripsap.mof*

**mofcomp** *msipbtp.mof*

**mofcomp** *msiprip2.mof*

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Acessando dispositivos SNMP](accessing-snmp-devices.md)
</dt> </dl>

 

 
