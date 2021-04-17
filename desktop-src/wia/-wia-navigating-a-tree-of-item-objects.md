---
description: 'Saiba mais sobre: navegando em uma árvore de objetos de item'
ms.assetid: e91f72c8-3ad6-49e8-88cc-aa99c13cd4c2
title: Navegando em uma árvore de objetos de item
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 04e87444c2b9c473268c5e97dd9c26d04d95b93b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105798070"
---
# <a name="navigating-a-tree-of-item-objects"></a>Navegando em uma árvore de objetos de item

> [!Note]  
> Este sistema de scripts foi substituído pela camada de automação da WIA (aquisição de imagem do Windows). Consulte [camada de automação de aquisição de imagem do Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).

 

Um aplicativo ou script navega por uma árvore de itens do dispositivo de aquisição de imagem do Windows (WIA) para localizar e selecionar imagens no dispositivo. Usando essa técnica, um aplicativo seleciona e adquire uma imagem sem o uso de uma caixa de diálogo.

Um dispositivo WIA é representado como o item raiz em uma árvore de objetos de [**Item**](-wia-item.md) . Os itens filho na árvore representam pastas e imagens para uma câmera ou ambientes de verificação para um scanner.

Depois de se conectar a um dispositivo, chame a propriedade [**Children**](-wia-iwiadispatchitem-children.md) do objeto [**Item**](-wia-item.md) que representa o dispositivo (o item raiz da árvore) para obter uma coleção dos itens filho (as imagens ou os ambientes de verificação) do dispositivo.

Enumere esta coleção (recursivamente, se necessário) para navegar na árvore de itens.

 

 
