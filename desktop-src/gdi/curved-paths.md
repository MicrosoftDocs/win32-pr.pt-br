---
description: Caminhos curvos
ms.assetid: 1ee9e6c6-5f8d-4727-b5f9-4b179c5371f1
title: Caminhos curvos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fe27e20d7c5c3f59ea4bd38b46049088ae9d409
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827667"
---
# <a name="curved-paths"></a><span data-ttu-id="e8a31-103">Caminhos curvos</span><span class="sxs-lookup"><span data-stu-id="e8a31-103">Curved Paths</span></span>

<span data-ttu-id="e8a31-104">Um aplicativo pode mesclar as curvas em um caminho chamando a função [**FlattenPath**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath) .</span><span class="sxs-lookup"><span data-stu-id="e8a31-104">An application can flatten the curves in a path by calling the [**FlattenPath**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath) function.</span></span> <span data-ttu-id="e8a31-105">Essa função é especialmente útil para aplicativos que se ajustam ao texto na delimitação de um caminho que contém curvas.</span><span class="sxs-lookup"><span data-stu-id="e8a31-105">This function is especially useful for applications that fit text onto the contour of a path which contains curves.</span></span> <span data-ttu-id="e8a31-106">Para ajustar o texto, o aplicativo deve executar as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="e8a31-106">To fit the text, the application must perform the following steps:</span></span>

1.  <span data-ttu-id="e8a31-107">Crie o caminho onde o texto é exibido.</span><span class="sxs-lookup"><span data-stu-id="e8a31-107">Create the path where the text appears.</span></span>
2.  <span data-ttu-id="e8a31-108">Chame a função [**FlattenPath**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath) para converter as curvas em um caminho em segmentos de linha.</span><span class="sxs-lookup"><span data-stu-id="e8a31-108">Call the [**FlattenPath**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath) function to convert the curves in a path into line segments.</span></span>
3.  <span data-ttu-id="e8a31-109">Chame a função [**GetPath**](/windows/desktop/api/Wingdi/nf-wingdi-getpath) para recuperar esses segmentos de linha.</span><span class="sxs-lookup"><span data-stu-id="e8a31-109">Call the [**GetPath**](/windows/desktop/api/Wingdi/nf-wingdi-getpath) function to retrieve those line segments.</span></span>
4.  <span data-ttu-id="e8a31-110">Calcule o comprimento de cada linha e a largura de cada caractere na cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="e8a31-110">Calculate the length of each line and the width of each character in the string.</span></span>
5.  <span data-ttu-id="e8a31-111">Use dados de largura de linha e largura de caractere para posicionar cada caractere ao longo da curva.</span><span class="sxs-lookup"><span data-stu-id="e8a31-111">Use line-width and character-width data to position each character along the curve.</span></span>

 

 



