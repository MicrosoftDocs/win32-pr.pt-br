---
description: Salvando e restaurando objetos DvdState
ms.assetid: 65180fe2-0faf-47c0-bccd-728e01056c46
title: Salvando e restaurando objetos DvdState
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 922851cce72f736364c1f1e66b24032586221ad9cb75494c7286fe962eb34403
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982566"
---
# <a name="saving-and-restoring-dvdstate-objects"></a>Salvando e restaurando objetos DvdState

Os objetos [**IDvdState**](/windows/desktop/api/Strmif/nn-strmif-idvdstate) permitem que os aplicativos salvem um instantâneo da sessão do usuário, incluindo informações como o local atual no disco, o nível dos pais da pessoa que está exibindo, os fluxos de áudio e subspícone selecionados e assim por diante. Isso significa que os usuários podem salvar seu lugar em um DVD-Video e assistir a ele posteriormente.

Os aplicativos não podem criar objetos DvdState. Esses objetos são criados internamente pelo Navegador de DVD quando um aplicativo chama [**IDvdInfo2::GetState**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getstate). Os objetos DvdState expõem a interface [**IDvdState**](/windows/desktop/api/Strmif/nn-strmif-idvdstate) para permitir que os aplicativos consultem determinadas informações.

No aplicativo de exemplo de DVD, as funções **CDvdCore::RestoreBookmark** e **CDvdCore::SaveBookmark** mostram como salvar e recuperar objetos DvdState.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aplicativos de DVD](dvd-applications.md)
</dt> </dl>

 

 



