---
title: Sobre o CD Desembolso
description: Sobre o CD Desembolso
ms.assetid: 1a179284-2909-4fc0-82be-996794ee4f31
keywords:
- Windows Media Player, CD
- Windows Media Player modelo de objeto, CD
- modelo de objeto, CD
- Windows Media Player ActiveX controle,CD
- ActiveX controle,CD
- Windows Media Player Controle ActiveX dispositivo móvel, CD
- Windows Media Player Móvel, CD
- CD de 10000012
- CDs de 10000001
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0efab14a97f9cc24c4137e5d939bc9562b1fc073cd551bd83388de4ba1de0b65
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903596"
---
# <a name="about-cd-ripping"></a>Sobre o CD Desembolso

O Windows Media Player SDK 11 apresenta uma nova funcionalidade para copiar faixas de áudio de CDs para o computador do usuário. Esse processo é *chamado de "10000001"*

Quando você tira faixas de áudio usando as interfaces do SDK do Windows Media Player, as faixas de música resultantes são criadas usando as configurações definidas pelo usuário na caixa de diálogo Windows Media Player **Opções.**

Para enumerar as unidades de CD no computador do usuário, use a interface **IWMPCdromCollection.** Você recupera um ponteiro para essa interface chamando [IWMPCore::get \_ cdromCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection). Usando os métodos **count** e **item,** você pode iterar a coleção para recuperar um ponteiro de interface **IWMPCdrom** para cada unidade de CD no computador do usuário. A **interface IWMPCdrom** representa uma unidade de CD individual. Antes de começar a usar um CD, primeiro você deve chamar **QueryInterface** por meio de um ponteiro **IWMPCdrom** para recuperar um ponteiro para a interface **IWMPCdromRip.**

Para iniciar a operação de resserção, basta [chamar IWMPCdromRip::startRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-startrip). Você pode monitorar o progresso da operação de redução chamando periodicamente [IWMPCdromRip::getripProgress \_ ](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripprogress). Esse método recupera um valor de progresso para toda a operação de responsabilidade. O valor recuperado é um número que representa a porcentagem de conclusão do processo. Você pode monitorar o estado da operação de resserção chamando [periodicamente IWMPCdromRip::getstate \_ ](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripstate). Esse método recupera um [valor de enumeração WMPRipState](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate) que indica se a operação está em andamento ou interrompida. Você também pode monitorar o estado da operação de manipulação manipulando o evento [IWMPEvents3::CdromRipStateChange.](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromripstatechange) Você deve ter cuidado para comparar o ponteiro **IWMPCdromRip** (fornecido pelo evento) com o ponteiro que representa a operação de resserção para garantir que o evento foi gerado pela sua operação. Você pode interromper a operação de resserção chamando [IWMPCdromRip::stopRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-stoprip).

Para receber notificações de erro sobre uma operação de falha, você pode manipular o evento [IWMPEvents3::CdromRipMediaError.](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromripmediaerror) Assim **como CdromRipStateChange**, esse evento fornece um ponteiro de interface **IWMPCdromRip** que representa a operação de replicação que gerou o evento. O evento também fornece um **ponteiro IDispatch** que representa o item de mídia que gerou o evento. Você pode chamar **QueryInterface por** meio desse ponteiro para recuperar um **ponteiro IWMPMedia.**

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre o modelo de objeto do player**](about-the-player-object-model.md)
</dt> </dl>

 

 




