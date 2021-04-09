---
title: Usando Gerenciamento Remoto do Windows
description: O Gerenciamento Remoto do Windows destina-se a melhorar o gerenciamento de hardware em um ambiente de rede com vários dispositivos que executam uma variedade de sistemas operacionais.
ms.assetid: 6ee2b238-5bc2-4274-b7ca-49dbc728d8f1
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0c2934694de5913b467521510179fffdb220b601
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084723"
---
# <a name="using-windows-remote-management"></a>Usando Gerenciamento Remoto do Windows

O Gerenciamento Remoto do Windows destina-se a melhorar o gerenciamento de hardware em um ambiente de rede com vários dispositivos que executam uma variedade de sistemas operacionais. Todo o projeto do serviço se concentra no monitoramento e gerenciamento de computadores remotos, implementando um protocolo padrão interoperável.

Como a [API de script do WinRM](winrm-scripting-api.md) e a [API do WinRM C++](winrm-c---api.md) implementam e modelam de forma minuciosa as operações definidas para o protocolo WS-Management, os scripts e os aplicativos recebem fluxos de XML em resposta a solicitações. Os parâmetros de entrada para chamadas de método devem ser construídos em XML. Você pode usar os métodos da API do [MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85)) para exibir ou construir cadeias de caracteres XML. Para obter um exemplo, consulte [exibindo a saída XML de scripts do WinRM](displaying-xml-output-from-winrm-scripts.md).

A lista a seguir inclui tópicos que descrevem como usar o script do WinRM:

-   [Detectando se um computador remoto dá suporte ao protocolo WS-Management](detecting-whether-a-remote-computer-supports-ws-management-protocol.md)
-   [Obtendo dados do computador local](obtaining-data-from-the-local-computer.md)
-   [Obtendo dados de um computador remoto](obtaining-data-from-a-remote-computer.md)
-   [Enumerando ou listando todas as instâncias de um recurso](enumerating-or-listing-all-instances-of-a-resource.md)
-   [Consultando instâncias específicas de um recurso](querying-for-specific-instances-of-a-resource.md)
-   [Exibindo a saída XML de scripts do WinRM](displaying-xml-output-from-winrm-scripts.md)

## <a name="tracing-winrm-activity"></a>Rastreando atividade do WinRM

Como o WinRM obtém dados por meio de [Instrumentação de gerenciamento do Windows (WMI)](/windows/desktop/WmiSdk/wmi-start-page), você pode rastrear a atividade do WMI resultante de mensagens do WinRM. A partir do Windows Vista, o serviço WMI não usa mais os [arquivos de log do WMI](/windows/desktop/WmiSdk/wmi-log-files). Em vez disso, ele usa o ETW ( [rastreamento de eventos](/windows/desktop/ETW/event-tracing-portal) ) e eventos estão disponíveis por meio da interface do usuário do **Visualizador de eventos** ou da ferramenta de linha de comando Evtutil.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gerenciamento Remoto do Windows](portal.md)
</dt> <dt>

[Sobre Gerenciamento Remoto do Windows](about-windows-remote-management.md)
</dt> <dt>

[Referência de Gerenciamento Remoto do Windows](windows-remote-management-reference.md)
</dt> <dt>

[Criando scripts no Gerenciamento Remoto do Windows](scripting-in-windows-remote-management.md)
</dt> </dl>

 

 