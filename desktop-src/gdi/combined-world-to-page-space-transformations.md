---
description: As cinco transformações de mundo para página podem ser combinadas em uma única matriz 3-por-3.
ms.assetid: d17ba826-8e8d-4121-8afd-0f256121b54c
title: Transformações de espaço de mundo para página combinadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b770ef614fe1538a528de640cacc5ad54b28c37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967695"
---
# <a name="combined-world-to-page-space-transformations"></a>Transformações de espaço de mundo para página combinadas

As cinco transformações de mundo para página podem ser combinadas em uma única matriz 3-por-3. A função [**CombineTransform**](/windows/desktop/api/Wingdi/nf-wingdi-combinetransform) pode ser usada para combinar duas transformações de espaço no mundo para página-espaço. As transformações combinadas podem ser usadas para alterar a saída associada a um determinado contexto de dispositivo (DC) chamando a função [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) e fornecendo os elementos para essa matriz. Quando um aplicativo chama **SetWorldTransform**, ele armazena os elementos da matriz 3-por-3 em uma estrutura [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) . Os membros dessa estrutura correspondem às duas primeiras colunas de uma matriz 3-por-3; a última coluna da matriz não é necessária porque seus valores são constantes.

Os elementos da matriz de transformação do mundo atual podem ser reativados chamando a função [**GetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-getworldtransform) e fornecendo um ponteiro para uma estrutura [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) .

 

 



