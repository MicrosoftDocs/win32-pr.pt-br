---
description: Os reconhecedores da Microsoft usam os GUIDs a seguir.
ms.assetid: dcf6bc5a-1b61-48f7-bc7a-f74ae6e2e57e
title: GUIDs de propriedade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b2eb089a9b3b5c7863f2d57d9a635b9ab042ae6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091810"
---
# <a name="property-guids"></a><span data-ttu-id="280c5-103">GUIDs de propriedade</span><span class="sxs-lookup"><span data-stu-id="280c5-103">Property GUIDs</span></span>

<span data-ttu-id="280c5-104">Os reconhecedores da Microsoft usam os GUIDs a seguir.</span><span class="sxs-lookup"><span data-stu-id="280c5-104">The Microsoft recognizers use the following GUIDs.</span></span> <span data-ttu-id="280c5-105">Sempre que possível, os aplicativos devem usar esses GUIDs.</span><span class="sxs-lookup"><span data-stu-id="280c5-105">Whenever possible, applications should use these GUIDs.</span></span> <span data-ttu-id="280c5-106">No entanto, é esperado e incentivado que outros reconhecedores usarão GUIDs adicionais para propriedades que não têm suporte dos reconhecedores da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="280c5-106">However, it is expected and encouraged that other recognizers will use additional GUIDs for properties that are not supported by the Microsoft recognizers.</span></span>

<span data-ttu-id="280c5-107">Todas as funções de propriedade foram desenvolvidas com a compreensão de que a lista de GUIDs pode ser estendida por outros reconhecedores.</span><span class="sxs-lookup"><span data-stu-id="280c5-107">All property functions have been developed with the understanding that the list of GUIDs may be extended by other recognizers.</span></span> <span data-ttu-id="280c5-108">Essas funções de propriedade incluem:</span><span class="sxs-lookup"><span data-stu-id="280c5-108">These property functions include:</span></span>

-   [<span data-ttu-id="280c5-109">**Função GetContextPropertyList**</span><span class="sxs-lookup"><span data-stu-id="280c5-109">**GetContextPropertyList Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-getcontextpropertylist)
-   [<span data-ttu-id="280c5-110">**Função GetContextPropertyValue**</span><span class="sxs-lookup"><span data-stu-id="280c5-110">**GetContextPropertyValue Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-getcontextpropertyvalue)
-   [<span data-ttu-id="280c5-111">**Função GetResultPropertyList**</span><span class="sxs-lookup"><span data-stu-id="280c5-111">**GetResultPropertyList Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-getresultpropertylist)
-   [<span data-ttu-id="280c5-112">**Função SetContextPropertyValue**</span><span class="sxs-lookup"><span data-stu-id="280c5-112">**SetContextPropertyValue Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-setcontextpropertyvalue)

<span data-ttu-id="280c5-113">A tabela a seguir lista os GUIDs de Propriedade do Tablet PC definidos em msinkaut. h (instalado em c: \\ arquivos de programas \\ Microsoft Tablet PC Platform SDK \\ incluem por padrão).</span><span class="sxs-lookup"><span data-stu-id="280c5-113">The following table lists Tablet PC property GUIDs defined in msinkaut.h (installed in c:\\Program Files\\Microsoft Tablet PC Platform SDK\\Include by default).</span></span>



