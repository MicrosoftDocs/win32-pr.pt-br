---
title: Constantes Direct2D
description: Direct2D define a lista de constantes a seguir.
ms.assetid: 98a443af-4bb7-486d-bc87-ff34c3671bdd
topic_type:
- apiref
api_name:
- D2D1_APPEND_ALIGNED_ELEMENT
- D2D1_DEFAULT_FLATTENING_TOLERANCE
- D2D1_INVALID_PROPERTY_INDEX
- D2D1_INVALID_TAG
- D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL
api_location:
- d2d1.h
- d2d1effects_2.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 09/19/2019
ms.openlocfilehash: bc25bf1055b923a383fc580a622e96d787ed13e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753549"
---
# <a name="direct2d-constants"></a><span data-ttu-id="7c305-103">Constantes Direct2D</span><span class="sxs-lookup"><span data-stu-id="7c305-103">Direct2D constants</span></span>

<span data-ttu-id="7c305-104">As constantes a seguir são declaradas nos `d2d1effectauthor.h` arquivos de cabeçalho,, `d2d1.h` `d2d1_1.h` e `d2d1effects_2.h` .</span><span class="sxs-lookup"><span data-stu-id="7c305-104">The following constants are declared in the `d2d1effectauthor.h`, `d2d1.h`, `d2d1_1.h`, and `d2d1effects_2.h` header files.</span></span>

## <a name="d2d1_append_aligned_element--1"></a><span data-ttu-id="7c305-105">D2D1_APPEND_ALIGNED_ELEMENT (-1)</span><span class="sxs-lookup"><span data-stu-id="7c305-105">D2D1_APPEND_ALIGNED_ELEMENT (-1)</span></span>
<span data-ttu-id="7c305-106">Usado ao empacotar elementos de layout de entrada.</span><span class="sxs-lookup"><span data-stu-id="7c305-106">Used when packing input layout elements.</span></span> <span data-ttu-id="7c305-107">Ele indica que os elementos devem ser empacotados de forma contígua.</span><span class="sxs-lookup"><span data-stu-id="7c305-107">It indicates that the elements must be packed contiguously.</span></span>

## <a name="d2d1_default_flattening_tolerance-025f"></a><span data-ttu-id="7c305-108">D2D1_DEFAULT_FLATTENING_TOLERANCE (0,25 f)</span><span class="sxs-lookup"><span data-stu-id="7c305-108">D2D1_DEFAULT_FLATTENING_TOLERANCE (0.25f)</span></span>
<span data-ttu-id="7c305-109">A tolerância padrão para operações de mesclagem geométricas.</span><span class="sxs-lookup"><span data-stu-id="7c305-109">The default tolerance for geometric flattening operations.</span></span>

## <a name="d2d1_invalid_property_index-uint_max"></a><span data-ttu-id="7c305-110">D2D1_INVALID_PROPERTY_INDEX (UINT_MAX)</span><span class="sxs-lookup"><span data-stu-id="7c305-110">D2D1_INVALID_PROPERTY_INDEX (UINT_MAX)</span></span>
<span data-ttu-id="7c305-111">Define um índice de propriedade inválido.</span><span class="sxs-lookup"><span data-stu-id="7c305-111">Defines an invalid property index.</span></span>

<span data-ttu-id="7c305-112">Essa constante é retornada de [**ID2D1Properties:: GetPropertyIndex**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getpropertyindex) para indicar que a propriedade nomeada que você forneceu não tem um índice na interface de propriedade.</span><span class="sxs-lookup"><span data-stu-id="7c305-112">This constant is returned from [**ID2D1Properties::GetPropertyIndex**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getpropertyindex) to indicate that the named property that you provided doesn't have an index in the property interface.</span></span>

