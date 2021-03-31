---
title: Pontos de sincronização
description: Quando há suporte para conjuntos de propriedades no mesmo objeto que o IStorage, é importante estar ciente dos pontos de sincronização entre o armazenamento de base e o armazenamento de propriedades.
ms.assetid: 34cc4338-b29f-43f9-946d-14b2b235ccec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa156efbb1573b2954c1f7da07a58ed663c71781
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637257"
---
# <a name="synchronization-points"></a>Pontos de sincronização

Quando há suporte para conjuntos de propriedades no mesmo objeto que o [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), é importante estar ciente dos pontos de sincronização entre o armazenamento de base e o armazenamento de propriedades.

O armazenamento do conjunto de propriedades mantém o fluxo do conjunto de propriedades em um buffer interno até que o buffer seja confirmado por meio do método [**IPropertyStorage:: Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) . Isso é verdadeiro se [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) foi aberto no modo transacionado ou em modo direto.

 

 




