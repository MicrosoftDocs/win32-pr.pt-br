---
description: Contém a resposta a uma \_ consulta D3DAUTHENTICATEDQUERY UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT.
ms.assetid: c283833d-e98c-4f01-b623-21027a6b90e8
title: Estrutura de D3DAUTHENTICATEDCHANNEL_QUERYUNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYUNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b3fd30cff59d35f845903e7f4fdb08cdff61df3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782280"
---
# <a name="d3dauthenticatedchannel_queryunrestrictedprotectedsharedresourcecount_output-structure"></a><span data-ttu-id="2c95c-103">Estrutura de saída do D3DAUTHENTICATEDCHANNEL \_ QUERYUNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT \_</span><span class="sxs-lookup"><span data-stu-id="2c95c-103">D3DAUTHENTICATEDCHANNEL\_QUERYUNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT\_OUTPUT structure</span></span>

<span data-ttu-id="2c95c-104">Contém a resposta a uma consulta [**D3DAUTHENTICATEDQUERY \_ UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT**](d3dauthenticatedquery-unrestrictedprotectedsharedresourcecount.md) .</span><span class="sxs-lookup"><span data-stu-id="2c95c-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT**](d3dauthenticatedquery-unrestrictedprotectedsharedresourcecount.md) query.</span></span>

<span data-ttu-id="2c95c-105">Para enviar essa consulta, chame [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="2c95c-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="2c95c-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2c95c-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYUNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  UINT                                 NumUnrestrictedProtectedSharedResources;
} D3DAUTHENTICATEDCHANNEL_QUERYUNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="2c95c-107">Membros</span><span class="sxs-lookup"><span data-stu-id="2c95c-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="2c95c-108">**Saída**</span><span class="sxs-lookup"><span data-stu-id="2c95c-108">**Output**</span></span>
</dt> <dd>

<span data-ttu-id="2c95c-109">Uma estrutura de [**\_ \_ saída de consulta D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) que contém um Message Authentication Code (Mac) e outros dados.</span><span class="sxs-lookup"><span data-stu-id="2c95c-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="2c95c-110">**NumUnrestrictedProtectedSharedResources**</span><span class="sxs-lookup"><span data-stu-id="2c95c-110">**NumUnrestrictedProtectedSharedResources**</span></span>
</dt> <dd>

<span data-ttu-id="2c95c-111">O número de recursos protegidos e compartilhados que podem ser abertos por qualquer processo sem restrições.</span><span class="sxs-lookup"><span data-stu-id="2c95c-111">The number of protected, shared resources that can be opened by any process without restrictions.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2c95c-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c95c-112">Requirements</span></span>



| <span data-ttu-id="2c95c-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c95c-113">Requirement</span></span> | <span data-ttu-id="2c95c-114">Valor</span><span class="sxs-lookup"><span data-stu-id="2c95c-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c95c-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2c95c-115">Minimum supported client</span></span><br/> | <span data-ttu-id="2c95c-116">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="2c95c-116">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2c95c-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2c95c-117">Minimum supported server</span></span><br/> | <span data-ttu-id="2c95c-118">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="2c95c-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="2c95c-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2c95c-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c95c-120"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c95c-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c95c-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="2c95c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c95c-122">Estruturas de vídeo do Direct3D</span><span class="sxs-lookup"><span data-stu-id="2c95c-122">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="2c95c-123">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="2c95c-123">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




