---
title: Interface ID3DX11DataLoader (D3DX11core. h)
description: Observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Objeto de carregamento de dados usado pela interface ID3DX11ThreadPump para carregar dados de forma assíncrona.
ms.assetid: 878929ea-0228-4650-9ca0-f83d60d9f915
keywords:
- Interface ID3DX11DataLoader Direct3D 11
- Interface ID3DX11DataLoader Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11DataLoader
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68236451bf2ba6f491d17541f7d4ca627f5063c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085259"
---
# <a name="id3dx11dataloader-interface"></a><span data-ttu-id="01801-106">Interface ID3DX11DataLoader</span><span class="sxs-lookup"><span data-stu-id="01801-106">ID3DX11DataLoader interface</span></span>

> [!Note]  
> <span data-ttu-id="01801-107">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="01801-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="01801-108">Objeto de carregamento de dados usado pela [**interface ID3DX11ThreadPump**](id3dx11threadpump.md) para carregar dados de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="01801-108">Data loading object used by [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md) for loading data asynchronously.</span></span>

## <a name="members"></a><span data-ttu-id="01801-109">Membros</span><span class="sxs-lookup"><span data-stu-id="01801-109">Members</span></span>

<span data-ttu-id="01801-110">A interface **ID3DX11DataLoader** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="01801-110">The **ID3DX11DataLoader** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="01801-111">**ID3DX11DataLoader** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="01801-111">**ID3DX11DataLoader** also has these types of members:</span></span>

-   [<span data-ttu-id="01801-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="01801-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="01801-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="01801-113">Methods</span></span>

<span data-ttu-id="01801-114">A interface **ID3DX11DataLoader** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="01801-114">The **ID3DX11DataLoader** interface has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="01801-115">Método</span><span class="sxs-lookup"><span data-stu-id="01801-115">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="01801-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="01801-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="01801-117"><a href="id3dx11dataloader-decompress.md"><strong>Descompactar</strong></a></span><span class="sxs-lookup"><span data-stu-id="01801-117"><a href="id3dx11dataloader-decompress.md"><strong>Decompress</strong></a></span></span></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="01801-118">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="01801-118">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/> <span data-ttu-id="01801-119">Descompacta dados codificados.</span><span class="sxs-lookup"><span data-stu-id="01801-119">Decompresses encoded data.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="01801-120"><a href="id3dx11dataloader-destroy.md"><strong>Destruir</strong></a></span><span class="sxs-lookup"><span data-stu-id="01801-120"><a href="id3dx11dataloader-destroy.md"><strong>Destroy</strong></a></span></span></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="01801-121">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="01801-121">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/> <span data-ttu-id="01801-122">Destrói o carregador após a conclusão de um item de trabalho.</span><span class="sxs-lookup"><span data-stu-id="01801-122">Destroys the loader after a work item completes.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="01801-123"><a href="id3dx11dataloader-load.md"><strong>Carregamento</strong></a></span><span class="sxs-lookup"><span data-stu-id="01801-123"><a href="id3dx11dataloader-load.md"><strong>Load</strong></a></span></span></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="01801-124">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="01801-124">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/> <span data-ttu-id="01801-125">Carrega dados de um disco.</span><span class="sxs-lookup"><span data-stu-id="01801-125">Loads data from a disk.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="01801-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="01801-126">Remarks</span></span>

<span data-ttu-id="01801-127">Esse objeto pode ser herdado e seus membros são redefinidos.</span><span class="sxs-lookup"><span data-stu-id="01801-127">This object can be inherited and its members redefined.</span></span> <span data-ttu-id="01801-128">Isso permitiria que você personalize a API para carregar e descompactar seus próprios formatos de arquivo personalizados.</span><span class="sxs-lookup"><span data-stu-id="01801-128">Doing so would enable you to customize the API for loading and decompressing your own custom file formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="01801-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01801-129">Requirements</span></span>



| <span data-ttu-id="01801-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="01801-130">Requirement</span></span> | <span data-ttu-id="01801-131">Valor</span><span class="sxs-lookup"><span data-stu-id="01801-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="01801-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01801-132">Minimum supported client</span></span><br/> | <span data-ttu-id="01801-133">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="01801-133">Windows 7 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="01801-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01801-134">Minimum supported server</span></span><br/> | <span data-ttu-id="01801-135">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="01801-135">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="01801-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="01801-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="01801-137"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="01801-137"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="01801-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="01801-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="01801-139"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="01801-139"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="01801-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="01801-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01801-141">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="01801-141">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

