---
description: Objeto de processamento de dados usado pela interface ID3DX10ThreadPump para processar dados carregados de forma assíncrona.
ms.assetid: c932f558-10da-45fc-a833-8ed86fa065ab
title: Interface ID3DX10DataProcessor (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataProcessor
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: de573e50a1442396df78dd6a3c8f0bd09c1cbf6d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103837986"
---
# <a name="id3dx10dataprocessor-interface"></a><span data-ttu-id="0a7b3-103">Interface ID3DX10DataProcessor</span><span class="sxs-lookup"><span data-stu-id="0a7b3-103">ID3DX10DataProcessor interface</span></span>

<span data-ttu-id="0a7b3-104">Objeto de processamento de dados usado pela [**interface ID3DX10ThreadPump**](id3dx10threadpump.md) para processar dados carregados de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="0a7b3-104">Data processing object used by [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md) for processing loaded data asynchronously.</span></span>

## <a name="members"></a><span data-ttu-id="0a7b3-105">Membros</span><span class="sxs-lookup"><span data-stu-id="0a7b3-105">Members</span></span>

<span data-ttu-id="0a7b3-106">A interface **ID3DX10DataProcessor** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="0a7b3-106">The **ID3DX10DataProcessor** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="0a7b3-107">**ID3DX10DataProcessor** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="0a7b3-107">**ID3DX10DataProcessor** also has these types of members:</span></span>

-   [<span data-ttu-id="0a7b3-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="0a7b3-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0a7b3-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="0a7b3-109">Methods</span></span>

<span data-ttu-id="0a7b3-110">A interface **ID3DX10DataProcessor** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="0a7b3-110">The **ID3DX10DataProcessor** interface has these methods.</span></span>



| <span data-ttu-id="0a7b3-111">Método</span><span class="sxs-lookup"><span data-stu-id="0a7b3-111">Method</span></span>                                                                | <span data-ttu-id="0a7b3-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="0a7b3-112">Description</span></span>                                                                                                                         |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0a7b3-113">**Deviceobject**</span><span class="sxs-lookup"><span data-stu-id="0a7b3-113">**CreateDeviceObject**</span></span>](id3dx10dataprocessor-createdeviceobject.md) | <span data-ttu-id="0a7b3-114">Crie um objeto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0a7b3-114">Create a device object.</span></span><br/>                                                                                                  |
| [<span data-ttu-id="0a7b3-115">**Destruir**</span><span class="sxs-lookup"><span data-stu-id="0a7b3-115">**Destroy**</span></span>](id3dx10dataprocessor-destroy.md)                       | <span data-ttu-id="0a7b3-116">Usado por uma [**interface ID3DX10ThreadPump**](id3dx10threadpump.md) para destruir o processador após a conclusão de um item de trabalho.</span><span class="sxs-lookup"><span data-stu-id="0a7b3-116">Used by a [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md) to destroy the processor after a work item completes.</span></span><br/> |
| [<span data-ttu-id="0a7b3-117">**Processar**</span><span class="sxs-lookup"><span data-stu-id="0a7b3-117">**Process**</span></span>](id3dx10dataprocessor-process.md)                       | <span data-ttu-id="0a7b3-118">Processar alguns dados.</span><span class="sxs-lookup"><span data-stu-id="0a7b3-118">Process some data.</span></span><br/>                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="0a7b3-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="0a7b3-119">Remarks</span></span>

<span data-ttu-id="0a7b3-120">Esse objeto pode ser herdado e seus membros são redefinidos.</span><span class="sxs-lookup"><span data-stu-id="0a7b3-120">This object can be inherited and its members redefined.</span></span> <span data-ttu-id="0a7b3-121">Isso permitiria que você personalize a API para processar seus próprios formatos de arquivo personalizados.</span><span class="sxs-lookup"><span data-stu-id="0a7b3-121">Doing so would enable you to customize the API for processing your own custom file formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a7b3-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a7b3-122">Requirements</span></span>



| <span data-ttu-id="0a7b3-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a7b3-123">Requirement</span></span> | <span data-ttu-id="0a7b3-124">Valor</span><span class="sxs-lookup"><span data-stu-id="0a7b3-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0a7b3-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0a7b3-125">Header</span></span><br/>  | <dl> <span data-ttu-id="0a7b3-126"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a7b3-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="0a7b3-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0a7b3-127">Library</span></span><br/> | <dl> <span data-ttu-id="0a7b3-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0a7b3-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a7b3-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="0a7b3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a7b3-130">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="0a7b3-130">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
