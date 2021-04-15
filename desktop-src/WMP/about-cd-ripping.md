---
title: Sobre a cópia de CD
description: Sobre a cópia de CD
ms.assetid: 1a179284-2909-4fc0-82be-996794ee4f31
keywords:
- Windows Media Player, CD de CDs
- Modelo de objeto do Windows Media Player, cópia de CD
- modelo de objeto, cópia de CD
- Controle ActiveX do Windows Media Player, cópia de CD
- Controle ActiveX, cópia de CD
- Controle ActiveX móvel do Windows Media Player, cópia de CD
- Windows Media Player Mobile, CD-CDs
- CD de CDs, sobre
- copiando CDs, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e28769c6af666e510fb97ebc98e44fadc7c3e472
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "105760904"
---
# <a name="about-cd-ripping"></a>Sobre a cópia de CD

O SDK do Windows Media Player 11 introduz uma nova funcionalidade para copiar faixas de áudio de CDs para o computador do usuário. Esse processo é chamado de *cópia de CDs*.

Quando você copia faixas de áudio usando as interfaces do SDK do Windows Media Player, as faixas de música resultantes são criadas usando as configurações definidas pelo usuário na caixa de diálogo **Opções** do Windows Media Player.

Para enumerar as unidades de CD no computador do usuário, use a interface **IWMPCdromCollection** . Você recupera um ponteiro para essa interface chamando [IWMPCore:: get \_ cdromCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection). Usando os métodos **Count** e **Item** , você pode iterar a coleção para recuperar um ponteiro de interface **IWMPCDROM** para cada unidade de CD no computador do usuário. A interface **IWMPCdrom** representa uma unidade de CD individual. Antes de começar a copiar um CD, você deve primeiro chamar **QueryInterface** por meio de um ponteiro **IWMPCdrom** para recuperar um ponteiro para a interface **IWMPCdromRip** .

Para iniciar a operação de cópia de CDs, basta chamar [IWMPCdromRip:: startRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-startrip). Você pode monitorar o progresso da operação de cópia de CDs chamando periodicamente [IWMPCdromRip:: get \_ ripProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripprogress). Esse método recupera um valor de progresso para toda a operação de cópia de CDs. O valor recuperado é um número que representa a porcentagem de cópia concluída. Você pode monitorar o estado da operação de cópia de CDs chamando periodicamente [IWMPCdromRip:: get \_ ripState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripstate). Esse método recupera um valor de enumeração [WMPRipState](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate) que indica se a operação está em andamento ou foi interrompida. Você também pode monitorar o estado da operação de cópia de CDs manipulando o evento [IWMPEvents3:: CdromRipStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromripstatechange) . Você deve ter cuidado para comparar o ponteiro **IWMPCdromRip** (fornecido pelo evento) com o ponteiro que representa a operação de cópia para garantir que o evento foi gerado pela operação. Você pode interromper a operação de cópia de CDs chamando [IWMPCdromRip:: stopRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-stoprip).

Para receber notificações de erro sobre uma operação de cópia de CDs, você pode manipular o evento [IWMPEvents3:: CdromRipMediaError](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromripmediaerror) . Assim como **CdromRipStateChange**, esse evento fornece um ponteiro de interface **IWMPCdromRip** que representa a operação de cópia de CDs que gerou o evento. O evento também fornece um ponteiro **IDispatch** que representa o item de mídia que disparou o evento. Você pode chamar **QueryInterface** por meio desse ponteiro para recuperar um ponteiro **IWMPMedia** .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre o modelo de objeto do Player**](about-the-player-object-model.md)
</dt> </dl>

 

 




