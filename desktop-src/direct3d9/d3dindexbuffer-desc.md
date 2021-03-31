---
description: Descreve um buffer de índice.
ms.assetid: 5d45213e-b3c0-4eb7-a4f9-8d8730eb3899
title: Estrutura de D3DINDEXBUFFER_DESC (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DINDEXBUFFER_DESC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 0a0bf63e732541f9394231cd82c23ff71a584b1e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930624"
---
# <a name="d3dindexbuffer_desc-structure"></a><span data-ttu-id="c3ce3-103">\_Estrutura desc de D3DINDEXBUFFER</span><span class="sxs-lookup"><span data-stu-id="c3ce3-103">D3DINDEXBUFFER\_DESC structure</span></span>

<span data-ttu-id="c3ce3-104">Descreve um buffer de índice.</span><span class="sxs-lookup"><span data-stu-id="c3ce3-104">Describes an index buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3ce3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c3ce3-105">Syntax</span></span>


```C++
typedef struct D3DINDEXBUFFER_DESC {
  D3DFORMAT       Format;
  D3DRESOURCETYPE Type;
  DWORD           Usage;
  D3DPOOL         Pool;
  UINT            Size;
} D3DINDEXBUFFER_DESC, *LPD3DINDEXBUFFER_DESC;
```



## <a name="members"></a><span data-ttu-id="c3ce3-106">Membros</span><span class="sxs-lookup"><span data-stu-id="c3ce3-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c3ce3-107">**Formato**</span><span class="sxs-lookup"><span data-stu-id="c3ce3-107">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="c3ce3-108">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="c3ce3-108">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c3ce3-109">Membro do tipo enumerado [D3DFORMAT](d3dformat.md) , que descreve o formato da superfície dos dados do buffer do índice.</span><span class="sxs-lookup"><span data-stu-id="c3ce3-109">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the surface format of the index buffer data.</span></span>

</dd> <dt>

<span data-ttu-id="c3ce3-110">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c3ce3-110">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="c3ce3-111">Tipo: **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**</span><span class="sxs-lookup"><span data-stu-id="c3ce3-111">Type: **[**D3DRESOURCETYPE**](./d3dresourcetype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c3ce3-112">Membro do tipo enumerado [**D3DRESOURCETYPE**](./d3dresourcetype.md) , identificando esse recurso como um buffer de índice.</span><span class="sxs-lookup"><span data-stu-id="c3ce3-112">Member of the [**D3DRESOURCETYPE**](./d3dresourcetype.md) enumerated type, identifying this resource as an index buffer.</span></span>

</dd> <dt>

<span data-ttu-id="c3ce3-113">**Usage**</span><span class="sxs-lookup"><span data-stu-id="c3ce3-113">**Usage**</span></span>
</dt> <dd>

<span data-ttu-id="c3ce3-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c3ce3-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c3ce3-115">Combinação de um ou mais dos sinalizadores a seguir, especificando o uso desse recurso.</span><span class="sxs-lookup"><span data-stu-id="c3ce3-115">Combination of one or more of the following flags, specifying the usage for this resource.</span></span>



| <span data-ttu-id="c3ce3-116">Valor</span><span class="sxs-lookup"><span data-stu-id="c3ce3-116">Value</span></span>                                                                                                                                                                                                   | <span data-ttu-id="c3ce3-117">Significado</span><span class="sxs-lookup"><span data-stu-id="c3ce3-117">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DUSAGE_DONOTCLIP"></span><span id="d3dusage_donotclip"></span><dl> <span data-ttu-id="c3ce3-118"><dt>**D3DUSAGE \_ DONOTCLIP**</dt></span><span class="sxs-lookup"><span data-stu-id="c3ce3-118"><dt>**D3DUSAGE\_DONOTCLIP**</dt></span></span> </dl>                            | <span data-ttu-id="c3ce3-119">Defina para indicar que o conteúdo do buffer de índice nunca exigirá o recorte.</span><span class="sxs-lookup"><span data-stu-id="c3ce3-119">Set to indicate that the index buffer content will never require clipping.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="D3DUSAGE_DYNAMIC"></span><span id="d3dusage_dynamic"></span><dl> <span data-ttu-id="c3ce3-120"><dt>**D3DUSAGE \_ dinâmico**</dt></span><span class="sxs-lookup"><span data-stu-id="c3ce3-120"><dt>**D3DUSAGE\_DYNAMIC**</dt></span></span> </dl>                                  | <span data-ttu-id="c3ce3-121">Defina para indicar que o buffer de índice requer uso de memória dinâmica.</span><span class="sxs-lookup"><span data-stu-id="c3ce3-121">Set to indicate that the index buffer requires dynamic memory use.</span></span> <span data-ttu-id="c3ce3-122">Isso é útil para drivers porque permite que eles decidam onde posicionar o buffer.</span><span class="sxs-lookup"><span data-stu-id="c3ce3-122">This is useful for drivers because it enables them to decide where to place the buffer.</span></span> <span data-ttu-id="c3ce3-123">Em geral, os buffers de índice estáticos são colocados na memória de vídeo e os buffers de índice dinâmicos são colocados na memória AGP.</span><span class="sxs-lookup"><span data-stu-id="c3ce3-123">In general, static index buffers are placed in video memory and dynamic index buffers are placed in AGP memory.</span></span> <span data-ttu-id="c3ce3-124">Observe que não há nenhum uso estático separado; Se você não especificar D3DUSAGE \_ Dynamic, o buffer de índice se tornará estático.</span><span class="sxs-lookup"><span data-stu-id="c3ce3-124">Note that there is no separate static usage; if you do not specify D3DUSAGE\_DYNAMIC the index buffer is made static.</span></span> <span data-ttu-id="c3ce3-125">\_O D3DUSAGE Dynamic é estritamente imposto por meio dos \_ sinalizadores de bloqueio D3DLOCK descarte e D3DLOCK \_ NoOverwrite.</span><span class="sxs-lookup"><span data-stu-id="c3ce3-125">D3DUSAGE\_DYNAMIC is strictly enforced through the D3DLOCK\_DISCARD and D3DLOCK\_NOOVERWRITE locking flags.</span></span> <span data-ttu-id="c3ce3-126">Como resultado, D3DLOCK \_ descarte e D3DLOCK \_ NoOverwrite só são válidos em buffers de índice criados com D3DUSAGE \_ Dynamic; eles não são sinalizadores válidos em buffers de vértice estáticos.</span><span class="sxs-lookup"><span data-stu-id="c3ce3-126">As a result, D3DLOCK\_DISCARD and D3DLOCK\_NOOVERWRITE are only valid on index buffers created with D3DUSAGE\_DYNAMIC; they are not valid flags on static vertex buffers.</span></span><br/> <span data-ttu-id="c3ce3-127">Para obter mais informações sobre como usar buffers de índice dinâmico, consulte [usando o vértice dinâmico e buffers de índice](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="c3ce3-127">For more information about using dynamic index buffers, see [Using Dynamic Vertex and Index Buffers](performance-optimizations.md).</span></span><br/> <span data-ttu-id="c3ce3-128">Observe que D3DUSAGE \_ Dynamic não pode ser especificado em buffers de índice gerenciados.</span><span class="sxs-lookup"><span data-stu-id="c3ce3-128">Note that D3DUSAGE\_DYNAMIC cannot be specified on managed index buffers.</span></span> <span data-ttu-id="c3ce3-129">Para obter mais informações, consulte [Managing Resources (Direct3D 9)](managing-resources.md).</span><span class="sxs-lookup"><span data-stu-id="c3ce3-129">For more information, see [Managing Resources (Direct3D 9)](managing-resources.md).</span></span><br/> |
| <span id="D3DUSAGE_RTPATCHES"></span><span id="d3dusage_rtpatches"></span><dl> <span data-ttu-id="c3ce3-130"><dt>**D3DUSAGE \_ RTPATCHES**</dt></span><span class="sxs-lookup"><span data-stu-id="c3ce3-130"><dt>**D3DUSAGE\_RTPATCHES**</dt></span></span> </dl>                            | <span data-ttu-id="c3ce3-131">Defina para indicar quando o buffer de índice deve ser usado para desenhar primitivos de ordem alta.</span><span class="sxs-lookup"><span data-stu-id="c3ce3-131">Set to indicate when the index buffer is to be used for drawing high-order primitives.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="D3DUSAGE_NPATCHES"></span><span id="d3dusage_npatches"></span><dl> <span data-ttu-id="c3ce3-132"><dt>**D3DUSAGE \_ NPATCHES**</dt></span><span class="sxs-lookup"><span data-stu-id="c3ce3-132"><dt>**D3DUSAGE\_NPATCHES**</dt></span></span> </dl>                               | <span data-ttu-id="c3ce3-133">Defina para indicar quando o buffer de índice deve ser usado para desenhar N patches.</span><span class="sxs-lookup"><span data-stu-id="c3ce3-133">Set to indicate when the index buffer is to be used for drawing N patches.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="D3DUSAGE_POINTS"></span><span id="d3dusage_points"></span><dl> <span data-ttu-id="c3ce3-134"><dt>**Pontos de D3DUSAGE \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c3ce3-134"><dt>**D3DUSAGE\_POINTS**</dt></span></span> </dl>                                     | <span data-ttu-id="c3ce3-135">Defina para indicar quando o buffer de índice deve ser usado para sprites de ponto de desenho ou listas de pontos indexados.</span><span class="sxs-lookup"><span data-stu-id="c3ce3-135">Set to indicate when the index buffer is to be used for drawing point sprites or indexed point lists.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="D3DUSAGE_SOFTWAREPROCESSING"></span><span id="d3dusage_softwareprocessing"></span><dl> <span data-ttu-id="c3ce3-136"><dt>**D3DUSAGE \_ SOFTWAREPROCESSING**</dt></span><span class="sxs-lookup"><span data-stu-id="c3ce3-136"><dt>**D3DUSAGE\_SOFTWAREPROCESSING**</dt></span></span> </dl> | <span data-ttu-id="c3ce3-137">Defina para indicar que o buffer deve ser usado com o processamento de software.</span><span class="sxs-lookup"><span data-stu-id="c3ce3-137">Set to indicate that the buffer is to be used with software processing.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="D3DUSAGE_WRITEONLY"></span><span id="d3dusage_writeonly"></span><dl> <span data-ttu-id="c3ce3-138"><dt>**\_WRITEONLY D3DUSAGE**</dt></span><span class="sxs-lookup"><span data-stu-id="c3ce3-138"><dt>**D3DUSAGE\_WRITEONLY**</dt></span></span> </dl>                            | <span data-ttu-id="c3ce3-139">Informa ao sistema que o aplicativo grava somente no buffer de índice.</span><span class="sxs-lookup"><span data-stu-id="c3ce3-139">Informs the system that the application writes only to the index buffer.</span></span> <span data-ttu-id="c3ce3-140">O uso desse sinalizador permite que o driver escolha o melhor local de memória para operações de gravação e renderização eficientes.</span><span class="sxs-lookup"><span data-stu-id="c3ce3-140">Using this flag enables the driver to choose the best memory location for efficient write operations and rendering.</span></span> <span data-ttu-id="c3ce3-141">As tentativas de ler de um buffer de índice criado com esse recurso podem resultar em degradação do desempenho.</span><span class="sxs-lookup"><span data-stu-id="c3ce3-141">Attempts to read from an index buffer that is created with this capability can result in degraded performance.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

<span data-ttu-id="c3ce3-142">**Pool**</span><span class="sxs-lookup"><span data-stu-id="c3ce3-142">**Pool**</span></span>
</dt> <dd>

<span data-ttu-id="c3ce3-143">Tipo: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="c3ce3-143">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c3ce3-144">Membro do tipo enumerado [**D3DPOOL**](./d3dpool.md) , especificando a classe de memória alocada para esse buffer de índice.</span><span class="sxs-lookup"><span data-stu-id="c3ce3-144">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, specifying the class of memory allocated for this index buffer.</span></span>

</dd> <dt>

<span data-ttu-id="c3ce3-145">**Tamanho**</span><span class="sxs-lookup"><span data-stu-id="c3ce3-145">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="c3ce3-146">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c3ce3-146">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c3ce3-147">Tamanho do buffer de índice, em bytes.</span><span class="sxs-lookup"><span data-stu-id="c3ce3-147">Size of the index buffer, in bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c3ce3-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3ce3-148">Requirements</span></span>



| <span data-ttu-id="c3ce3-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3ce3-149">Requirement</span></span> | <span data-ttu-id="c3ce3-150">Valor</span><span class="sxs-lookup"><span data-stu-id="c3ce3-150">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c3ce3-151">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c3ce3-151">Header</span></span><br/> | <dl> <span data-ttu-id="c3ce3-152"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3ce3-152"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3ce3-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="c3ce3-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3ce3-154">Estruturas do Direct3D</span><span class="sxs-lookup"><span data-stu-id="c3ce3-154">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="c3ce3-155">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="c3ce3-155">**GetDesc**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-getdesc)
</dt> <dt>

[<span data-ttu-id="c3ce3-156">Buffers de índice (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="c3ce3-156">Index Buffers (Direct3D 9)</span></span>](index-buffers.md)
</dt> </dl>

 

 
