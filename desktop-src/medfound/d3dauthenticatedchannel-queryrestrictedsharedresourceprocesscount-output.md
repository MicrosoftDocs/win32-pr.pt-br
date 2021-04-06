---
description: Contém a resposta a uma \_ consulta D3DAUTHENTICATEDQUERY RESTRICTEDSHAREDRESOURCEPROCESSCOUNT.
ms.assetid: dd6286d8-dfb5-413a-ba38-8b99dc8fe305
title: Estrutura de D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 60568e7056ab9df7aafcec1cac7864685c7c6100
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646603"
---
# <a name="d3dauthenticatedchannel_queryrestrictedsharedresourceprocesscount_output-structure"></a><span data-ttu-id="2e395-103">Estrutura de saída do D3DAUTHENTICATEDCHANNEL \_ QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT \_</span><span class="sxs-lookup"><span data-stu-id="2e395-103">D3DAUTHENTICATEDCHANNEL\_QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT\_OUTPUT structure</span></span>

<span data-ttu-id="2e395-104">Contém a resposta a uma consulta [**D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESSCOUNT**](d3dauthenticatedquery-restrictedsharedresourceprocesscount.md) .</span><span class="sxs-lookup"><span data-stu-id="2e395-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_RESTRICTEDSHAREDRESOURCEPROCESSCOUNT**](d3dauthenticatedquery-restrictedsharedresourceprocesscount.md) query.</span></span>

<span data-ttu-id="2e395-105">Para enviar essa consulta, chame [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="2e395-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="2e395-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2e395-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  UINT                                 NumRestrictedSharedResourceProcesses;
} D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="2e395-107">Membros</span><span class="sxs-lookup"><span data-stu-id="2e395-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="2e395-108">**Saída**</span><span class="sxs-lookup"><span data-stu-id="2e395-108">**Output**</span></span>
</dt> <dd>

<span data-ttu-id="2e395-109">Uma estrutura de [**\_ \_ saída de consulta D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) que contém um Message Authentication Code (Mac) e outros dados.</span><span class="sxs-lookup"><span data-stu-id="2e395-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="2e395-110">**NumRestrictedSharedResourceProcesses**</span><span class="sxs-lookup"><span data-stu-id="2e395-110">**NumRestrictedSharedResourceProcesses**</span></span>
</dt> <dd>

<span data-ttu-id="2e395-111">O número de processos com permissão para abrir recursos compartilhados que têm acesso restrito.</span><span class="sxs-lookup"><span data-stu-id="2e395-111">The number of processes allowed to open shared resources that have restricted access.</span></span> <span data-ttu-id="2e395-112">Um processo não pode abrir um recurso desse tipo, a menos que o processo tenha sido concedido acesso.</span><span class="sxs-lookup"><span data-stu-id="2e395-112">A process cannot open such a resource unless the process has been granted access.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2e395-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e395-113">Requirements</span></span>



| <span data-ttu-id="2e395-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e395-114">Requirement</span></span> | <span data-ttu-id="2e395-115">Valor</span><span class="sxs-lookup"><span data-stu-id="2e395-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e395-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2e395-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2e395-117">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="2e395-117">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2e395-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2e395-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2e395-119">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="2e395-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="2e395-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2e395-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e395-121"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e395-121"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e395-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="2e395-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e395-123">Estruturas de vídeo do Direct3D</span><span class="sxs-lookup"><span data-stu-id="2e395-123">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="2e395-124">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="2e395-124">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




