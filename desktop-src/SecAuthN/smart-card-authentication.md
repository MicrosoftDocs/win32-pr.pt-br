---
description: Autenticação de cartão inteligente
ms.assetid: cb5c80ea-c15e-4f68-a94b-b458d69ff474
title: Autenticação de cartão inteligente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6241d323f4c5e982fee96f44002da316d5d645d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751611"
---
# <a name="smart-card-authentication"></a>Autenticação de cartão inteligente

As partes básicas do [*subsistema de cartão inteligente*](../secgloss/s-gly.md) são baseadas em padrões de PC/SC (consulte as especificações em [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/) ). Essas partes básicas incluem:

-   Um [*Gerenciador de recursos*](../secgloss/r-gly.md) que usa uma API do Windows.
-   Uma [*interface do usuário*](../secgloss/u-gly.md) que funciona com o Gerenciador de recursos.
-   Vários [*provedores de serviço*](../secgloss/s-gly.md) base que fornecem acesso a serviços específicos. Ao contrário da API do Windows do Gerenciador de recursos, os provedores de serviço usam um modelo de interface COM para fornecer serviços de [*cartão inteligente*](../secgloss/s-gly.md) .

A ilustração a seguir mostra as relações dessas partes na arquitetura geral do cartão inteligente.

![arquitetura de cartão inteligente](images/smartovr2a.png)

Para obter informações sobre como o [*subsistema de cartão inteligente*](../secgloss/s-gly.md) funciona com outros serviços disponíveis no Microsoft Internet Security Framework, consulte [relação a outros serviços](relation-to-other-services.md).

Para obter informações sobre a autenticação de cartão inteligente, consulte os tópicos a seguir.



| Tópicos                                                                      | Sumário                                                                                                                                                                                                                                           |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Conceitos de cartão inteligente](smart-card-concepts.md)<br/>                   | Conceitos básicos e a descrição da interação entre usuários e cartões inteligentes.<br/>                                                                                                                                                        |
| [Gerenciador de recursos de cartão inteligente](smart-card-resource-manager.md)<br/>   | Informações sobre a API do Gerenciador de recursos, que gerencia o acesso a [*leitores*](../secgloss/r-gly.md) e a [*cartões inteligentes*](../secgloss/s-gly.md).<br/> |
| [Interface do usuário do cartão inteligente](smart-card-user-interface.md)<br/>       | Informações sobre a [*caixa de diálogo comum do cartão inteligente*](../secgloss/s-gly.md).<br/>                                                                                   |
| [Provedores de serviço de cartão inteligente](smart-card-service-providers.md)<br/> | Informações sobre interfaces, comandos e wrappers que fornecem recursos de cartão inteligente.<br/>                                                                                                                                              |



 

Além disso, os desenvolvimentos de cartão inteligente atuais da Microsoft podem ser encontrados em [https://www.microsoft.com/whdc/device/input/smartcard/default.mspx](https://www.microsoft.com/whdc/device/input/smartcard/default.mspx) .

 

 