<span data-ttu-id="7c305-113">Se você passar essa constante para [**ID2D1Properties:: GetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getvalue(uint32_byte_uint32)) ou [**ID2D1Properties:: GetValueByName**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getvaluebyname(pcwstr_byte_uint32)), a chamada falhará e o buffer de saída será preenchido com zero.</span><span class="sxs-lookup"><span data-stu-id="7c305-113">If you pass this constant to [**ID2D1Properties::GetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getvalue(uint32_byte_uint32)) or [**ID2D1Properties::GetValueByName**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getvaluebyname(pcwstr_byte_uint32)), then the call fails, and the output buffer is zero-filled.</span></span>

## <a name="d2d1_invalid_tag-ulonglong_max"></a><span data-ttu-id="7c305-114">D2D1_INVALID_TAG (ULONGLONG_MAX)</span><span class="sxs-lookup"><span data-stu-id="7c305-114">D2D1_INVALID_TAG (ULONGLONG_MAX)</span></span>
<span data-ttu-id="7c305-115">Reservado Não use.</span><span class="sxs-lookup"><span data-stu-id="7c305-115">Reserved; don't use.</span></span>

## <a name="d2d1_scene_referred_sdr_white_level-800f"></a><span data-ttu-id="7c305-116">D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL (80.0 f)</span><span class="sxs-lookup"><span data-stu-id="7c305-116">D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL (80.0f)</span></span>
<span data-ttu-id="7c305-117">O número de nits que o espaço de cores sRGB ou scRGB usa para o SDR branco ou valores de ponto flutuante de 1,0 f.</span><span class="sxs-lookup"><span data-stu-id="7c305-117">The number of nits that sRGB or scRGB color space uses for SDR white, or floating point values of 1.0f.</span></span> <span data-ttu-id="7c305-118">Esse valor é constante somente quando o espaço de cores usa a luminância referida pela cena, que é verdadeira para conteúdo de intervalo dinâmico alto (HDR).</span><span class="sxs-lookup"><span data-stu-id="7c305-118">This value is constant only when the color space uses scene-referred luminance, which is true for high dynamic range (HDR) content.</span></span> <span data-ttu-id="7c305-119">Se o espaço de cores usar a luminância de exibição referenciada, o nível de branco do SDR deverá ser consultado a partir da exibição.</span><span class="sxs-lookup"><span data-stu-id="7c305-119">If the color space uses display-referred luminance instead, then the SDR white level should be queried from the display.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c305-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c305-120">Requirements</span></span>

| <span data-ttu-id="7c305-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c305-121">Requirement</span></span> | <span data-ttu-id="7c305-122">Valor</span><span class="sxs-lookup"><span data-stu-id="7c305-122">Value</span></span> |
|-|-|
| <span data-ttu-id="7c305-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7c305-123">Minimum supported client</span></span> | <span data-ttu-id="7c305-124">Windows 7, Windows Vista com SP2 e atualização de plataforma para aplicativos UWP do Windows Vista \[ Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="7c305-124">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span> |
| <span data-ttu-id="7c305-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7c305-125">Minimum supported server</span></span> | <span data-ttu-id="7c305-126">Windows Server 2008 R2, Windows Server 2008 com SP2 e atualização de plataforma para aplicativos de aplicativos de desktop do Windows Server 2008 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="7c305-126">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span> |
| <span data-ttu-id="7c305-127">Número mínimo de telefone com suporte</span><span class="sxs-lookup"><span data-stu-id="7c305-127">Minimum supported phone</span></span> | <span data-ttu-id="7c305-128">Windows Phone 8,1 \[ Windows Phone silverlight 8,1 e aplicativos \] de Windows Runtime, Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="7c305-128">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\], Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span> |
| <span data-ttu-id="7c305-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7c305-129">Header</span></span> | <span data-ttu-id="7c305-130">d2d1effectauthor. h, d2d1. h, d2d1_1. h, d2d1effects_2. h</span><span class="sxs-lookup"><span data-stu-id="7c305-130">d2d1effectauthor.h, d2d1.h, d2d1_1.h, d2d1effects_2.h</span></span> |
