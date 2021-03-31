---
description: A operação de transferência permite que um aplicativo envie uma sessão de comunicações conectada no momento a um endereço diferente.
ms.assetid: b1027f09-74e1-4da8-b718-bb55a56dda1d
title: Transferência
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 724b9ade43e41ab95a5baa6dfe7d3269f4e4a174
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011067"
---
# <a name="transfer"></a>Transferência

A operação de transferência permite que um aplicativo envie uma sessão de comunicações conectada no momento a um endereço diferente.

A TAPI fornece dois mecanismos para transferir uma sessão atual para um endereço diferente. A *transferência oculta* permite que uma sessão existente seja transferida para um endereço de destino especificado em uma única fase. A *transferência de consulta* requer a existência de uma sessão de consulta, além da sessão atual, para ser configurada para a transferência e a conclusão da transferência. A escolha entre esses dois tipos é frequentemente baseada em recursos do provedor de serviços, pois alguns provedores de serviços não dão suporte à transferência oculta. Em alguns casos, as necessidades do aplicativo podem fazer com que a transferência de consultoria seja o método preferencial, mesmo onde a transferência oculta é possível.

A operação de transferência oculta é basicamente a mesma sob TAPI 2 e TAPI 3, mas a transferência consultiva segue padrões ligeiramente diferentes.

**TAPI 2. x:** A transferência consultiva começa com a invocação de [**lineSetupTransfer**](/windows/win32/api/tapi/nf-tapi-linesetuptransfer), que coloca a chamada existente na retenção de consulta e identifica essa chamada como o destino para a próxima solicitação de conclusão da transferência. A função **lineSetupTransfer** também aloca uma chamada de consulta que pode ser usada para estabelecer a chamada de consulta com a parte para a qual a chamada será transferida. O aplicativo pode discar a extensão da parte de destino na chamada de consulta (usando [**lineDial**](/windows/win32/api/tapi/nf-tapi-linedial)) ou pode remover e desalocar a chamada de consulta e, em vez disso, ativar uma chamada mantida existente (usando [**lineUnhold**](/windows/win32/api/tapi/nf-tapi-lineunhold)), se houver suporte no comutador. Enquanto a chamada inicial está em um controle de consulta e a chamada de consulta está ativa, o aplicativo pode alternar entre essas chamadas usando [**lineSwapHold**](/windows/win32/api/tapi/nf-tapi-lineswaphold).

**TAPI 2. x:** Os aplicativos concluem a transferência consultiva usando o [**lineCompleteTransfer**](/windows/win32/api/tapi/nf-tapi-linecompletetransfer). Ambas as chamadas serão revertidas para o estado *ocioso* .

Os aplicativos podem usar o recurso de "transferência em uma etapa" de vários PBXs (um único pressionamento de botão para estabelecer uma transferência de consulta) definindo o parâmetro *lpCallParams* para o membro **LINECALLPARAMFLAGS \_ ONESTEPTRANSFER** das [ \_ constantes LINECALLPARAMFLAGS](./linecallparamflags--constants.md) ao chamar [**lineSetupTransfer**](/windows/win32/api/tapi/nf-tapi-linesetuptransfer).

**TAPI 3. x:** A transferência consultiva começa com o uso de [**ITAddress:: createcall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall) para criar uma chamada de consulta para o novo endereço de destino. [**ITBasicCallControl:: Transfer**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-transfer) é chamado no objeto de chamada original usando um ponteiro para o novo objeto de chamada de consulta como um parâmetro. Chamar [**ITBasicCallControl:: Finish**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-finish) no objeto de chamada de consulta, em seguida, conclui a transferência.

O aplicativo deve liberar recursos de sessão após a conclusão bem-sucedida de uma operação de transferência.

Nem todos os provedores de serviço dão suporte ao uso desta operação.

**TAPI 2. x:** Consulte [**lineBlindTransfer**](/windows/win32/api/tapi/nf-tapi-lineblindtransfer), [**lineSetupTransfer**](/windows/win32/api/tapi/nf-tapi-linesetuptransfer), [**lineCompleteTransfer**](/windows/win32/api/tapi/nf-tapi-linecompletetransfer).

**TAPI 3. x:** Consulte [**ITBasicCallControl:: BlindTransfer**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-blindtransfer), [**ITAddress:: createchama**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall), [**ITBasicCallControl:: transferência**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-transfer), [**ITBasicCallControl:: concluir**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-finish).

 

 
