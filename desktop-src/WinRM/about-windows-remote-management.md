---
title: Sobre Windows gerenciamento remoto
description: Windows O Gerenciamento Remoto é um componente dos recursos Windows gerenciamento de hardware que gerenciam o hardware do servidor local e remotamente.
ms.assetid: f58add53-0746-4423-9ab8-02ba05f82fa7
ms.tgt_platform: multiple
keywords:
- Sobre Windows gerenciamento remoto
- Windows Gerenciamento Remoto, sobre
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a83df38de4af354f826b9bbba59ddab76e1b656c72e1c3dc74301da883f875cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858906"
---
# <a name="about-windows-remote-management"></a>Sobre Windows gerenciamento remoto

Windows O Gerenciamento Remoto é um componente dos recursos [Windows gerenciamento de hardware](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) que gerenciam o hardware do servidor local e remotamente. Esses recursos incluem um serviço que implementa o protocolo [*WS-Management,*](windows-remote-management-glossary.md) o diagnóstico de hardware e o controle por meio de [*BMCs*](windows-remote-management-glossary.md)(controladores de gerenciamento de placa base) e uma API COM e [objetos de script](winrm-scripting-api.md) que permitem escrever aplicativos que se comunicam remotamente por meio do protocolo WS-Management. Para obter mais informações sobre a especificação pública WS-Management protocolo, consulte [Serviços Web para Gerenciamento (WS–Management).](https://dmtf.org/sites/default/files/standards/documents/DSP0226_1.2.0.pdf)

## <a name="components-of-winrm-and-hardware-management"></a>Componentes do Gerenciamento de Hardware e WinRM

Veja a seguir uma lista de componentes e recursos fornecidos pelo WinRM e pelo monitoramento de hardware:

-   [API de Script WinRM](winrm-scripting-api.md)

    Essa API de script permite que você obtenha dados de computadores remotos usando scripts que executam WS-Management de protocolo.

-   **Winrm.cmd**

    Essa ferramenta de linha de comando para gerenciamento de sistema é implementada em um arquivo Visual Basic Scripting Edition (Winrm.vbs) escrito usando a API de script WinRM. Essa ferramenta permite que um administrador configure o WinRM e receba dados ou gerencie recursos. Para obter mais informações, consulte a ajuda online fornecida pela linha de comando **Winrm** **/?**.

-   **Winrs.exe**

    Essa ferramenta de linha de comando permite que os administradores executem remotamente a maioria dos Cmd.exe usando o protocolo WS-Management segurança. Para obter mais informações, consulte a ajuda online fornecida pela linha de comando **Winrs** **/?**.

-   Driver IPMI (Interface de Gerenciamento de Plataforma Inteligente) e provedor WMI

    O gerenciamento de hardware por meio do provedor e driver [*IPMI (Interface*](windows-remote-management-glossary.md) de Gerenciamento de Plataforma Inteligente) permite controlar e diagnosticar o hardware do servidor remoto por meio de BMCs quando o sistema operacional não está em execução ou implantado.

    Para obter mais informações, consulte o [Provedor IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).

-   Serviço WMI

    O serviço WMI continua sendo executado lado a lado com o WinRM e fornece dados ou controle solicitados por meio do [*plug-in WMI*](windows-remote-management-glossary.md). Você pode continuar a obter dados de classes WMI padrão, como [**Processo Win32, \_**](/windows/desktop/CIMWin32Prov/win32-process)bem como dados fornecidos por IPMI. Para obter mais informações sobre a configuração e a instalação necessárias para o WinRM, consulte [Introdução ao Gerenciamento de Hardware.](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10))

-   WS-Management protocolo

    WS-Management protocolo, um protocolo amigável baseado em SOAP, foi projetado para que os sistemas localizem e troquem informações de gerenciamento. A intenção da especificação WS-Management protocolo é fornecer interoperabilidade e consistência para sistemas empresariais que têm computadores em execução em uma variedade de sistemas operacionais de fornecedores diferentes.

    WS-Management protocolo é baseado nas seguintes especificações de serviço Web padrão: HTTPS, SOAP sobre HTTP (perfil WS-I), SOAP 1.2, WS-Addressing, WS-Transfer, WS-Enumeration e WS-Eventing. Para obter mais informações sobre o rascunho atual da especificação, consulte a [Página índice de especificações de gerenciamento](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).

## <a name="working-with-winrm"></a>Trabalhando com o WinRM

Para obter mais informações sobre como escrever scripts WinRM, consulte [Using Windows Remote Management](using-windows-remote-management.md).

A tabela a seguir lista tópicos que fornecem informações sobre o protocolo WS-Management, WinRM e WMI, como especificar recursos de gerenciamento, como unidades de disco ou processos.



| Tópico                                                                                                                            | Descrição                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Instalação e configuração para Windows Gerenciamento Remoto](installation-and-configuration-for-windows-remote-management.md) | O ouvinte [*winRM*](windows-remote-management-glossary.md) requer configuração em computadores cliente e servidor.                                                                                                                                                                                                                               |
| [Windows Arquitetura de gerenciamento remoto](windows-remote-management-architecture.md)                                             | Diagrama que ilustra os componentes do WinRM e quais componentes são encontrados em computadores cliente e servidor.                                                                                                                                                                                                                                                               |
| [Protocolo WS-Management](ws-management-protocol.md)                                                                             | Descrição do protocolo de WS-Management público para enviar e receber remotamente dados de gerenciamento para qualquer dispositivo de computador que implemente o protocolo.                                                                                                                                                                                                             |
| [Scripts no Windows Gerenciamento Remoto](scripting-in-windows-remote-management.md)                                             | A API de script WinRM é semelhante às ações do protocolo WS-Management. Os dados recuperados por scripts são formatados em XML, não em objetos.                                                                                                                                                                                                                                  |
| [Autenticação para conexões remotas](authentication-for-remote-connections.md)                                               | WS-Management protocolo mantém a segurança para transferência de dados entre computadores, dando suporte a vários métodos padrão de autenticação e criptografia de mensagens.                                                                                                                                                                                                                |
| [Windows Gerenciamento Remoto e WMI](windows-remote-management-and-wmi.md)                                                       | Como o WinRM é integrado ao [WMI (Instrumentação](/windows/desktop/WmiSdk/wmi-start-page)de Gerenciamento de Windows), você pode obter dados WMI com scripts ou aplicativos que usam a API de [Script WinRM](winrm-scripting-api.md) ou por meio da ferramenta de linha de comando Winrm.                                                                                                                     |
| [URIs do Recurso](resource-uris.md)                                                                                               | Um [*URI de recurso*](windows-remote-management-glossary.md) é um identificador para uma operação de gerenciamento ou valor. Por exemplo, as unidades de disco representam um tipo de recurso.                                                                                                                                                                              |
| [Gerenciamento de hardware remoto](remote-hardware-management.md)                                                                     | O [Provedor IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) fornece classes e dados que descrevem o domínio de gerenciamento de hardware do BMC (controlador de placa base), os sistemas de computador BMC no domínio e os sensores do BMC. [](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) Outros objetos representam o SEL (Log de Eventos do Sistema BMC) e as mensagens no log. |
| [Eventos](events.md)                                                                                                             | Não é possível obter eventos por meio do script WinRM, mas você pode usar a Wevtutil.exe de linha de comando para exibir eventos [do Coletor de](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) Eventos.                                                                                                                                                                                        |



 

 

 