| <span data-ttu-id="280c5-114">GUID</span><span class="sxs-lookup"><span data-stu-id="280c5-114">GUID</span></span>                                                  | <span data-ttu-id="280c5-115">Definição</span><span class="sxs-lookup"><span data-stu-id="280c5-115">Definition</span></span>                                                                                   |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="280c5-116">INKRECOGNITIONPROPERTY \_ BOXNUMBER</span><span class="sxs-lookup"><span data-stu-id="280c5-116">INKRECOGNITIONPROPERTY\_BOXNUMBER</span></span><br/>          | <span data-ttu-id="280c5-117">O índice da caixa alternativa do reconhecedor no modo de caixa</span><span class="sxs-lookup"><span data-stu-id="280c5-117">The recognizer alternate box index in box mode</span></span><br/>                                    |
| <span data-ttu-id="280c5-118">INKRECOGNITIONPROPERTY \_ LINENUMBER</span><span class="sxs-lookup"><span data-stu-id="280c5-118">INKRECOGNITIONPROPERTY\_LINENUMBER</span></span><br/>         | <span data-ttu-id="280c5-119">O número da linha</span><span class="sxs-lookup"><span data-stu-id="280c5-119">The line number</span></span><br/>                                                                   |
| <span data-ttu-id="280c5-120">\_segmentação INKRECOGNITIONPROPERTY</span><span class="sxs-lookup"><span data-stu-id="280c5-120">INKRECOGNITIONPROPERTY\_SEGMENTATION</span></span><br/>       | <span data-ttu-id="280c5-121">Como o reconhecedor segmenta palavras e caracteres</span><span class="sxs-lookup"><span data-stu-id="280c5-121">How the recognizer segments words and characters</span></span><br/>                                  |
| <span data-ttu-id="280c5-122">INKRECOGNITIONPROPERTY \_ HOTPOINT</span><span class="sxs-lookup"><span data-stu-id="280c5-122">INKRECOGNITIONPROPERTY\_HOTPOINT</span></span><br/>           | <span data-ttu-id="280c5-123">O ponto de acesso do gesto</span><span class="sxs-lookup"><span data-stu-id="280c5-123">The gesture hot point</span></span><br/>                                                             |
| <span data-ttu-id="280c5-124">INKRECOGNITIONPROPERTY \_ MAXIMUMSTROKECOUNT</span><span class="sxs-lookup"><span data-stu-id="280c5-124">INKRECOGNITIONPROPERTY\_MAXIMUMSTROKECOUNT</span></span><br/> | <span data-ttu-id="280c5-125">Número máximo de traços para um segmento</span><span class="sxs-lookup"><span data-stu-id="280c5-125">Maximum number of strokes for a segment</span></span><br/>                                           |
| <span data-ttu-id="280c5-126">INKRECOGNITIONPROPERTY \_ POINTSPERINCH</span><span class="sxs-lookup"><span data-stu-id="280c5-126">INKRECOGNITIONPROPERTY\_POINTSPERINCH</span></span><br/>      | <span data-ttu-id="280c5-127">A métrica de pontos por polegada</span><span class="sxs-lookup"><span data-stu-id="280c5-127">The points-per-inch metric</span></span><br/>                                                        |
| <span data-ttu-id="280c5-128">INKRECOGNITIONPROPERTY \_ CONFIDENCELEVEL</span><span class="sxs-lookup"><span data-stu-id="280c5-128">INKRECOGNITIONPROPERTY\_CONFIDENCELEVEL</span></span><br/>    | <span data-ttu-id="280c5-129">[**Confiança \_**](/windows/win32/api/rectypes/ne-rectypes-confidence_level) Enumeração de nível</span><span class="sxs-lookup"><span data-stu-id="280c5-129">[**CONFIDENCE\_LEVEL**](/windows/win32/api/rectypes/ne-rectypes-confidence_level) enumeration</span></span><br/>                         |
| <span data-ttu-id="280c5-130">INKRECOGNITIONPROPERTY \_ LINEMETRICS</span><span class="sxs-lookup"><span data-stu-id="280c5-130">INKRECOGNITIONPROPERTY\_LINEMETRICS</span></span><br/>        | <span data-ttu-id="280c5-131">Informações para computação de linha de base, Tabs no meio ou Both, que são usadas no malha</span><span class="sxs-lookup"><span data-stu-id="280c5-131">Information for computing baseline, midline, or both, that is used in the lattice</span></span><br/> |



 

 

 




