---
description: Contém a resposta a uma \_ consulta accessibilityattributes do D3DAUTHENTICATEDQUERY.
ms.assetid: 9f66a467-ba05-413b-b001-ea4c5ca4a37d
title: Estrutura de D3DAUTHENTICATEDCHANNEL_QUERYINFOBUSTYPE_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYINFOBUSTYPE_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 853488c98687825ab55d642b2e01e569f0d435c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105785967"
---
# <a name="d3dauthenticatedchannel_queryinfobustype_output-structure"></a><span data-ttu-id="95676-103">Estrutura de saída do D3DAUTHENTICATEDCHANNEL \_ QUERYINFOBUSTYPE \_</span><span class="sxs-lookup"><span data-stu-id="95676-103">D3DAUTHENTICATEDCHANNEL\_QUERYINFOBUSTYPE\_OUTPUT structure</span></span>

<span data-ttu-id="95676-104">Contém a resposta a uma [**consulta \_ accessibilityattributes do D3DAUTHENTICATEDQUERY**](d3dauthenticatedquery-accessibilityattributes.md) .</span><span class="sxs-lookup"><span data-stu-id="95676-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_ACCESSIBILITYATTRIBUTES**](d3dauthenticatedquery-accessibilityattributes.md) query.</span></span>

<span data-ttu-id="95676-105">Para enviar essa consulta, chame [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="95676-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="95676-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="95676-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYINFOBUSTYPE_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  D3DBUSTYPE                           BusType;
  BOOL                                 bAccessibleInContiguousBlocks;
  BOOL                                 bAccessibleInNonContiguousBlocks;
} D3DAUTHENTICATEDCHANNEL_QUERYINFOBUSTYPE_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="95676-107">Membros</span><span class="sxs-lookup"><span data-stu-id="95676-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="95676-108">**Saída**</span><span class="sxs-lookup"><span data-stu-id="95676-108">**Output**</span></span>
</dt> <dd>

<span data-ttu-id="95676-109">Uma estrutura de [**\_ \_ saída de consulta D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) que contém um Message Authentication Code (Mac) e outros dados.</span><span class="sxs-lookup"><span data-stu-id="95676-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="95676-110">**BusType**</span><span class="sxs-lookup"><span data-stu-id="95676-110">**BusType**</span></span>
</dt> <dd>

<span data-ttu-id="95676-111">Um or de bit **ou** de sinalizadores da enumeração [**D3DBUSTYPE**](d3dbustype.md) .</span><span class="sxs-lookup"><span data-stu-id="95676-111">A bitwise **OR** of flags from the [**D3DBUSTYPE**](d3dbustype.md) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="95676-112">**bAccessibleInContiguousBlocks**</span><span class="sxs-lookup"><span data-stu-id="95676-112">**bAccessibleInContiguousBlocks**</span></span>
</dt> <dd>

<span data-ttu-id="95676-113">Se **for verdadeiro**, blocos contíguos de memória de vídeo poderão ser acessíveis para a CPU ou para o barramento.</span><span class="sxs-lookup"><span data-stu-id="95676-113">If **TRUE**, contiguous blocks of video memory may be accessible to the CPU or the bus.</span></span>

</dd> <dt>

<span data-ttu-id="95676-114">**bAccessibleInNonContiguousBlocks**</span><span class="sxs-lookup"><span data-stu-id="95676-114">**bAccessibleInNonContiguousBlocks**</span></span>
</dt> <dd>

<span data-ttu-id="95676-115">Se **for verdadeiro**, blocos não contíguos de memória de vídeo poderão estar acessíveis para a CPU ou para o barramento.</span><span class="sxs-lookup"><span data-stu-id="95676-115">If **TRUE**, non-contiguous blocks of video memory may be accessible to the CPU or the bus.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="95676-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95676-116">Requirements</span></span>



| <span data-ttu-id="95676-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="95676-117">Requirement</span></span> | <span data-ttu-id="95676-118">Valor</span><span class="sxs-lookup"><span data-stu-id="95676-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="95676-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="95676-119">Minimum supported client</span></span><br/> | <span data-ttu-id="95676-120">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="95676-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="95676-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="95676-121">Minimum supported server</span></span><br/> | <span data-ttu-id="95676-122">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="95676-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="95676-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="95676-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="95676-124"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="95676-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95676-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="95676-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95676-126">Estruturas de vídeo do Direct3D</span><span class="sxs-lookup"><span data-stu-id="95676-126">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="95676-127">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="95676-127">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




