---
description: Contém dados de entrada para uma \_ consulta D3DAUTHENTICATEDQUERY RESTRICTEDSHAREDRESOURCEPROCESS.
ms.assetid: a1ceb394-7af9-4f05-9f58-a3103bf0150e
title: Estrutura de D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_INPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 06c4421f048af80186077da022fdecfaea79dca6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768682"
---
# <a name="d3dauthenticatedchannel_queryrestrictedsharedresourceprocess_input-structure"></a><span data-ttu-id="4ff04-103">Estrutura de entrada do D3DAUTHENTICATEDCHANNEL \_ QUERYRESTRICTEDSHAREDRESOURCEPROCESS \_</span><span class="sxs-lookup"><span data-stu-id="4ff04-103">D3DAUTHENTICATEDCHANNEL\_QUERYRESTRICTEDSHAREDRESOURCEPROCESS\_INPUT structure</span></span>

<span data-ttu-id="4ff04-104">Contém dados de entrada para uma consulta [**D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESS**](d3dauthenticatedquery-restrictedsharedresourceprocess.md) .</span><span class="sxs-lookup"><span data-stu-id="4ff04-104">Contains input data for a [**D3DAUTHENTICATEDQUERY\_RESTRICTEDSHAREDRESOURCEPROCESS**](d3dauthenticatedquery-restrictedsharedresourceprocess.md) query.</span></span>

<span data-ttu-id="4ff04-105">Para enviar essa consulta, chame [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="4ff04-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="4ff04-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4ff04-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_INPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_INPUT Input;
  UINT                                ProcessIndex;
} D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_INPUT;
```



## <a name="members"></a><span data-ttu-id="4ff04-107">Membros</span><span class="sxs-lookup"><span data-stu-id="4ff04-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="4ff04-108">**Entrada**</span><span class="sxs-lookup"><span data-stu-id="4ff04-108">**Input**</span></span>
</dt> <dd>

<span data-ttu-id="4ff04-109">Uma estrutura de [**\_ \_ entrada de consulta D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-input.md) que contém o GUID para a consulta e outros dados.</span><span class="sxs-lookup"><span data-stu-id="4ff04-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**](d3dauthenticatedchannel-query-input.md) structure that contains the GUID for the query and other data.</span></span>

</dd> <dt>

<span data-ttu-id="4ff04-110">**ProcessIndex**</span><span class="sxs-lookup"><span data-stu-id="4ff04-110">**ProcessIndex**</span></span>
</dt> <dd>

<span data-ttu-id="4ff04-111">O índice do processo.</span><span class="sxs-lookup"><span data-stu-id="4ff04-111">The index of the process.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4ff04-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ff04-112">Requirements</span></span>



| <span data-ttu-id="4ff04-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ff04-113">Requirement</span></span> | <span data-ttu-id="4ff04-114">Valor</span><span class="sxs-lookup"><span data-stu-id="4ff04-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ff04-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ff04-115">Minimum supported client</span></span><br/> | <span data-ttu-id="4ff04-116">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4ff04-116">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4ff04-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ff04-117">Minimum supported server</span></span><br/> | <span data-ttu-id="4ff04-118">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="4ff04-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="4ff04-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4ff04-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ff04-120"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ff04-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ff04-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="4ff04-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ff04-122">Estruturas de vídeo do Direct3D</span><span class="sxs-lookup"><span data-stu-id="4ff04-122">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="4ff04-123">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="4ff04-123">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




