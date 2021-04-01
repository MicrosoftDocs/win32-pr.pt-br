---
description: A função phoneDevSpecific e sua mensagem DEVSPECIFIC de telefone associada \_ permitem que um aplicativo acesse recursos de telefone específicos do dispositivo que não estão disponíveis por meio dos serviços de telefonia comuns para telefones.
ms.assetid: b4c8d721-26e4-4895-9f09-0f67fe4d346b
title: Funções e mensagens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 292f85e2ea57ac11da8150d4d0a183c7c4fd2c88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921696"
---
# <a name="functions-and-messages"></a>Funções e mensagens

A função [**phoneDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific) e sua mensagem [**\_ DEVSPECIFIC de telefone**](phone-devspecific.md) associada permitem que um aplicativo acesse recursos de telefone específicos do dispositivo que não estão disponíveis por meio dos serviços de telefonia comuns para telefones. Em outras palavras, **phoneDevSpecific** é a função de escape específica do dispositivo que permite extensões dependentes do fornecedor, e \_ o Phone DEVSPECIFIC é a mensagem específica do dispositivo que é enviada para o aplicativo.

O perfil de parâmetro da função [**phoneDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific) é genérico, pois essa pequena interpretação dos parâmetros é feita pela TAPI. Em vez disso, a interpretação dos parâmetros é definida pelo provedor de serviços e deve ser compreendida por um aplicativo que os utilize. Os parâmetros são simplesmente passados pela TAPI do aplicativo para o provedor de serviços. Um aplicativo que se baseia em extensões específicas do dispositivo geralmente não funcionará com outros provedores de serviço, mas os aplicativos gravados nos serviços de telefone de telefonia comuns funcionarão com o provedor de serviços estendido.

 

 



