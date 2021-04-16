---
description: Contém dados de entrada para uma \_ consulta outputid D3DAUTHENTICATEDQUERY.
ms.assetid: 8864c298-be9a-4ff4-a9c5-996b62937c18
title: Estrutura de D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_INPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 7c64d43261ccc849772372110ad73169c698cd0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765172"
---
# <a name="d3dauthenticatedchannel_queryoutputid_input-structure"></a><span data-ttu-id="362a2-103">Estrutura de entrada do D3DAUTHENTICATEDCHANNEL \_ QUERYOUTPUTID \_</span><span class="sxs-lookup"><span data-stu-id="362a2-103">D3DAUTHENTICATEDCHANNEL\_QUERYOUTPUTID\_INPUT structure</span></span>

<span data-ttu-id="362a2-104">Contém dados de entrada para uma consulta [**\_ outputid D3DAUTHENTICATEDQUERY**](d3dauthenticatedquery-outputid.md) .</span><span class="sxs-lookup"><span data-stu-id="362a2-104">Contains input data for a [**D3DAUTHENTICATEDQUERY\_OUTPUTID**](d3dauthenticatedquery-outputid.md) query.</span></span>

<span data-ttu-id="362a2-105">Para enviar essa consulta, chame [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="362a2-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="362a2-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="362a2-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_INPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_INPUT Input;
  HANDLE                              DeviceHandle;
  HANDLE                              CryptoSessionHandle;
  UINT                                OutputIDIndex;
} D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_INPUT;
```



## <a name="members"></a><span data-ttu-id="362a2-107">Membros</span><span class="sxs-lookup"><span data-stu-id="362a2-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="362a2-108">**Entrada**</span><span class="sxs-lookup"><span data-stu-id="362a2-108">**Input**</span></span>
</dt> <dd>

<span data-ttu-id="362a2-109">Uma estrutura de [**\_ \_ entrada de consulta D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-input.md) que contém o GUID para a consulta e outros dados.</span><span class="sxs-lookup"><span data-stu-id="362a2-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**](d3dauthenticatedchannel-query-input.md) structure that contains the GUID for the query and other data.</span></span>

</dd> <dt>

<span data-ttu-id="362a2-110">**DeviceHandle**</span><span class="sxs-lookup"><span data-stu-id="362a2-110">**DeviceHandle**</span></span>
</dt> <dd>

<span data-ttu-id="362a2-111">Um identificador para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="362a2-111">A handle to the device.</span></span>

</dd> <dt>

<span data-ttu-id="362a2-112">**CryptoSessionHandle**</span><span class="sxs-lookup"><span data-stu-id="362a2-112">**CryptoSessionHandle**</span></span>
</dt> <dd>

<span data-ttu-id="362a2-113">Um identificador para a sessão de criptografia.</span><span class="sxs-lookup"><span data-stu-id="362a2-113">A handle to the cryptographic session.</span></span>

</dd> <dt>

<span data-ttu-id="362a2-114">**OutputIDIndex**</span><span class="sxs-lookup"><span data-stu-id="362a2-114">**OutputIDIndex**</span></span>
</dt> <dd>

<span data-ttu-id="362a2-115">O índice da ID de saída.</span><span class="sxs-lookup"><span data-stu-id="362a2-115">The index of the output ID.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="362a2-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="362a2-116">Requirements</span></span>



| <span data-ttu-id="362a2-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="362a2-117">Requirement</span></span> | <span data-ttu-id="362a2-118">Valor</span><span class="sxs-lookup"><span data-stu-id="362a2-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="362a2-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="362a2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="362a2-120">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="362a2-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="362a2-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="362a2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="362a2-122">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="362a2-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="362a2-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="362a2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="362a2-124"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="362a2-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="362a2-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="362a2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="362a2-126">Estruturas de vídeo do Direct3D</span><span class="sxs-lookup"><span data-stu-id="362a2-126">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="362a2-127">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="362a2-127">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




