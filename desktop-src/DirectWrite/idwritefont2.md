---
title: Interface IDWriteFont2
description: Representa uma fonte física em uma coleção de fontes.
ms.assetid: 4E3069AE-5882-4A26-A36D-BE7D7EE1B0C3
keywords:
- Gravação direta da interface IDWriteFont2
- Gravação direta da interface IDWriteFont2, descrita
topic_type:
- apiref
api_name:
- IDWriteFont2
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f82a47e56915747b0e118a6f63484b9dd3dcdbd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295816"
---
# <a name="idwritefont2-interface"></a><span data-ttu-id="f512a-105">Interface IDWriteFont2</span><span class="sxs-lookup"><span data-stu-id="f512a-105">IDWriteFont2 interface</span></span>

<span data-ttu-id="f512a-106">Representa uma fonte física em uma coleção de fontes.</span><span class="sxs-lookup"><span data-stu-id="f512a-106">Represents a physical font in a font collection.</span></span>

<span data-ttu-id="f512a-107">Essa interface adiciona a capacidade de verificar se um caminho de renderização de cor é potencialmente necessário.</span><span class="sxs-lookup"><span data-stu-id="f512a-107">This interface adds the ability to check if a color rendering path is potentially necessary.</span></span>

## <a name="members"></a><span data-ttu-id="f512a-108">Membros</span><span class="sxs-lookup"><span data-stu-id="f512a-108">Members</span></span>

<span data-ttu-id="f512a-109">A interface **IDWriteFont2** herda de [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1).</span><span class="sxs-lookup"><span data-stu-id="f512a-109">The **IDWriteFont2** interface inherits from [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1).</span></span> <span data-ttu-id="f512a-110">**IDWriteFont2** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f512a-110">**IDWriteFont2** also has these types of members:</span></span>

-   [<span data-ttu-id="f512a-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="f512a-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f512a-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="f512a-112">Methods</span></span>

<span data-ttu-id="f512a-113">A interface **IDWriteFont2** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="f512a-113">The **IDWriteFont2** interface has these methods.</span></span>



| <span data-ttu-id="f512a-114">Método</span><span class="sxs-lookup"><span data-stu-id="f512a-114">Method</span></span>                                          | <span data-ttu-id="f512a-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="f512a-115">Description</span></span>                                                                        |
|:------------------------------------------------|:-----------------------------------------------------------------------------------|
| [<span data-ttu-id="f512a-116">**IsColorFont**</span><span class="sxs-lookup"><span data-stu-id="f512a-116">**IsColorFont**</span></span>](idwritefont2-iscolorfont.md) | <span data-ttu-id="f512a-117">Permite determinar se um caminho de renderização de cor é potencialmente necessário.</span><span class="sxs-lookup"><span data-stu-id="f512a-117">Enables determining if a color rendering path is potentially necessary.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f512a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f512a-118">Requirements</span></span>



| <span data-ttu-id="f512a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f512a-119">Requirement</span></span> | <span data-ttu-id="f512a-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f512a-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f512a-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f512a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f512a-122">Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="f512a-122">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="f512a-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f512a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f512a-124">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="f512a-124">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="f512a-125">Número mínimo de telefone com suporte</span><span class="sxs-lookup"><span data-stu-id="f512a-125">Minimum supported phone</span></span><br/>  | <span data-ttu-id="f512a-126">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="f512a-126">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="f512a-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f512a-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="f512a-128"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f512a-128"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="f512a-129">DLL</span><span class="sxs-lookup"><span data-stu-id="f512a-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f512a-130"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f512a-130"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f512a-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="f512a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f512a-132">**IDWriteFont1**</span><span class="sxs-lookup"><span data-stu-id="f512a-132">**IDWriteFont1**</span></span>](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1)
</dt> </dl>

 

