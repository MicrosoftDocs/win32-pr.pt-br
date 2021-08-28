---
title: Windows Remote Management
description: Windows o gerenciamento remoto (Gerenciamento Remoto do Windows) é a implementação da Microsoft do protocolo WS-Management, um protocolo padrão baseado em SOAP, compatível com firewall, que permite que os sistemas operacionais e de hardware, de fornecedores diferentes, interoperem.
ms.assetid: 6429e748-e0bf-431a-8989-db5b211665d5
ms.tgt_platform: multiple
keywords:
- Windows Gerenciamento remoto (WinRM), página inicial
- WS-Management
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbOrient
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c816e3f7092fc7825407497793ed529df13cf9115426b63e4b535bd019f81df0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858756"
---
# <a name="windows-remote-management"></a>Windows Remote Management

## <a name="purpose"></a>Finalidade

O WinRM (Gerenciamento Remoto do Windows) é a implementação da Microsoft do [Protocolo WS-Management](ws-management-protocol.md), um protocolo padrão amigável para firewall, baseado no protocolo SOAP, que permite que hardware e sistemas operacionais de fornecedores diferentes interajam.

A especificação do protocolo WS-Management fornece uma maneira comum de os sistemas acessarem e trocarem informações de gerenciamento em uma infra-estrutura de ti. o WinRM e a [*IPMI (Interface de gerenciamento de plataforma inteligente)*](windows-remote-management-glossary.md), juntamente com o [coletor de eventos](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) , são componentes do Windows recursos de [gerenciamento de Hardware](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) .

## <a name="where-applicable"></a>Quando aplicável

você pode usar objetos de script do winrm, a ferramenta de linha de comando winrm ou a Windows ferramenta de linha de comando do Shell remoto WinRS para obter dados de gerenciamento de computadores locais e remotos que podem ter [*BMCs (baseboard management controller)*](windows-remote-management-glossary.md). se o computador executar uma versão do sistema operacional baseada em Windows que inclui o WinRM, os dados de gerenciamento serão fornecidos pelo [Instrumentação de Gerenciamento do Windows (WMI)](/windows/desktop/WmiSdk/wmi-start-page).

Você também pode obter dados de hardware e do sistema a partir de implementações do protocolo WS-Management que são executadas em sistemas operacionais diferentes do Windows em sua empresa. O WinRM estabelece uma sessão com um computador remoto por meio do protocolo WS-Management baseado em SOAP, em vez de uma conexão por meio do DCOM, como a WMI faz. Os dados retornados ao protocolo WS-Management são formatados em XML, não em objetos.

O provedor WMI da [IPMI (interface de gerenciamento de plataforma inteligente)](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) é um provedor WMI padrão com classes que obtêm dados do sensor do BMC de computadores com hardware apropriado. Os dados do IPMI podem ser acessados usando a API de script do WinRM, o [script](/windows/desktop/WmiSdk/scripting-api-for-wmi)do WMI ou APIs [com](/windows/desktop/WmiSdk/com-api-for-wmi) .

## <a name="developer-audience"></a>Público de desenvolvedores

o público-alvo do desenvolvedor é o Pro de ti que escreve scripts para automatizar o gerenciamento de servidores ou o desenvolvedor ISV obtendo dados para aplicativos de gerenciamento.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

O WinRM faz parte do sistema operacional. No entanto, para obter dados de computadores remotos, você deve configurar um [*ouvinte*](windows-remote-management-glossary.md#l)do WinRM. para obter mais informações, consulte [instalação e configuração para Gerenciamento Remoto do Windows](installation-and-configuration-for-windows-remote-management.md). Se um BMC for detectado na inicialização do sistema, o provedor de IPMI será carregado; caso contrário, os objetos de script do WinRM e a ferramenta de linha de comando WinRM ainda estarão disponíveis.

## <a name="in-this-section"></a>Nesta seção

<dl> <dt>

[sobre Gerenciamento Remoto do Windows](about-windows-remote-management.md)
</dt> <dd>

Link para especificação de protocolo de WS-Management público, arquitetura do WinRM, relação com o WMI, gerenciamento de hardware com o provedor IPMI, configuração e instalação.

</dd> <dt>

[usando Gerenciamento Remoto do Windows](using-windows-remote-management.md)
</dt> <dd>

Introdução ao uso da API de script do WinRM e do gerenciamento de hardware.

</dd> <dt>

[Windows Referência de gerenciamento remoto](windows-remote-management-reference.md)
</dt> <dd>

Lista de interfaces de script definidas pela automação do Microsoft Web Services for Management (WS-Management) e definições de classe das classes WMI criadas pelo provedor IPMI e pelas classes que se comunicam com o driver IPMI para obter os dados do [controlador de gerenciamento de placa-base (BMC)](windows-remote-management-glossary.md) .

</dd> </dl>

 

 