---
description: A operação de transferência permite que um aplicativo envie uma sessão de comunicação conectada no momento para um endereço diferente.
ms.assetid: b1027f09-74e1-4da8-b718-bb55a56dda1d
title: Transferência
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87bb527ad8e0a26ba5e4da341eb15509e8af05e7950d82de92be839e70370c79
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119514536"
---
# <a name="transfer"></a>Transferência

A operação de transferência permite que um aplicativo envie uma sessão de comunicação conectada no momento para um endereço diferente.

A TAPI fornece dois mecanismos para transferir uma sessão atual para um endereço diferente. *A transferência* às escuras permite que uma sessão existente seja transferida para um endereço de destino especificado em uma fase. *A transferência* de consulta requer a existência de uma sessão de consulta além da sessão atual para configurar a transferência e, em seguida, a conclusão da transferência. A escolha entre esses dois tipos é frequentemente baseada em recursos do provedor de serviços porque alguns provedores de serviços não são suportados para transferências às escuras. Em alguns casos, as necessidades do aplicativo podem fazer com que a transferência consultativa seja o método preferencial, mesmo quando a transferência às vezes é possível.

A operação de transferência às escuras é basicamente a mesma em TAPI 2 e TAPI 3, mas a transferência consultativa segue padrões ligeiramente diferentes.

**TAPI 2.x:** A transferência consultativa começa com a invocação [**de lineSetupTransfer,**](/windows/win32/api/tapi/nf-tapi-linesetuptransfer)que coloca a chamada existente em espera de consulta e identifica essa chamada como o destino para a próxima solicitação de conclusão de transferência. A **função lineSetupTransfer** também aloca uma chamada de consultoria que pode ser usada para estabelecer a chamada de consultoria com a parte para a qual a chamada será transferida. O aplicativo pode discar a extensão da parte de destino na chamada de consultoria (usando [**lineDial**](/windows/win32/api/tapi/nf-tapi-linedial)) ou pode soltar e desalocar a chamada de consulta e, em vez disso, ativar uma chamada mantida existente (usando [**lineUnhold**](/windows/win32/api/tapi/nf-tapi-lineunhold)), se tiver suporte pela opção. Enquanto a chamada inicial está em espera de consulta e a chamada de consulta está ativa, o aplicativo pode alternar entre essas chamadas usando [**lineSwapHold**](/windows/win32/api/tapi/nf-tapi-lineswaphold).

**TAPI 2.x:** Os aplicativos concluem a transferência consultativa [**usando lineCompleteTransfer.**](/windows/win32/api/tapi/nf-tapi-linecompletetransfer) Ambas as chamadas serão revertidas para o *estado ocioso.*

Os aplicativos podem usar o recurso de "transferência em uma etapa" de muitos PBXs (um único pressionamento de botão para estabelecer uma transferência de consulta) definindo o parâmetro *lpCallParams* como o membro **LINECALLPARAMFLAGS \_ ONESTEPTRANSFER** das [ \_ constantes LINECALLPARAMFLAGS](./linecallparamflags--constants.md) ao chamar [**lineSetupTransfer**](/windows/win32/api/tapi/nf-tapi-linesetuptransfer).

**TAPI 3.x:** A transferência consultativa começa com o [**uso de ITAddress::CreateCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall) para criar uma chamada de consultoria para o novo endereço de destino. [**ITBasicCallControl::Transfer**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-transfer) é chamado no objeto de chamada original usando um ponteiro para o novo objeto de chamada de consulta como um parâmetro. Chamar [**ITBasicCallControl::Concluir no**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-finish) objeto de chamada de consulta conclui a transferência.

O aplicativo deve liberar recursos de sessão após a conclusão bem-sucedida de uma operação de transferência.

Nem todos os provedores de serviços suportam o uso dessa operação.

**TAPI 2.x:** Consulte [**lineBlindTransfer**](/windows/win32/api/tapi/nf-tapi-lineblindtransfer), [**lineSetupTransfer**](/windows/win32/api/tapi/nf-tapi-linesetuptransfer), [**lineCompleteTransfer**](/windows/win32/api/tapi/nf-tapi-linecompletetransfer).

**TAPI 3.x:** Consulte [**ITBasicCallControl::BlindTransfer**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-blindtransfer), [**ITAddress::CreateCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall), [**ITBasicCallControl::Transfer**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-transfer), [**ITBasicCallControl::Finish**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-finish).

 

 
