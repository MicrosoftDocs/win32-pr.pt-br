---
description: A função phoneDevSpecific e sua mensagem PHONE DEVSPECIFIC associada permitem que um aplicativo acesse recursos de telefone específicos do dispositivo que não estão disponíveis por meio dos serviços de telefonia comuns para \_ telefones.
ms.assetid: b4c8d721-26e4-4895-9f09-0f67fe4d346b
title: Funções e mensagens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61cabdc271548e42b20de695296321f5f5ab0fdbe45a246be2b7ccb1993ee5d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660726"
---
# <a name="functions-and-messages"></a>Funções e mensagens

A [**função phoneDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific) e sua mensagem [**PHONE \_ DEVSPECIFIC**](phone-devspecific.md) associada permitem que um aplicativo acesse recursos de telefone específicos do dispositivo que não estão disponíveis por meio dos serviços de telefonia comuns para telefones. Em outras palavras, **phoneDevSpecific** é a função de escape específica do dispositivo que permite extensões dependentes do fornecedor e PHONE DEVSPECIFIC é a mensagem específica do dispositivo enviada ao \_ aplicativo.

O perfil de parâmetro [**da função phoneDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific) é genérico nessa pequena interpretação dos parâmetros feita pela TAPI. Em vez disso, a interpretação dos parâmetros é definida pelo provedor de serviços e deve ser compreendida por um aplicativo que os usa. Os parâmetros são simplesmente passados pela TAPI do aplicativo para o provedor de serviços. Um aplicativo que depende de extensões específicas do dispositivo geralmente não funcionará com outros provedores de serviços, mas os aplicativos gravados nos serviços de telefonia comuns funcionarão com o provedor de serviços estendidos.

 

 



