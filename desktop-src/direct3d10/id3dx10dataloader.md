---
description: Objeto de carregamento de dados usado pela interface ID3DX10ThreadPump para carregar dados de forma assíncrona.
ms.assetid: bda2414c-bbab-47ac-b23a-f58fb86e732d
title: Interface ID3DX10DataLoader (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataLoader
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: b0e45d24d663f0ba9a8978bc251a4adf0c7868fd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930608"
---
# <a name="id3dx10dataloader-interface"></a><span data-ttu-id="100f1-103">Interface ID3DX10DataLoader</span><span class="sxs-lookup"><span data-stu-id="100f1-103">ID3DX10DataLoader interface</span></span>

<span data-ttu-id="100f1-104">Objeto de carregamento de dados usado pela [**interface ID3DX10ThreadPump**](id3dx10threadpump.md) para carregar dados de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="100f1-104">Data loading object used by [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md) for loading data asynchronously.</span></span>

## <a name="members"></a><span data-ttu-id="100f1-105">Membros</span><span class="sxs-lookup"><span data-stu-id="100f1-105">Members</span></span>

<span data-ttu-id="100f1-106">A interface **ID3DX10DataLoader** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="100f1-106">The **ID3DX10DataLoader** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="100f1-107">**ID3DX10DataLoader** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="100f1-107">**ID3DX10DataLoader** also has these types of members:</span></span>

-   [<span data-ttu-id="100f1-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="100f1-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="100f1-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="100f1-109">Methods</span></span>

<span data-ttu-id="100f1-110">A interface **ID3DX10DataLoader** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="100f1-110">The **ID3DX10DataLoader** interface has these methods.</span></span>



| <span data-ttu-id="100f1-111">Método</span><span class="sxs-lookup"><span data-stu-id="100f1-111">Method</span></span>                                             | <span data-ttu-id="100f1-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="100f1-112">Description</span></span>                                                                                                                                                                                                                        |
|:---------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="100f1-113">**Descompactar**</span><span class="sxs-lookup"><span data-stu-id="100f1-113">**Decompress**</span></span>](id3dx10dataloader-decompress.md) | <span data-ttu-id="100f1-114">Usado para descompactar dados codificados.</span><span class="sxs-lookup"><span data-stu-id="100f1-114">Used to decompress encoded data.</span></span> <span data-ttu-id="100f1-115">Normalmente, isso seria usado para carregar recursos de sistemas de arquivos, como arquivos ZIP.</span><span class="sxs-lookup"><span data-stu-id="100f1-115">Typically this would be used to load resources from file systems, such as ZIP files.</span></span> <span data-ttu-id="100f1-116">Ao carregar de um recurso descompactado, o estágio de descompactação não precisa fazer nenhum trabalho.</span><span class="sxs-lookup"><span data-stu-id="100f1-116">When loading from an uncompressed resource, the decompression stage does not have to do any work.</span></span><br/> |
| [<span data-ttu-id="100f1-117">**Destruir**</span><span class="sxs-lookup"><span data-stu-id="100f1-117">**Destroy**</span></span>](id3dx10dataloader-destroy.md)       | <span data-ttu-id="100f1-118">Usado por uma [**interface ID3DX10ThreadPump**](id3dx10threadpump.md) para destruir o carregador após a conclusão de um item de trabalho.</span><span class="sxs-lookup"><span data-stu-id="100f1-118">Used by a [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md) to destroy the loader after a work item completes.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="100f1-119">**Carregar**</span><span class="sxs-lookup"><span data-stu-id="100f1-119">**Load**</span></span>](id3dx10dataloader-load.md)             | <span data-ttu-id="100f1-120">Usado por uma [**interface ID3DX10ThreadPump**](id3dx10threadpump.md) para carregar dados de um disco.</span><span class="sxs-lookup"><span data-stu-id="100f1-120">Used by a [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md) to load data from a disk.</span></span><br/>                                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="100f1-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="100f1-121">Remarks</span></span>

<span data-ttu-id="100f1-122">Esse objeto pode ser herdado e seus membros são redefinidos.</span><span class="sxs-lookup"><span data-stu-id="100f1-122">This object can be inherited and its members redefined.</span></span> <span data-ttu-id="100f1-123">Isso permitiria que você personalize a API para carregar e descompactar seus próprios formatos de arquivo personalizados.</span><span class="sxs-lookup"><span data-stu-id="100f1-123">Doing so would enable you to customize the API for loading and decompressing your own custom file formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="100f1-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="100f1-124">Requirements</span></span>



| <span data-ttu-id="100f1-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="100f1-125">Requirement</span></span> | <span data-ttu-id="100f1-126">Valor</span><span class="sxs-lookup"><span data-stu-id="100f1-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="100f1-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="100f1-127">Header</span></span><br/>  | <dl> <span data-ttu-id="100f1-128"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="100f1-128"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="100f1-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="100f1-129">Library</span></span><br/> | <dl> <span data-ttu-id="100f1-130"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="100f1-130"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="100f1-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="100f1-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="100f1-132">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="100f1-132">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
