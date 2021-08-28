---
description: A lista a seguir contém os recursos com suporte do TAPI MSP.
ms.assetid: e36bba94-1fa7-4514-9f8a-bcd690b04d73
title: Recursos com suporte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32f0a37664a578bd091ce9972c1979dc7d22f4db33ab2f8eb803bc2c83642f47
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080506"
---
# <a name="features-supported"></a>Recursos com suporte

A lista a seguir contém os recursos com suporte do TAPI MSP.

-   Implementa um MSP que lida com um único endereço por instância do MSP. Vários endereços like são tratados instando o MSP várias vezes. Isso simplifica muito a implementação do MSP e das classes base.
-   Implementa todas as interfaces MSPI, incluindo [**ITMSPAddress,**](/windows/desktop/api/msp/nn-msp-itmspaddress) [**ITTerminalSupport,**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol)e [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream).
-   Implementa terminais estáticos prontos para uso para áudio e vídeo.
-   Implementa classes base de terminal genéricas. Essas classes base de terminal são usadas pelas implementações de terminal estático mencionadas acima e pelas implementações de terminais dinâmicos encontrados em Termmgr.dll. O MSP também pode usá-los para implementar terminais adicionais.
-   Usa o Gerenciador de Terminal para lidar com terminais dinâmicos. Cria terminais dinâmicos em um thread de trabalho com uma bomba de mensagem (para liberar aplicativos de console de ter que processar mensagens de janela para terminais de renderização de vídeo e simplificar problemas de sincronização).
-   Dá suporte a chamadas que usam um grafo de filtro por fluxo.
-   Implementa a manipulação de eventos de grafo.
-   Usa as APIs de pooling de threads, em conjunto com um thread de trabalho próprio, para manipular eventos.
-   Usa as APIs de rastreamento do Windows 2000 (originalmente desenvolvidas para o projeto de roteamento) juntamente com lógica adicional para fornecer um mecanismo de registro em log flexível e genérico que pode fazer logon simultaneamente em qualquer combinação do seguinte: um depurador de modo kernel ou usuário; uma janela separada do console com mensagens de log separadas por componente; um arquivo de log.
-   Executa free-threaded.

 

 
