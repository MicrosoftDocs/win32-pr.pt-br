---
title: Efeito de tonalidade
description: Esse efeito dicolori a imagem de origem multiplicando a imagem de origem pela cor especificada. Ele tem uma única entrada.
ms.assetid: b0fd3598-26b6-faee-4f10-ebba96241bc8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f12e7593f9cb0695a6adb7b955fb66b13c8d00b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918378"
---
# <a name="tint-effect"></a><span data-ttu-id="438de-104">Efeito de tonalidade</span><span class="sxs-lookup"><span data-stu-id="438de-104">Tint effect</span></span>

<span data-ttu-id="438de-105">Esse efeito dicolori a imagem de origem multiplicando a imagem de origem pela cor especificada.</span><span class="sxs-lookup"><span data-stu-id="438de-105">This effect tints the source image by multiplying the source image by the specified color.</span></span> <span data-ttu-id="438de-106">Ele tem uma única entrada.</span><span class="sxs-lookup"><span data-stu-id="438de-106">It has a single input.</span></span>

<span data-ttu-id="438de-107">O CLSID para esse efeito é CLSID \_ D2D1Tint.</span><span class="sxs-lookup"><span data-stu-id="438de-107">The CLSID for this effect is CLSID\_D2D1Tint.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="438de-108">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="438de-108">Effect properties</span></span>



| <span data-ttu-id="438de-109">Nome de exibição e enumeração de índice</span><span class="sxs-lookup"><span data-stu-id="438de-109">Display name and index enumeration</span></span>                    | <span data-ttu-id="438de-110">Tipo e valor padrão</span><span class="sxs-lookup"><span data-stu-id="438de-110">Type and default value</span></span>                              | <span data-ttu-id="438de-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="438de-111">Description</span></span>                                                      |
|-------------------------------------------------------|-----------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="438de-112">Cor de prop ColorD2D1 de \_ tonalidade \_ \_</span><span class="sxs-lookup"><span data-stu-id="438de-112">ColorD2D1\_TINT\_PROP\_COLOR</span></span><br/>               | <span data-ttu-id="438de-113">\_ \_ 4F de vetor d2d1 (1,0 f, 1,0 f, 1,0 f, 1,0 f)</span><span class="sxs-lookup"><span data-stu-id="438de-113">D2D1\_VECTOR\_4F(1.0f, 1.0f, 1.0f, 1.0f)</span></span><br/> | <span data-ttu-id="438de-114">As cores da imagem de origem são multiplicadas por esse valor.</span><span class="sxs-lookup"><span data-stu-id="438de-114">Colors from the source image are multiplied by this value.</span></span>       |
| <span data-ttu-id="438de-115">\_Saída de \_ \_ fixe \_ de diClampOutputD2D1 de tonalidade</span><span class="sxs-lookup"><span data-stu-id="438de-115">ClampOutputD2D1\_TINT\_PROP\_CLAMP\_OUTPUT</span></span><br/> | <span data-ttu-id="438de-116">BOOLFALSE</span><span class="sxs-lookup"><span data-stu-id="438de-116">BOOLFALSE</span></span><br/>                                | <span data-ttu-id="438de-117">Se deseja ou não fixe os valores de saída para o intervalo de \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="438de-117">Whether or not to clamp the output values to the range \[0, 1\].</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="438de-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="438de-118">Requirements</span></span>



| <span data-ttu-id="438de-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="438de-119">Requirement</span></span> | <span data-ttu-id="438de-120">Valor</span><span class="sxs-lookup"><span data-stu-id="438de-120">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="438de-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="438de-121">Minimum supported client</span></span> | <span data-ttu-id="438de-122">Aplicativos do Windows 10 \[ Desktop aplicativos da \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="438de-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="438de-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="438de-123">Minimum supported server</span></span> | <span data-ttu-id="438de-124">Aplicativos do Windows 10 \[ Desktop aplicativos da \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="438de-124">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="438de-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="438de-125">Header</span></span>                   | <span data-ttu-id="438de-126">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="438de-126">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="438de-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="438de-127">Library</span></span>                  | <span data-ttu-id="438de-128">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="438de-128">d2d1.lib, dxguid.lib</span></span>                              |



 ## <a name="related-topics"></a><span data-ttu-id="438de-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="438de-129">Related topics</span></span>

* [<span data-ttu-id="438de-130">Interface ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="438de-130">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
