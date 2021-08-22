---
description: A operação de parque permite que um aplicativo envie uma sessão para um endereço especial em que ela será mantida até que ela seja desempareada.
ms.assetid: 6a82f03e-d8fd-4d0b-8f5d-f7934ba86759
title: Parque
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fc09067ad40bc965a6cd909d911de0070138e1d27addb552d728eff2ed60dde
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119335526"
---
# <a name="park"></a>Parque

A operação de parque permite que um aplicativo envie uma sessão para um endereço especial em que ela será mantida até que ela seja desempareada. Do ponto de vista do aplicativo, isso se parece muito com uma transferência. Para a parte na outra extremidade da conexão, isso é semelhante a ser colocado em espera.

A diferença entre o parque e a transferência é que o endereço de conexões não é um ponto de conexão para a sessão, e a sessão não alerta ou tempo máximo. A diferença entre o parque e a espera é que, depois que a operação de parque for concluída, a sessão não será mais associada ao endereço do aplicativo.

Duas formas de estacionamento de uma sessão são fornecidas: *parque direcionado* e parque *não direcionado.* No parque de chamada direcionada, o aplicativo especifica o endereço de destino em que a chamada deve ser ressalvada. Com o parque não direcionado, o provedor de serviços ou o hardware subjacente determina o endereço e o retorna para o aplicativo.

Uma sessão de ressada normalmente entra no estado ocioso depois de ter sido desassociada com êxito e o aplicativo deve liberar os recursos associados a ela. Confira [Encerrar uma sessão](terminate-a-session-ovr.md) para ver um resumo de como fazer isso.

Se o aplicativo desemparecar a sessão, novos recursos de sessão serão alocados mesmo se o aplicativo tiver retornado os ponteiros anteriores, portanto, a falha ao fazer versões adequadas poderá resultar em uma variedade de problemas.

Alguns provedores de serviços podem lembrar o usuário depois que uma sessão tiver sido desamocada por algum tempo. O aplicativo vê uma chamada de oferta com um motivo [de chamada](reason-ovr.md) definido como lembrete.

Nem todos os provedores de serviços suportam o uso dessa operação.

**TAPI 2.x:** Consulte [**linePark**](/windows/win32/api/tapi/nf-tapi-linepark), [**lineUnpark**](/windows/win32/api/tapi/nf-tapi-lineunpark).

**TAPI 3:** Consulte [**ITBasicCallControl::P arkDirect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-parkdirect), [**ITBasicCallControl::P arkIndirect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-parkindirect), [**ITBasicCallControl::Unpark**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-unpark).

 

 
