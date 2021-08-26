---
description: Antes que o subsistema de cartão inteligente possa encontrar um cartão inteligente, o cartão inteligente deve ser introduzido no sistema.
ms.assetid: 5b331d7d-9440-4e0d-a73b-48a2a556c31c
title: Introdução de cartões inteligentes ao sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07cd65135e1580792135a1042729f2002f4437697fa0548a4f6cd776650485b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015706"
---
# <a name="introducing-smart-cards-to-the-system"></a>Introdução de cartões inteligentes ao sistema

Antes que o [*subsistema de cartão inteligente*](../secgloss/s-gly.md) possa encontrar um [*cartão inteligente*](../secgloss/s-gly.md), o cartão inteligente deve ser introduzido no sistema. Isso normalmente é feito com uma ferramenta de configuração de cartão inteligente fornecida pelo fabricante do cartão. a ferramenta pode ser um programa em um disquete (com o cartão inteligente), um controle de ActiveX disponível em um site e assim por diante.

A ferramenta de instalação deve fornecer as seguintes informações sobre o cartão:

-   Sua [*cadeia de caracteres ATR*](../secgloss/a-gly.md)e uma máscara opcional para usar como uma ajuda na identificação do cartão.
-   Uma lista de interfaces de cartão inteligente com suporte no cartão.
-   Um nome de exibição para o cartão a ser usado na identificação do cartão para o usuário. Na maioria dos casos, o usuário fornecerá isso à ferramenta de instalação.
-   O [*provedor de serviços primário*](../secgloss/p-gly.md) associado ao cartão (opcional) a ser usado ao acessar o cartão por meio de interfaces com.

Para simplificar as ferramentas de instalação e garantir a integridade do [*banco de dados do cartão inteligente*](../secgloss/s-gly.md), o subsistema de cartão inteligente fornece as duas funções a seguir. [**SCardIntroduceCardType**](/windows/desktop/api/Winscard/nf-winscard-scardintroducecardtypea) introduz um cartão inteligente no banco de dados e o [**SCardForgetCardType**](/windows/desktop/api/Winscard/nf-winscard-scardforgetcardtypea) o Remove do banco de dados.

 

 
