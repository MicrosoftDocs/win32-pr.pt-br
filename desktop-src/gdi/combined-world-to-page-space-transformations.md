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
# <a name="combined-world-to-page-space-transformations"></a><span data-ttu-id="3a4be-103">Transformações de espaço de mundo para página combinadas</span><span class="sxs-lookup"><span data-stu-id="3a4be-103">Combined World-to-Page Space Transformations</span></span>

<span data-ttu-id="3a4be-104">As cinco transformações de mundo para página podem ser combinadas em uma única matriz 3-por-3.</span><span class="sxs-lookup"><span data-stu-id="3a4be-104">The five world-to-page transformations can be combined into a single 3-by-3 matrix.</span></span> <span data-ttu-id="3a4be-105">A função [**CombineTransform**](/windows/desktop/api/Wingdi/nf-wingdi-combinetransform) pode ser usada para combinar duas transformações de espaço no mundo para página-espaço.</span><span class="sxs-lookup"><span data-stu-id="3a4be-105">The [**CombineTransform**](/windows/desktop/api/Wingdi/nf-wingdi-combinetransform) function can be used to combine two world-space to page-space transformations.</span></span> <span data-ttu-id="3a4be-106">As transformações combinadas podem ser usadas para alterar a saída associada a um determinado contexto de dispositivo (DC) chamando a função [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) e fornecendo os elementos para essa matriz.</span><span class="sxs-lookup"><span data-stu-id="3a4be-106">The combined transformations can be used to alter output associated with a particular device context (DC) by calling the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) function and supplying the elements for this matrix.</span></span> <span data-ttu-id="3a4be-107">Quando um aplicativo chama **SetWorldTransform**, ele armazena os elementos da matriz 3-por-3 em uma estrutura [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) .</span><span class="sxs-lookup"><span data-stu-id="3a4be-107">When an application calls **SetWorldTransform**, it stores the elements of the 3-by-3 matrix in an [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) structure.</span></span> <span data-ttu-id="3a4be-108">Os membros dessa estrutura correspondem às duas primeiras colunas de uma matriz 3-por-3; a última coluna da matriz não é necessária porque seus valores são constantes.</span><span class="sxs-lookup"><span data-stu-id="3a4be-108">The members of this structure correspond to the first two columns of a 3-by-3 matrix; the last column of the matrix is not required because its values are constant.</span></span>

<span data-ttu-id="3a4be-109">Os elementos da matriz de transformação do mundo atual podem ser reativados chamando a função [**GetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-getworldtransform) e fornecendo um ponteiro para uma estrutura [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) .</span><span class="sxs-lookup"><span data-stu-id="3a4be-109">The elements of the current world transformation matrix can be revived by calling the [**GetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-getworldtransform) function and supplying a pointer to an [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) structure.</span></span>

 

 



