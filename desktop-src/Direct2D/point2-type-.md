---
title: Função de tipo Point2 (D2d1helper. h)
description: Cria um ponto que armazena suas coordenadas usando o tipo de dados especificado.
ms.assetid: 59a631ae-d70e-4ee2-9546-2d19da40aa9b
keywords:
- Função de tipo point2 Direct2D
topic_type:
- apiref
api_name:
- Point2 Type Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f614f49077ed198c5e85d17b9ee3c84a5e300670
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105751289"
---
# <a name="point2type-function"></a><span data-ttu-id="84c69-104"><Type>Função point2</span><span class="sxs-lookup"><span data-stu-id="84c69-104">Point2<Type> Function</span></span>

<span data-ttu-id="84c69-105">Cria um ponto que armazena suas coordenadas usando o tipo de dados especificado.</span><span class="sxs-lookup"><span data-stu-id="84c69-105">Creates a point that stores its coordinates using the specified data type.</span></span>

``` syntax
template<typename Type>
typename TypeTraits<Type>::Point Point2(
  Type x,
  Type y
);
```

## <a name="template-parameters"></a><span data-ttu-id="84c69-106">Parâmetros de modelo</span><span class="sxs-lookup"><span data-stu-id="84c69-106">Template Parameters</span></span>



| <span data-ttu-id="84c69-107">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="84c69-107">Parameter</span></span> | <span data-ttu-id="84c69-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="84c69-108">Description</span></span>                                                                                                       |
|-----------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84c69-109">Type</span><span class="sxs-lookup"><span data-stu-id="84c69-109">Type</span></span>      | <span data-ttu-id="84c69-110">O tipo de dados usado para armazenar a coordenada x e a coordenada y do ponto.</span><span class="sxs-lookup"><span data-stu-id="84c69-110">The data type used to store the x-coordinate and y-coordinate of the point.</span></span> <span data-ttu-id="84c69-111">Os valores possíveis são FLOAT e UINT32.</span><span class="sxs-lookup"><span data-stu-id="84c69-111">Possible values are FLOAT and UINT32.</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="84c69-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="84c69-112">Parameters</span></span>



| <span data-ttu-id="84c69-113">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="84c69-113">Parameter</span></span> | <span data-ttu-id="84c69-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="84c69-114">Description</span></span>                    |
|-----------|--------------------------------|
| <span data-ttu-id="84c69-115">x</span><span class="sxs-lookup"><span data-stu-id="84c69-115">x</span></span>         | <span data-ttu-id="84c69-116">A coordenada X do ponto.</span><span class="sxs-lookup"><span data-stu-id="84c69-116">The x-coordinate of the point.</span></span> |
| <span data-ttu-id="84c69-117">a</span><span class="sxs-lookup"><span data-stu-id="84c69-117">y</span></span>         | <span data-ttu-id="84c69-118">A coordenada Y do ponto.</span><span class="sxs-lookup"><span data-stu-id="84c69-118">The y-coordinate of the point.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="84c69-119">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="84c69-119">Return Value</span></span>

<span data-ttu-id="84c69-120">Um ponto que contém a coordenada x e a coordenada y especificados.</span><span class="sxs-lookup"><span data-stu-id="84c69-120">A point that contains the specified x-coordinate and y-coordinate.</span></span>

## <a name="requirements"></a><span data-ttu-id="84c69-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84c69-121">Requirements</span></span>



| <span data-ttu-id="84c69-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="84c69-122">Requirement</span></span> | <span data-ttu-id="84c69-123">Valor</span><span class="sxs-lookup"><span data-stu-id="84c69-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84c69-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="84c69-124">Minimum supported client</span></span><br/> | <span data-ttu-id="84c69-125">Windows 7, Windows Vista com SP2 e atualização de plataforma para aplicativos UWP do Windows Vista \[ Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="84c69-125">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="84c69-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="84c69-126">Minimum supported server</span></span><br/> | <span data-ttu-id="84c69-127">Windows Server 2008 R2, Windows Server 2008 com SP2 e atualização de plataforma para aplicativos de aplicativos de desktop do Windows Server 2008 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="84c69-127">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="84c69-128">Número mínimo de telefone com suporte</span><span class="sxs-lookup"><span data-stu-id="84c69-128">Minimum supported phone</span></span><br/>  | <span data-ttu-id="84c69-129">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="84c69-129">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="84c69-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="84c69-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="84c69-131"><dt>D2d1helper. h</dt></span><span class="sxs-lookup"><span data-stu-id="84c69-131"><dt>D2d1helper.h</dt></span></span> </dl>                                                  |
| <span data-ttu-id="84c69-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="84c69-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="84c69-133"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="84c69-133"><dt>D2d1.lib</dt></span></span> </dl>                                                      |
| <span data-ttu-id="84c69-134">DLL</span><span class="sxs-lookup"><span data-stu-id="84c69-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84c69-135"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84c69-135"><dt>D2d1.dll</dt></span></span> </dl>                                                      |



 

 





