---
title: Pontos de sincronização
description: Quando há suporte para conjuntos de propriedades no mesmo objeto que o IStorage, é importante estar ciente dos pontos de sincronização entre o armazenamento de base e o armazenamento de propriedades.
ms.assetid: 34cc4338-b29f-43f9-946d-14b2b235ccec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf924458d81003e2cc211ff810ebb714399ac28e91189586491b584cff6a3390
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034876"
---
# <a name="synchronization-points"></a>Pontos de sincronização

Quando há suporte para conjuntos de propriedades no mesmo objeto que o [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), é importante estar ciente dos pontos de sincronização entre o armazenamento de base e o armazenamento de propriedades.

O armazenamento do conjunto de propriedades mantém o fluxo do conjunto de propriedades em um buffer interno até que o buffer seja confirmado por meio do método [**IPropertyStorage:: Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) . Isso é verdadeiro se [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) foi aberto no modo transacionado ou em modo direto.

 

 




