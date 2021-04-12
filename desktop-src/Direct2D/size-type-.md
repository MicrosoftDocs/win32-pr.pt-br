---
title: Função de tipo de tamanho (D2d1helper. h)
description: Cria uma estrutura de tamanho que armazena sua largura e altura usando o tipo de dados especificado.
ms.assetid: 9f7e37a3-440e-40c0-a527-9fcbd207dce8
keywords:
- Função de tipo de tamanho Direct2D
topic_type:
- apiref
api_name:
- Size Type Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a300ab0ce7da57440516733459f703379cf5a943
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454993"
---
# <a name="sizetype-function"></a><span data-ttu-id="88e6d-104"><Type>Função size</span><span class="sxs-lookup"><span data-stu-id="88e6d-104">Size<Type> Function</span></span>

<span data-ttu-id="88e6d-105">Cria uma estrutura de tamanho que armazena sua largura e altura usando o tipo de dados especificado.</span><span class="sxs-lookup"><span data-stu-id="88e6d-105">Creates a size structure that stores its width and height using the specified data type.</span></span>

``` syntax
template<typename Type>
typename TypeTraits<Type>::Size Size(
  Type width,
  Type height
);
```

## <a name="template-parameters"></a><span data-ttu-id="88e6d-106">Parâmetros de modelo</span><span class="sxs-lookup"><span data-stu-id="88e6d-106">Template Parameters</span></span>



| <span data-ttu-id="88e6d-107">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="88e6d-107">Parameter</span></span> | <span data-ttu-id="88e6d-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="88e6d-108">Description</span></span>                                                                                         |
|-----------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88e6d-109">Type</span><span class="sxs-lookup"><span data-stu-id="88e6d-109">Type</span></span>      | <span data-ttu-id="88e6d-110">O tipo de dados usado para armazenar a largura e a altura do tamanho.</span><span class="sxs-lookup"><span data-stu-id="88e6d-110">The data type used to store the width and height of the size.</span></span> <span data-ttu-id="88e6d-111">Os valores possíveis são FLOAT e UINT32.</span><span class="sxs-lookup"><span data-stu-id="88e6d-111">Possible values are FLOAT and UINT32.</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="88e6d-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="88e6d-112">Parameters</span></span>



| <span data-ttu-id="88e6d-113">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="88e6d-113">Parameter</span></span> | <span data-ttu-id="88e6d-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="88e6d-114">Description</span></span>        |
|-----------|--------------------|
| <span data-ttu-id="88e6d-115">width</span><span class="sxs-lookup"><span data-stu-id="88e6d-115">width</span></span>     | <span data-ttu-id="88e6d-116">A largura do tamanho.</span><span class="sxs-lookup"><span data-stu-id="88e6d-116">The size's width.</span></span>  |
| <span data-ttu-id="88e6d-117">altura</span><span class="sxs-lookup"><span data-stu-id="88e6d-117">height</span></span>    | <span data-ttu-id="88e6d-118">A altura do tamanho.</span><span class="sxs-lookup"><span data-stu-id="88e6d-118">The size's height.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="88e6d-119">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="88e6d-119">Return Value</span></span>

<span data-ttu-id="88e6d-120">Um tamanho que contém a largura e a altura especificadas.</span><span class="sxs-lookup"><span data-stu-id="88e6d-120">A size that contains the specified width and height.</span></span>

## <a name="requirements"></a><span data-ttu-id="88e6d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88e6d-121">Requirements</span></span>



| <span data-ttu-id="88e6d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="88e6d-122">Requirement</span></span> | <span data-ttu-id="88e6d-123">Valor</span><span class="sxs-lookup"><span data-stu-id="88e6d-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88e6d-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="88e6d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="88e6d-125">Windows 7, Windows Vista com SP2 e atualização de plataforma para aplicativos UWP do Windows Vista \[ Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="88e6d-125">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="88e6d-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="88e6d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="88e6d-127">Windows Server 2008 R2, Windows Server 2008 com SP2 e atualização de plataforma para aplicativos de aplicativos de desktop do Windows Server 2008 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="88e6d-127">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="88e6d-128">Número mínimo de telefone com suporte</span><span class="sxs-lookup"><span data-stu-id="88e6d-128">Minimum supported phone</span></span><br/>  | <span data-ttu-id="88e6d-129">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="88e6d-129">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="88e6d-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="88e6d-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="88e6d-131"><dt>D2d1helper. h</dt></span><span class="sxs-lookup"><span data-stu-id="88e6d-131"><dt>D2d1helper.h</dt></span></span> </dl>                                                  |
| <span data-ttu-id="88e6d-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="88e6d-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="88e6d-133"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="88e6d-133"><dt>D2d1.lib</dt></span></span> </dl>                                                      |
| <span data-ttu-id="88e6d-134">DLL</span><span class="sxs-lookup"><span data-stu-id="88e6d-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88e6d-135"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88e6d-135"><dt>D2d1.dll</dt></span></span> </dl>                                                      |



 

 





