---
description: Autenticação de cartão inteligente
ms.assetid: cb5c80ea-c15e-4f68-a94b-b458d69ff474
title: Autenticação de cartão inteligente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78bccfa9e762c137e332c26b5375584658c22718d336800b6dc73cf056ebde1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118917998"
---
# <a name="smart-card-authentication"></a>Autenticação de cartão inteligente

As partes básicas do [*subsistema de cartão*](../secgloss/s-gly.md) inteligente são baseadas em padrões de PC/SC (consulte as especificações em [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/) ). Essas partes básicas incluem:

-   Um [*gerenciador de recursos*](../secgloss/r-gly.md) que usa uma API Windows aplicativo.
-   Uma [*interface do*](../secgloss/u-gly.md) usuário que funciona com o gerenciador de recursos.
-   Vários [*provedores de serviços básicos*](../secgloss/s-gly.md) que fornecem acesso a serviços específicos. Ao contrário da API de Windows do gerenciador de recursos, os provedores de serviços usam um modelo de interface COM para fornecer [*serviços de cartão*](../secgloss/s-gly.md) inteligente.

A ilustração a seguir mostra as relações dessas partes na arquitetura geral do cartão inteligente.

![arquitetura de cartão inteligente](images/smartovr2a.png)

Para obter informações sobre como o [*subsistema*](../secgloss/s-gly.md) de cartão inteligente funciona com outros serviços disponíveis no Microsoft Internet Security Framework, consulte [Relation to Other Services](relation-to-other-services.md).

Para obter informações sobre a autenticação de cartão inteligente, consulte os tópicos a seguir.



| Tópicos                                                                      | Sumário                                                                                                                                                                                                                                           |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Conceitos de cartão inteligente](smart-card-concepts.md)<br/>                   | Conceitos básicos e descrição da interação entre usuários e cartões inteligentes.<br/>                                                                                                                                                        |
| [Cartão inteligente Resource Manager](smart-card-resource-manager.md)<br/>   | Informações sobre a API do Resource Manager, que gerencia o acesso aos leitores [*e*](../secgloss/r-gly.md) aos [*cartões inteligentes.*](../secgloss/s-gly.md)<br/> |
| [Cartão inteligente Interface do Usuário](smart-card-user-interface.md)<br/>       | Informações sobre a [*caixa de diálogo comum do cartão inteligente*](../secgloss/s-gly.md).<br/>                                                                                   |
| [Provedores de serviços de cartão inteligente](smart-card-service-providers.md)<br/> | Informações sobre interfaces, comandos e wrappers que fornecem recursos de cartão inteligente.<br/>                                                                                                                                              |



 

Além disso, os desenvolvimentos atuais de cartão inteligente da Microsoft podem ser encontrados em [https://www.microsoft.com/whdc/device/input/smartcard/default.mspx](https://www.microsoft.com/whdc/device/input/smartcard/default.mspx) .

 

 
