---
title: Função Rect Type (D2d1helper. h)
description: Cria uma estrutura de retângulo que armazena suas coordenadas usando o tipo de dados especificado.
ms.assetid: b152efaf-0779-4024-b998-82a347abba71
keywords:
- Função de tipo Rect Direct2D
topic_type:
- apiref
api_name:
- Rect Type Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2ed16ecd5a79c73ecb7341b9aa7f3378854dd4e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105749863"
---
# <a name="recttype-function"></a><span data-ttu-id="99cd1-104"><Type>Função Rect</span><span class="sxs-lookup"><span data-stu-id="99cd1-104">Rect<Type> Function</span></span>

<span data-ttu-id="99cd1-105">Cria uma estrutura de retângulo que armazena suas coordenadas usando o tipo de dados especificado.</span><span class="sxs-lookup"><span data-stu-id="99cd1-105">Creates a rectangle structure that stores its coordinates using the specified data type.</span></span>

``` syntax
template<typename Type>
typename TypeTraits<Type>::Rect Rect(
  Type left,
  Type top,
  Type right,
  Type bottom
);
```

## <a name="template-parameters"></a><span data-ttu-id="99cd1-106">Parâmetros de modelo</span><span class="sxs-lookup"><span data-stu-id="99cd1-106">Template Parameters</span></span>



| <span data-ttu-id="99cd1-107">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="99cd1-107">Parameter</span></span> | <span data-ttu-id="99cd1-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="99cd1-108">Description</span></span>                                                                                                |
|-----------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99cd1-109">Type</span><span class="sxs-lookup"><span data-stu-id="99cd1-109">Type</span></span>      | <span data-ttu-id="99cd1-110">O tipo de dados usado para armazenar as dimensões do retângulo.</span><span class="sxs-lookup"><span data-stu-id="99cd1-110">The data type used to store the dimensions of the rectangle.</span></span> <span data-ttu-id="99cd1-111">Os valores possíveis são **float** e **UINT32**.</span><span class="sxs-lookup"><span data-stu-id="99cd1-111">Possible values are **FLOAT** and **UINT32**.</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="99cd1-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="99cd1-112">Parameters</span></span>



| <span data-ttu-id="99cd1-113">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="99cd1-113">Parameter</span></span> | <span data-ttu-id="99cd1-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="99cd1-114">Description</span></span>                                             |
|-----------|---------------------------------------------------------|
| <span data-ttu-id="99cd1-115">esquerda</span><span class="sxs-lookup"><span data-stu-id="99cd1-115">left</span></span>      | <span data-ttu-id="99cd1-116">A coordenada x do canto superior esquerdo do retângulo.</span><span class="sxs-lookup"><span data-stu-id="99cd1-116">The x-coordinate of the rectangle's upper-left corner.</span></span>  |
| <span data-ttu-id="99cd1-117">top</span><span class="sxs-lookup"><span data-stu-id="99cd1-117">top</span></span>       | <span data-ttu-id="99cd1-118">A coordenada y do canto superior esquerdo do retângulo.</span><span class="sxs-lookup"><span data-stu-id="99cd1-118">The y-coordinate of the rectangle's upper-left corner.</span></span>  |
| <span data-ttu-id="99cd1-119">direita</span><span class="sxs-lookup"><span data-stu-id="99cd1-119">right</span></span>     | <span data-ttu-id="99cd1-120">A coordenada x do canto inferior direito do retângulo.</span><span class="sxs-lookup"><span data-stu-id="99cd1-120">The x-coordinate of the rectangle's lower-right corner.</span></span> |
| <span data-ttu-id="99cd1-121">parte inferior</span><span class="sxs-lookup"><span data-stu-id="99cd1-121">bottom</span></span>    | <span data-ttu-id="99cd1-122">A coordenada y do canto inferior direito do retângulo.</span><span class="sxs-lookup"><span data-stu-id="99cd1-122">The y-coordinate of the rectangle's lower-right corner.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="99cd1-123">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="99cd1-123">Return Value</span></span>

<span data-ttu-id="99cd1-124">Uma estrutura de retângulo que contém as coordenadas especificadas.</span><span class="sxs-lookup"><span data-stu-id="99cd1-124">A rectangle structure that contains the specified coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="99cd1-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99cd1-125">Requirements</span></span>



| <span data-ttu-id="99cd1-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="99cd1-126">Requirement</span></span> | <span data-ttu-id="99cd1-127">Valor</span><span class="sxs-lookup"><span data-stu-id="99cd1-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99cd1-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="99cd1-128">Minimum supported client</span></span><br/> | <span data-ttu-id="99cd1-129">Windows 7, Windows Vista com SP2 e atualização de plataforma para aplicativos UWP do Windows Vista \[ Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="99cd1-129">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="99cd1-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="99cd1-130">Minimum supported server</span></span><br/> | <span data-ttu-id="99cd1-131">Windows Server 2008 R2, Windows Server 2008 com SP2 e atualização de plataforma para aplicativos de aplicativos de desktop do Windows Server 2008 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="99cd1-131">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="99cd1-132">Número mínimo de telefone com suporte</span><span class="sxs-lookup"><span data-stu-id="99cd1-132">Minimum supported phone</span></span><br/>  | <span data-ttu-id="99cd1-133">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="99cd1-133">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="99cd1-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="99cd1-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="99cd1-135"><dt>D2d1helper. h</dt></span><span class="sxs-lookup"><span data-stu-id="99cd1-135"><dt>D2d1helper.h</dt></span></span> </dl>                                                  |
| <span data-ttu-id="99cd1-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="99cd1-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="99cd1-137"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="99cd1-137"><dt>D2d1.lib</dt></span></span> </dl>                                                      |
| <span data-ttu-id="99cd1-138">DLL</span><span class="sxs-lookup"><span data-stu-id="99cd1-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99cd1-139"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99cd1-139"><dt>D2d1.dll</dt></span></span> </dl>                                                      |



 

 





