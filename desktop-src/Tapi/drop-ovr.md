---
description: Descartar ou desconectar uma sessão encerra a comunicação. O aplicativo tem a opção de enviar informações do usuário no momento da desconexão, se o provedor de serviços oferecer suporte a ela.
ms.assetid: dc348bb2-d564-40f8-afe3-5473c5769fa4
title: Remover
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5821b9778ff59f0c515c7d7d00c1d3709cfdafdc36b6b0f113bceab312ff419b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117945599"
---
# <a name="drop"></a>Remover

Descartar ou desconectar uma sessão encerra a comunicação. O aplicativo tem a opção de enviar informações do usuário no momento da desconexão, se o provedor de serviços oferecer suporte a ela.

Os motivos usuais para descartar uma sessão é que um usuário solicitou uma desconexão ou a outra extremidade da sessão foi descartada. Uma operação de remoção também pode ser chamada quando a TAPI oferece uma sessão para o aplicativo. Se o provedor de serviços oferecer suporte a isso, o efeito é que o aplicativo rejeita a chamada.

Ao invocar uma operação de remoção, as sessões relacionadas às vezes podem ser também afetadas. Por exemplo, remover uma chamada de conferência pode descartar todos os participantes individuais. As mensagens de alteração de estado são enviadas para o aplicativo para todas as chamadas cujo estado é afetado.

Em várias configurações de ponte ou de linha de terceiros quando várias partes estão na chamada, uma operação de soltar pode não limpar realmente a chamada. Por exemplo, em uma situação de ponte, a chamada pode não ser descartada porque o status de outras estações na chamada pode governar. Em vez disso, a chamada pode ser simplesmente alterada para o estado inativo enquanto estiver restante conectada em outras estações.

Após uma operação de soltar, o identificador de sessão e a maioria dos recursos associados à sessão permanecerão utilizáveis para a maioria das operações de consulta. Quando um aplicativo não exige mais esses recursos, ele deve [encerrar a sessão](terminate-a-session-ovr.md) para evitar vazamentos de memória.

**TAPI 2. x:** Consulte [**lineDrop**](/windows/win32/api/tapi/nf-tapi-linedrop).

**TAPI 3. x:** Consulte [**ITBasicCallControl::D isconnect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect).

 

 
