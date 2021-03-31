---
description: Contém dados de entrada para uma \_ consulta D3DAUTHENTICATEDQUERY OUTPUTIDCOUNT.
ms.assetid: cc68b39f-4645-46a6-a752-549b070cf23b
title: Estrutura de D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_INPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 93f58bcd05efb8c173986186d631c713195d8363
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089762"
---
# <a name="d3dauthenticatedchannel_queryoutputidcount_input-structure"></a><span data-ttu-id="f3b0a-103">Estrutura de entrada do D3DAUTHENTICATEDCHANNEL \_ QUERYOUTPUTIDCOUNT \_</span><span class="sxs-lookup"><span data-stu-id="f3b0a-103">D3DAUTHENTICATEDCHANNEL\_QUERYOUTPUTIDCOUNT\_INPUT structure</span></span>

<span data-ttu-id="f3b0a-104">Contém dados de entrada para uma consulta [**D3DAUTHENTICATEDQUERY \_ OUTPUTIDCOUNT**](d3dauthenticatedquery-outputidcount.md) .</span><span class="sxs-lookup"><span data-stu-id="f3b0a-104">Contains input data for a [**D3DAUTHENTICATEDQUERY\_OUTPUTIDCOUNT**](d3dauthenticatedquery-outputidcount.md) query.</span></span>

<span data-ttu-id="f3b0a-105">Para enviar essa consulta, chame [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="f3b0a-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="f3b0a-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f3b0a-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_INPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_INPUT Input;
  HANDLE                              DeviceHandle;
  HANDLE                              CryptoSessionHandle;
} D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_INPUT;
```



## <a name="members"></a><span data-ttu-id="f3b0a-107">Membros</span><span class="sxs-lookup"><span data-stu-id="f3b0a-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="f3b0a-108">**Entrada**</span><span class="sxs-lookup"><span data-stu-id="f3b0a-108">**Input**</span></span>
</dt> <dd>

<span data-ttu-id="f3b0a-109">Uma estrutura de [**\_ \_ entrada de consulta D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-input.md) que contém o GUID para a consulta e outros dados.</span><span class="sxs-lookup"><span data-stu-id="f3b0a-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**](d3dauthenticatedchannel-query-input.md) structure that contains the GUID for the query and other data.</span></span>

</dd> <dt>

<span data-ttu-id="f3b0a-110">**DeviceHandle**</span><span class="sxs-lookup"><span data-stu-id="f3b0a-110">**DeviceHandle**</span></span>
</dt> <dd>

<span data-ttu-id="f3b0a-111">Um identificador para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f3b0a-111">A handle to the device.</span></span>

</dd> <dt>

<span data-ttu-id="f3b0a-112">**CryptoSessionHandle**</span><span class="sxs-lookup"><span data-stu-id="f3b0a-112">**CryptoSessionHandle**</span></span>
</dt> <dd>

<span data-ttu-id="f3b0a-113">Um identificador para a sessão de criptografia.</span><span class="sxs-lookup"><span data-stu-id="f3b0a-113">A handle to the cryptographic session.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f3b0a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3b0a-114">Requirements</span></span>



| <span data-ttu-id="f3b0a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3b0a-115">Requirement</span></span> | <span data-ttu-id="f3b0a-116">Valor</span><span class="sxs-lookup"><span data-stu-id="f3b0a-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f3b0a-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f3b0a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f3b0a-118">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f3b0a-118">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f3b0a-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f3b0a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f3b0a-120">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="f3b0a-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f3b0a-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f3b0a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3b0a-122"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3b0a-122"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3b0a-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="f3b0a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3b0a-124">Estruturas de vídeo do Direct3D</span><span class="sxs-lookup"><span data-stu-id="f3b0a-124">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="f3b0a-125">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="f3b0a-125">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




