---
description: um aplicativo navega em uma árvore de itens do dispositivo de aquisição de imagem Windows (WIA) para localizar e selecionar imagens no dispositivo. Usando essa técnica, um aplicativo seleciona e adquire uma imagem sem apresentar uma caixa de diálogo ao usuário.
ms.assetid: 1f124b4a-45fb-4181-b45a-e810a61ac37d
title: Navegando em uma árvore de itens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5a8ef11fc534a621c31461df897c8cc81f987ef83163a1300b0e392ce4f190e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119593016"
---
# <a name="navigating-an-item-tree"></a>Navegando em uma árvore de itens

um aplicativo navega em uma árvore de itens do dispositivo de aquisição de imagem Windows (WIA) para localizar e selecionar imagens no dispositivo. Usando essa técnica, um aplicativo seleciona e adquire uma imagem sem apresentar uma caixa de diálogo ao usuário.

Um dispositivo WIA é representado como o item raiz em uma árvore de objetos [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) ou [**IWiaItem2**](-wia-iwiaitem2.md) . Os itens filho na árvore representam imagens para uma câmera ou ambientes de verificação para um scanner.

Depois que um dispositivo WIA é selecionado, um aplicativo chama o método [**IWiaItem:: EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) da interface [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) ou [**IWiaItem2**](-wia-iwiaitem2.md) do dispositivo para enumerar os itens filho (imagens ou ambientes de verificação) do dispositivo. Para obter instruções, consulte [selecionando um dispositivo](-wia-selecting-a-device.md).

O método [**IWiaItem:: EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) cria um objeto de enumeração para os itens filho do dispositivo e retorna um ponteiro para a interface [**IEnumWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwiaitem) desse objeto. O aplicativo pode, então, usar os métodos da interface **IEnumWiaItem** para obter ponteiros para os itens na árvore de itens do dispositivo.

 

 



