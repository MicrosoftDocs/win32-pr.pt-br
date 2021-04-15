---
description: A operação de resposta é uma resposta típica aos aplicativos para uma sessão de comunicações oferecida. Se for bem-sucedida, essa operação fará com que uma sessão faça a transição para o estado conectado.
ms.assetid: 34ac0b34-1d1b-4657-a737-27a4ed9326af
title: Resposta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e08081b32b7ba3a3a24cde3ec37c1a6118582cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104505917"
---
# <a name="answer"></a>Resposta

A operação de resposta é uma resposta típica do aplicativo a uma sessão de comunicações oferecida. Se for bem-sucedida, essa operação fará com que uma sessão faça a transição para o estado conectado.

Em alguns ambientes de telefonia (como o ISDN), onde os alertas do usuário são separados da oferta de chamada, o aplicativo tem a opção de [aceitar](accept-ovr.md) uma chamada antes de responder ou rejeitar ([remover](drop-ovr.md)) ou [redirecionar](redirect-ovr.md) a chamada de *oferta* .

Se uma operação de resposta for executada para uma nova sessão quando uma sessão já estiver ativa, o efeito que ela tem na sessão ativa existente dependerá dos recursos do provedor de serviços. A primeira chamada pode não ser afetada, pode ser descartada automaticamente ou pode ser automaticamente colocada em espera. A TAPI enviará as notificações de eventos apropriadas relacionadas às duas chamadas.

Em uma situação de ponte, se uma chamada estiver conectada, mas no estado ativo, ela poderá ser unida usando a operação de resposta.

O aplicativo tem a opção de enviar informações do usuário no momento da resposta, se o provedor de serviços oferecer suporte a ela.

**TAPI 2. x:** Consulte [**lineAnswer**](/windows/win32/api/tapi/nf-tapi-lineanswer).

**TAPI 3. x:** Consulte [**ITBasicCallControl:: answer**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-answer).

 

 
