---
description: O dispositivo de scanner de aquisição de imagens do Windows (WIA) é implementado como uma árvore hierárquica de objetos IWiaItem.
ms.assetid: d716faec-9ace-422d-b6eb-ad4d86c1b0fd
title: Dispositivos do scanner WIA no WIA 1,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 443277b0b580a481b523739cd5bc21642d827252
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647214"
---
# <a name="wia-scanner-devices-in-wia-10"></a>Dispositivos do scanner WIA no WIA 1,0

> [!Note]  
> Este tópico discute a árvore de dispositivos do scanner para aplicativos que usam o serviço WIA (Windows Image Acquisition) 1,0 (que tem suporte no Windows XP ou anterior). Para obter informações sobre a árvore de dispositivos dos itens de aquisição de imagens do Windows (WIA) 2,0 (que têm suporte no Windows Vista ou posterior), consulte [sobre a árvore de itens do IWiaItem2](-wia-about-item-tree.md).

 

O dispositivo de scanner de aquisição de imagens do Windows (WIA) é implementado como uma árvore hierárquica de objetos [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) . A partir do item raiz, um aplicativo pode:

-   Recursos do verificador de consultas
-   Definir propriedades do dispositivo do scanner
-   Controlar o alimentador de documentos

Um dispositivo de scanner WIA é diferente de um dispositivo de câmera WIA porque, em geral, ele não armazena várias imagens na memória.

Sob o item raiz, um objeto de scanner típico tem um único objeto [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) que representa a funcionalidade de coleta de dados do dispositivo, o item de verificação. Este item tem o sinalizador [**WiaItemTypeFile**](-wia-wia-item-type-flags.md) definido para indicar que as transferências de dados neste item são possíveis. Um aplicativo configura uma verificação definindo as propriedades do item de verificação e, em seguida, executa a verificação e transfere os dados usando uma interface de transferência de dados.

O diagrama a seguir ilustra a implementação do WIA para um scanner típico:

![implementação de WIA de um scanner típico](images/wiscantr.gif)

Um scanner de duplex típico é representado em WIA por ter um objeto [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) . Os dados de página inicial e traseira são acessados sequencialmente uma transferência de dados por página. Portanto, a representação de um scanner duplex é idêntica à representação de um scanner típico.

Um scanner de slide capaz de digitalizar vários slides em uma única operação de verificação representa cada imagem separada como um objeto [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) separado.

O diagrama a seguir ilustra a representação WIA de um scanner de slide:

![scanner de slide](images/wislscan.gif)

 

 



