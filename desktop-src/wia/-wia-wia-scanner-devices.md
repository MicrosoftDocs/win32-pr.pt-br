---
description: O Windows de varredura WIA (Aquisição de Imagem) é implementado como uma árvore hierárquica de objetos IWiaItem.
ms.assetid: d716faec-9ace-422d-b6eb-ad4d86c1b0fd
title: Dispositivos de scanner WIA no WIA 1.0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd22cc9fe330a3acf231034b61c72178f3b282cb9e66a1f455d4b6939a1c3cde
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592658"
---
# <a name="wia-scanner-devices-in-wia-10"></a>Dispositivos de scanner WIA no WIA 1.0

> [!Note]  
> Este tópico discute a árvore de dispositivos do scanner para aplicativos que usam o serviço WIA (Aquisição de Imagem) 1.0 do Windows (que tem suporte no Windows XP ou anterior). Para obter informações sobre a árvore de dispositivos de itens wia (aquisição de imagem) 2.0 do Windows (que têm suporte no Windows Vista ou posterior), consulte Sobre a árvore de itens [IWiaItem2](-wia-about-item-tree.md).

 

O Windows do scanner wia (aquisição de imagem) é implementado como uma árvore hierárquica de [**objetos IWiaItem.**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) No item raiz, um aplicativo pode:

-   Funcionalidades do scanner de consultas
-   Definir propriedades do dispositivo do scanner
-   Controlar o feeder de documentos

Um dispositivo de scanner WIA é diferente de um dispositivo de câmera WIA porque, em geral, ele não armazena várias imagens na memória.

Sob o item raiz, um objeto de scanner típico tem um único objeto [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) que representa a funcionalidade de coleta de dados do dispositivo, o Item de Verificação. Esse item tem o [**sinalizador WiaItemTypeFile**](-wia-wia-item-type-flags.md) definido para indicar que as transferências de dados nesse item são possíveis. Um aplicativo configura uma verificação definindo as propriedades do item de verificação e, em seguida, executa a verificação e transfere os dados usando uma interface de transferência de dados.

O diagrama a seguir ilustra a implementação do WIA para um scanner típico:

![implementação wia de um scanner típico](images/wiscantr.gif)

Um scanner duplex típico é representado no WIA por ter um [**objeto IWiaItem.**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) Os dados de front-and-back-page são acessados sequencialmente uma transferência de dados por página. Portanto, a representação de um scanner duplex é idêntica à representação de um scanner típico.

Um verificador de slides capaz de examinar vários slides em uma única operação de verificação representa cada imagem separada como um [**objeto IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) separado.

O diagrama a seguir ilustra a representação WIA de um scanner de slides:

![scanner de slides](images/wislscan.gif)

 

 



