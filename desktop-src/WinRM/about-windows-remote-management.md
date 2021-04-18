---
title: Sobre Gerenciamento Remoto do Windows
description: Gerenciamento Remoto do Windows é um componente dos recursos de gerenciamento de hardware do Windows que gerenciam o hardware de servidor local e remotamente.
ms.assetid: f58add53-0746-4423-9ab8-02ba05f82fa7
ms.tgt_platform: multiple
keywords:
- Sobre Gerenciamento Remoto do Windows
- Gerenciamento Remoto do Windows, sobre
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9221676d3a9864e4fc88fc57c5bb6691512c220a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105815454"
---
# <a name="about-windows-remote-management"></a>Sobre Gerenciamento Remoto do Windows

Gerenciamento Remoto do Windows é um componente dos recursos de [Gerenciamento de hardware do Windows](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) que gerenciam o hardware de servidor local e remotamente. Esses recursos incluem um serviço que implementa o protocolo [*WS-Management*](windows-remote-management-glossary.md) , o diagnóstico de hardware e o controle por meio de [*BMCs*](windows-remote-management-glossary.md)(controladores de gerenciamento da baseboard), além de uma API com e [objetos de script](winrm-scripting-api.md) que permitem que você grave aplicativos que se comunicam remotamente por meio do protocolo WS-Management. Para obter mais informações sobre a especificação pública para o protocolo WS-Management, consulte [Web Services for Management (WS – Management)](https://dmtf.org/sites/default/files/standards/documents/DSP0226_1.2.0.pdf).

## <a name="components-of-winrm-and-hardware-management"></a>Componentes de gerenciamento de hardware e WinRM

Veja a seguir uma lista de componentes e recursos fornecidos pelo WinRM e pelo monitoramento de hardware:

-   [API de script do WinRM](winrm-scripting-api.md)

    Essa API de script permite que você obtenha dados de computadores remotos usando scripts que executam operações de protocolo WS-Management.

-   **WinRM. cmd**

    Essa ferramenta de linha de comando para gerenciamento do sistema é implementada em um arquivo de Visual Basic Scripting Edition (Winrm.vbs) escrito usando a API de script do WinRM. Essa ferramenta permite que um administrador configure o WinRM e obtenha dados ou gerencie recursos. Para obter mais informações, consulte a ajuda online fornecida pela linha de comando **WinRM** **/?**.

-   **Winrs.exe**

    Essa ferramenta de linha de comando permite que os administradores executem a maioria dos comandos Cmd.exe remotamente usando o protocolo WS-Management. Para obter mais informações, consulte a ajuda online fornecida pela linha de comando **WinRS** **/?**.

-   Driver de IPMI (interface de gerenciamento de plataforma inteligente) e provedor WMI

    O gerenciamento de hardware por meio do provedor de [*IPMI (interface de gerenciamento de plataforma inteligente)*](windows-remote-management-glossary.md) e do driver permite controlar e diagnosticar o hardware de servidor remoto por meio do BMCs quando o sistema operacional não está em execução ou implantado.

    Para obter mais informações, consulte o [provedor de IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).

-   Serviço WMI

    O serviço WMI continua sendo executado lado a lado com o WinRM e fornece dados ou controle solicitados por meio do [*plug-in WMI*](windows-remote-management-glossary.md). Você pode continuar a obter dados de classes WMI padrão, como o [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process), bem como dados fornecidos pelo IPMI. Para obter mais informações sobre a configuração e a instalação necessárias para o WinRM, consulte [introdução ao gerenciamento de hardware](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)).

-   Protocolo WS-Management

    O protocolo WS-Management, um protocolo amigável para firewall baseado em SOAP, foi projetado para sistemas para localizar e trocar informações de gerenciamento. A intenção da especificação do protocolo WS-Management é fornecer interoperabilidade e consistência para sistemas empresariais que têm computadores em execução em uma variedade de sistemas operacionais de diferentes fornecedores.

    WS-Management protocolo baseia-se nas especificações de serviço Web padrão a seguir: HTTPS, SOAP sobre HTTP (perfil WS-I), SOAP 1,2, WS-Addressing, WS-Transfer, WS-Enumeration e WS-Eventing. Para obter mais informações sobre o rascunho atual da especificação, consulte a [página de índice especificações de gerenciamento](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).

## <a name="working-with-winrm"></a>Trabalhando com o WinRM

Para obter mais informações sobre como escrever scripts WinRM, consulte [usando gerenciamento remoto do Windows](using-windows-remote-management.md).

A tabela a seguir lista os tópicos que fornecem informações sobre o protocolo WS-Management, WinRM e WMI, como especificar recursos de gerenciamento, como unidades de disco ou processos.



| Tópico                                                                                                                            | Descrição                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Instalação e configuração para Gerenciamento Remoto do Windows](installation-and-configuration-for-windows-remote-management.md) | O [*ouvinte*](windows-remote-management-glossary.md) do WinRM requer configuração nos computadores cliente e servidor.                                                                                                                                                                                                                               |
| [Arquitetura de Gerenciamento Remoto do Windows](windows-remote-management-architecture.md)                                             | Diagrama que ilustra os componentes do WinRM e quais componentes são encontrados em computadores cliente e servidor.                                                                                                                                                                                                                                                               |
| [Protocolo WS-Management](ws-management-protocol.md)                                                                             | Descrição do protocolo de WS-Management público padrão para envio e recebimento remoto de dados de gerenciamento para qualquer dispositivo de computador que implemente o protocolo.                                                                                                                                                                                                             |
| [Criando scripts no Gerenciamento Remoto do Windows](scripting-in-windows-remote-management.md)                                             | A API de script do WinRM é semelhante às ações do protocolo WS-Management. Os dados recuperados por scripts são formatados em XML, não em objetos.                                                                                                                                                                                                                                  |
| [Autenticação para conexões remotas](authentication-for-remote-connections.md)                                               | O protocolo WS-Management mantém a segurança para transferência de dados entre computadores ao dar suporte a vários métodos padrão de autenticação e criptografia de mensagens.                                                                                                                                                                                                                |
| [Gerenciamento Remoto do Windows e WMI](windows-remote-management-and-wmi.md)                                                       | Como o WinRM é integrado ao [Instrumentação de gerenciamento do Windows (WMI)](/windows/desktop/WmiSdk/wmi-start-page), você pode obter dados do WMI com scripts ou aplicativos que usam a [API de script do WinRM](winrm-scripting-api.md) ou por meio da ferramenta de linha de comando WinRM.                                                                                                                     |
| [URIs do Recurso](resource-uris.md)                                                                                               | Um [*URI de recurso*](windows-remote-management-glossary.md) é um identificador para uma operação de gerenciamento ou valor. Por exemplo, unidades de disco representam um tipo de recurso.                                                                                                                                                                              |
| [Gerenciamento de hardware remoto](remote-hardware-management.md)                                                                     | O [provedor de IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) fornece [classes](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) e dados que descrevem o domínio de gerenciamento de hardware do BMC (Baseboard Management Controller), os sistemas de computador da BMC no domínio e os sensores do BMC. Outros objetos representam o SEL (log de eventos do sistema) do BMC e as mensagens no log. |
| [Eventos](events.md)                                                                                                             | Você não pode obter eventos por meio de script do WinRM, mas pode usar a ferramenta de linha de comando Wevtutil.exe para exibir eventos do [coletor de eventos](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) .                                                                                                                                                                                        |



 

 

 