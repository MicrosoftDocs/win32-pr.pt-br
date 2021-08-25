---
title: Sobre a gravação de CD
description: Sobre a gravação de CD
ms.assetid: 1ecc73ed-c49d-4190-baa9-93162f075a4c
keywords:
- Windows Media Player, gravação de CD
- Windows Media Player modelo de objeto, gravação de CD
- modelo de objeto, gravação de CD
- Windows Media Player ActiveX controle, gravação de CD
- ActiveX controle, gravação de CD
- Windows Media Player Controle de ActiveX móvel, gravação de CD
- Windows Media Player Móvel, gravação de CD
- Gravação de CD, sobre
- CDs de gravação, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c784765a09b601da2f0ec75434a37f55a75ff7e6ab6d737f7912daab8f197c07
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957136"
---
# <a name="about-cd-burning"></a>Sobre a gravação de CD

O SDK Windows Media Player 11 apresenta uma nova funcionalidade para a criação de CDs. Esse processo é chamado *de gravação.*

Para enumerar as unidades de CD no computador do usuário, use a interface **IWMPCdromCollection.** Você recupera um ponteiro para essa interface chamando [IWMPCore::get \_ cdromCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection). Usando os métodos **count** e **item,** você pode iterar a coleção para recuperar um ponteiro de interface **IWMPCdrom** para cada unidade de CD no computador do usuário. A **interface IWMPCdrom** representa uma unidade de CD individual.

Antes de começar a gravar um CD, primeiro você deve chamar **QueryInterface** por meio de um ponteiro **IWMPCdrom** para recuperar um ponteiro para a interface **IWMPCdromFace.** Usando o **método isAvailable,** você pode determinar se uma unidade de CD específica pode gravar CDs, se há um CD na unidade e como o CD pode ser usado.

Para especificar os itens a gravar em CD, você deve criar uma playlist. Windows Media Player representa listas de reprodução usando a interface **IWMPPlaylist.** Você pode criar essa playlist da maneira que quiser. Por exemplo, você pode simplesmente recuperar uma playlist da biblioteca chamando [IWMPMediaCollection::getByAlbum](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection-getbyalbum). Depois de criar a playlist que deseja gravar em CD, você deve chamar o método [IWMPCdromPlay::p ut \_ burnPlaylist](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_burnplaylist) e passar o ponteiro da playlist como um argumento. Isso define sua playlist como aquela que Windows Media Player copiará para o CD.

Se você recuperar uma playlist da biblioteca, as alterações feitas na playlist serão refletidas na biblioteca do usuário. Para evitar isso, chame [IWMPPlaylist::setItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-setiteminfo), passando o nome do atributo "Temporário" e o valor "true". Isso converte sua instância de playlist em uma playlist temporária, que pode ser editada sem alterar a playlist original.

Sempre que você definir uma nova playlist para gravação ou fazer alterações em uma playlist de gravação existente, deverá chamar [IWMPCdrom Playlist::refreshStatus](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-refreshstatus) para atualizar as informações de status. Isso garante que Windows Media Player o processamento necessário para fornecer informações de status precisas para a operação de gravação de CD.

Para especificar o tipo de CD a ser gravar, chame [IWMPCdrom Ltd::p ut \_ burnFormat.](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_burnformat) Windows Media Player permite gravar dois tipos de CDs: CDs de áudio e CDs de dados. A [enumeração WMP Ltdaformat](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnformat) define os tipos de CD.

Você pode especificar um rótulo de volume para o CD chamando [IWMPCdrom \_ Ltd::p ut.](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_label)

Quando estiver pronto para começar a gravar o CD, chame [IWMPCdrom Ltd::startEar.](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-startburn) Você pode monitorar o progresso da operação de redução chamando periodicamente [IWMPCdrom Ltd::get \_ burnProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnprogress). Esse método recupera um valor de progresso para toda a operação de gravação. O valor recuperado é um número que representa a porcentagem de gravação concluída. Você pode monitorar o estado da operação de gravação manipulando o evento [IWMPEvents3::CdromStateChange,](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromburnstatechange) que usa a enumeração [WMPState](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate) para indicar o estado atual. Você deve ter cuidado para comparar o ponteiro **IWMPCdrom Ltda** (fornecido pelo evento) com o ponteiro que representa a operação de gravação para garantir que o evento tenha sido gerado pela operação. Você pode interromper a operação de gravação chamando [IWMPCdrom Ltd::stopEar.](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-stopburn)

Há dois eventos que você pode manipular para receber notificações de erro sobre sua operação de gravação. O [evento IWMPEvents3::CdromError](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromburnerror) é gerado quando ocorre um erro genérico. [IWMPEvents3::CdromErrorMedia é](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromburnmediaerror) gerado quando um item de mídia específico causa um erro durante a gravação. Como o **evento CdromStateChange,** cada um desses eventos fornece um ponteiro **IWMPCdromChang** que representa a operação de gravação que gerou o evento. O **evento CdromErrorMediaError** fornece um **ponteiro IDispatch** que representa o item de mídia que gerou o evento. Você pode chamar **QueryInterface por** meio desse ponteiro para recuperar um **ponteiro IWMPMedia.**

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre o modelo de objeto do player**](about-the-player-object-model.md)
</dt> <dt>

[**IWMPCdrom Interface**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom)
</dt> <dt>

[**Interface IWMPCdrom Ltda**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn)
</dt> <dt>

[**IWMPCdromCollection Interface**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)
</dt> <dt>

[**IWMPEvents3 Interface**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents3)
</dt> <dt>

[**IWMPMedia Interface**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)
</dt> <dt>

[**IWMPPlaylist Interface**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist)
</dt> <dt>

[**Atributo temporário**](temporary-attribute.md)
</dt> </dl>

 

 




