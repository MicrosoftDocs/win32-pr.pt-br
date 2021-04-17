---
description: Salvando e restaurando objetos DvdState
ms.assetid: 65180fe2-0faf-47c0-bccd-728e01056c46
title: Salvando e restaurando objetos DvdState
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9640b20bc8d763054c15331017da343ef45f3c2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105757245"
---
# <a name="saving-and-restoring-dvdstate-objects"></a>Salvando e restaurando objetos DvdState

Os objetos [**IDvdState**](/windows/desktop/api/Strmif/nn-strmif-idvdstate) permitem que os aplicativos salvem um instantâneo da sessão do usuário, incluindo informações como o local atual no disco, o nível pai da pessoa que está exibindo, os fluxos de áudio e subimagem selecionados e assim por diante. Isso significa que os usuários podem salvar seu lugar em um disco DVD-Video e observá-lo em um momento posterior.

Os aplicativos não podem criar objetos DvdState. Esses objetos são criados internamente pelo navegador de DVD quando um aplicativo chama [**IDvdInfo2:: GetState**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getstate). Os objetos DvdState expõem a interface [**IDvdState**](/windows/desktop/api/Strmif/nn-strmif-idvdstate) para permitir que os aplicativos consultem determinadas informações.

No aplicativo de exemplo de DVD, as funções **CDvdCore:: RestoreBookmark** e **CDvdCore:: SaveBookmark** mostram como salvar e recuperar objetos DvdState.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aplicativos de DVD](dvd-applications.md)
</dt> </dl>

 

 



