---
description: Um aplicativo navega pela árvore de itens do dispositivo de aquisição de imagens do Windows (WIA) para localizar e selecionar imagens no dispositivo. Usando essa técnica, um aplicativo seleciona e adquire uma imagem sem apresentar uma caixa de diálogo ao usuário.
ms.assetid: 1f124b4a-45fb-4181-b45a-e810a61ac37d
title: Navegando em uma árvore de itens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 787ff3b53690ae7db4ff69fd5de2f4f4186f8e43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501782"
---
# <a name="navigating-an-item-tree"></a>Navegando em uma árvore de itens

Um aplicativo navega pela árvore de itens do dispositivo de aquisição de imagens do Windows (WIA) para localizar e selecionar imagens no dispositivo. Usando essa técnica, um aplicativo seleciona e adquire uma imagem sem apresentar uma caixa de diálogo ao usuário.

Um dispositivo WIA é representado como o item raiz em uma árvore de objetos [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) ou [**IWiaItem2**](-wia-iwiaitem2.md) . Os itens filho na árvore representam imagens para uma câmera ou ambientes de verificação para um scanner.

Depois que um dispositivo WIA é selecionado, um aplicativo chama o método [**IWiaItem:: EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) da interface [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) ou [**IWiaItem2**](-wia-iwiaitem2.md) do dispositivo para enumerar os itens filho (imagens ou ambientes de verificação) do dispositivo. Para obter instruções, consulte [selecionando um dispositivo](-wia-selecting-a-device.md).

O método [**IWiaItem:: EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) cria um objeto de enumeração para os itens filho do dispositivo e retorna um ponteiro para a interface [**IEnumWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwiaitem) desse objeto. O aplicativo pode, então, usar os métodos da interface **IEnumWiaItem** para obter ponteiros para os itens na árvore de itens do dispositivo.

 

 



