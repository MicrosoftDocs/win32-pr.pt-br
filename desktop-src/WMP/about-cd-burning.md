---
title: Sobre a gravação de CD
description: Sobre a gravação de CD
ms.assetid: 1ecc73ed-c49d-4190-baa9-93162f075a4c
keywords:
- Windows Media Player, gravação de CD
- Modelo de objeto do Windows Media Player, gravação de CD
- modelo de objeto, gravação de CD
- Controle ActiveX do Windows Media Player, gravação de CD
- Controle ActiveX, gravação de CD
- Controle ActiveX móvel do Windows Media Player, gravação de CD
- Windows Media Player Mobile, gravação de CD
- Gravação de CD, sobre
- gravando CDs, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc921080d02bef6ffbf916fe4d7d1df09f1e8bbc
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/21/2020
ms.locfileid: "103640287"
---
# <a name="about-cd-burning"></a>Sobre a gravação de CD

O SDK do Windows Media Player 11 apresenta uma nova funcionalidade para a criação de CDs. Esse processo é chamado de *gravação*.

Para enumerar as unidades de CD no computador do usuário, use a interface **IWMPCdromCollection** . Você recupera um ponteiro para essa interface chamando [IWMPCore:: get \_ cdromCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection). Usando os métodos **Count** e **Item** , você pode iterar a coleção para recuperar um ponteiro de interface **IWMPCDROM** para cada unidade de CD no computador do usuário. A interface **IWMPCdrom** representa uma unidade de CD individual.

Antes de começar a gravar um CD, você deve primeiro chamar **QueryInterface** por meio de um ponteiro **IWMPCdrom** para recuperar um ponteiro para a interface **IWMPCdromBurn** . Usando o método **IsAvailable** , você pode determinar se uma unidade de CD específica pode gravar CDs, se há um CD na unidade e como o CD pode ser usado.

Para especificar os itens a serem gravados no CD, você deve criar uma lista de reprodução. O Windows Media Player representa as listas de reprodução usando a interface **IWMPPlaylist** . Você pode criar essa playlist da maneira que desejar. Por exemplo, você pode simplesmente recuperar uma lista de reprodução da biblioteca chamando [IWMPMediaCollection:: getByAlbum](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection-getbyalbum). Depois de criar a lista de reprodução que você deseja gravar no CD, você deve chamar o método [IWMPCdromBurn::p UT \_ burnPlaylist](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_burnplaylist) e passar o ponteiro da playlist como um argumento. Isso define sua lista de reprodução como aquela que o Windows Media Player copiará para o CD.

Se você recuperar uma lista de reprodução da biblioteca, as alterações feitas na playlist serão refletidas na biblioteca do usuário. Para evitar isso, chame [IWMPPlaylist:: setItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-setiteminfo), passando o nome do atributo "Temporary" e o valor "true". Isso converte a instância de playlist em uma playlist temporária, que pode ser editada sem alterar a playlist original.

Cada vez que você define uma nova lista de reprodução para gravação ou faz alterações em uma lista de reprodução de gravação existente, você deve chamar [IWMPCdromBurn:: refreshStatus](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-refreshstatus) para atualizar as informações de status. Isso garante que o Windows Media Player faça o processamento necessário para fornecer informações de status precisas para a operação de gravação de CD.

Para especificar o tipo de CD a ser gravado, chame [IWMPCdromBurn::p UT \_ burnFormat](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_burnformat). O Windows Media Player permite que você grave dois tipos de CDs: CDs de áudio e CDs de dados. A enumeração [WMPBurnFormat](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnformat) define os tipos de CD.

Você pode especificar um rótulo de volume para o CD chamando [IWMPCdromBurn::p UT \_ Label](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_label).

Quando você estiver pronto para começar a gravar o CD, chame [IWMPCdromBurn:: startBurn](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-startburn). Você pode monitorar o progresso da operação de gravação chamando periodicamente [IWMPCdromBurn:: get \_ burnProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnprogress). Esse método recupera um valor de progresso para toda a operação de gravação. O valor recuperado é um número que representa a porcentagem de gravação concluída. Você pode monitorar o estado da operação de gravação manipulando o evento [IWMPEvents3:: CdromBurnStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromburnstatechange) , que usa a enumeração [WMPBurnState](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate) para indicar o estado atual. Você deve ter cuidado para comparar o ponteiro **IWMPCdromBurn** (fornecido pelo evento) com o ponteiro que representa a operação de gravação para garantir que o evento foi gerado pela operação. Você pode interromper a operação de gravação chamando [IWMPCdromBurn:: stopBurn](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-stopburn).

Há dois eventos que você pode manipular para receber notificações de erro sobre a operação de gravação. O evento [IWMPEvents3:: CdromBurnError](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromburnerror) é gerado quando ocorre um erro genérico. [IWMPEvents3:: CdromBurnMediaError](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromburnmediaerror) é gerado quando um determinado item de mídia causa um erro durante a gravação. Como o evento **CdromBurnStateChange** , cada um desses eventos fornece um ponteiro **IWMPCdromBurn** que representa a operação de gravação que gerou o evento. O evento **CdromBurnMediaError** fornece um ponteiro **IDispatch** que representa o item de mídia que disparou o evento. Você pode chamar **QueryInterface** por meio desse ponteiro para recuperar um ponteiro **IWMPMedia** .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre o modelo de objeto do Player**](about-the-player-object-model.md)
</dt> <dt>

[**Interface IWMPCdrom**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom)
</dt> <dt>

[**Interface IWMPCdromBurn**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn)
</dt> <dt>

[**Interface IWMPCdromCollection**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)
</dt> <dt>

[**Interface IWMPEvents3**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents3)
</dt> <dt>

[**Interface IWMPMedia**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)
</dt> <dt>

[**Interface IWMPPlaylist**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist)
</dt> <dt>

[**Atributo temporário**](temporary-attribute.md)
</dt> </dl>

 

 




