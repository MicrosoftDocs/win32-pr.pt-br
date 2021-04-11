---
description: A lista a seguir contém os recursos compatíveis com TAPI MSP.
ms.assetid: e36bba94-1fa7-4514-9f8a-bcd690b04d73
title: Recursos com suporte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00d10fd9ac787483b8dfa6e15046a733992adb97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164501"
---
# <a name="features-supported"></a>Recursos com suporte

A lista a seguir contém os recursos compatíveis com TAPI MSP.

-   Implementa um MSP que manipula um único endereço por instância do MSP. Vários endereços like são tratados instanciando o MSP várias vezes. Isso simplifica muito a implementação do MSP e das classes base.
-   Implementa todas as interfaces MSPI, incluindo [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress), [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport), [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol)e [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream).
-   Implementa terminais estáticos prontos para uso para áudio e vídeo.
-   Implementa classes base de terminal genéricas. Essas classes de base de dados de terminal são usadas pelas implementações de terminais estáticas mencionadas acima e pelas implementações de terminais dinâmicos encontrados no Termmgr.dll. O MSP também pode usá-los para implementar terminais adicionais.
-   Usa o Gerenciador de terminal para lidar com terminais dinâmicos. Cria terminais dinâmicos em um thread de trabalho com uma bomba de mensagem (para liberar aplicativos de console de ter que processar mensagens de janela para terminais de renderização de vídeo e para simplificar problemas de sincronização).
-   Dá suporte a chamadas que usam um grafo de filtro por fluxo.
-   Implementa a manipulação de eventos de grafo.
-   Usa as APIs de pool de threads, em conjunto com um thread de trabalho próprio, para manipular eventos.
-   Usa as APIs de rastreamento do Windows 2000 (originalmente desenvolvidas para o projeto de roteamento) junto com a lógica adicional para fornecer um mecanismo de registro em log genérico e flexível que pode fazer logon simultaneamente em qualquer combinação do seguinte: um usuário ou depurador de modo kernel; uma janela de console separada com mensagens de log separadas por componente; um arquivo de log.
-   Executa threads livres.

 

 
