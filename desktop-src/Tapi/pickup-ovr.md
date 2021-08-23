---
description: A operação de retirada permite que um aplicativo responda a uma sessão que está alertando em outro endereço. O aplicativo identifica o destino da retirada e retorna um identificador de sessão para a chamada retirada.
ms.assetid: 3dfbb5c0-b533-403f-ad6c-b9e1b52ab47a
title: Separação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 288510d2d9e2eb2ed6e9a5cc5c58f6957b933b7d43db951eb330dd081a4c446f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873056"
---
# <a name="pickup"></a>Separação

A operação de retirada permite que um aplicativo responda a uma sessão que está alertando em outro endereço. O aplicativo identifica o destino da retirada e retorna um identificador de sessão para a chamada retirada.

Há várias maneiras de identificar o destino da solicitação de retirada. Primeiro, o aplicativo pode especificar o endereço da parte de alerta. Em segundo lugar, se nenhum endereço for especificado e a opção permitir, o aplicativo poderá pegar qualquer sessão de alerta em seu grupo de retirada. Em terceiro lugar, algumas opções permitem a retirada de um alerta de sessão em um grupo de retirada diferente se o identificador de grupo for especificado.

Alguns sistemas telefônicos importantes dão suporte a uma *transferência por meio* do recurso de bloqueio em aparências de chamada exclusivas em ponte. Nesse esquema, um telefone específico possui uma chamada exclusivamente quando a chamada está ativa, mas quando a chamada está em espera, qualquer telefone que tenha uma aparência da linha pode pegar a chamada.

**TAPI 2. x:** Um aplicativo pode usar uma operação de retirada com um endereço de destino **nulo** para essa finalidade, semelhante a como a função é usada para pegar uma chamada em espera de chamada em uma linha analógica. LINEADDRFEATURE \_ PICKUPHELD indica a existência do recurso.

Se LINEADDRCAPFLAGS \_ PICKUPCALLWAIT for **true**, uma sessão poderá ser selecionada para a qual o usuário tenha forma audível detectado o sinal de espera de chamada, mas para o qual o provedor de serviços não consegue realizar a detecção. Isso dá ao usuário um mecanismo para "responder" uma chamada em espera mesmo que o provedor de serviços não consiga detectar o sinal de espera de chamada. O endereço de destino e a ID do grupo devem ser **nulos** para pegar uma chamada de chamada em espera.

Quando uma sessão tiver sido removida com êxito, o aplicativo receberá uma notificação de alteração de estado com o [motivo](reason-ovr.md) definido como LINECALLREASON \_ pickup.

Nem todos os provedores de serviço dão suporte ao uso desta operação.

**TAPI 2. x:** Consulte [**linePickup**](/windows/win32/api/tapi/nf-tapi-linepickup).

**TAPI 3. x:** Consulte [**ITBasicCallControl::P ickup**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-pickup).

 

 
