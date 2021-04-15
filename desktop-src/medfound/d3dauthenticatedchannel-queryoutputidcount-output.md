---
description: Contém a resposta a uma \_ consulta D3DAUTHENTICATEDQUERY OUTPUTIDCOUNT.
ms.assetid: 8b9fa0dc-bbe5-4382-8acc-59aeadfca825
title: Estrutura de D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 86a840de2b36b7089b31d15e8375c17a0610b77f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457217"
---
# <a name="d3dauthenticatedchannel_queryoutputidcount_output-structure"></a><span data-ttu-id="bf15b-103">Estrutura de saída do D3DAUTHENTICATEDCHANNEL \_ QUERYOUTPUTIDCOUNT \_</span><span class="sxs-lookup"><span data-stu-id="bf15b-103">D3DAUTHENTICATEDCHANNEL\_QUERYOUTPUTIDCOUNT\_OUTPUT structure</span></span>

<span data-ttu-id="bf15b-104">Contém a resposta a uma consulta [**D3DAUTHENTICATEDQUERY \_ OUTPUTIDCOUNT**](d3dauthenticatedquery-outputidcount.md) .</span><span class="sxs-lookup"><span data-stu-id="bf15b-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_OUTPUTIDCOUNT**](d3dauthenticatedquery-outputidcount.md) query.</span></span>

<span data-ttu-id="bf15b-105">Para enviar essa consulta, chame [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="bf15b-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="bf15b-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bf15b-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  HANDLE                               DeviceHandle;
  HANDLE                               CryptoSessionHandle;
  UINT                                 NumOutputIDs;
} D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="bf15b-107">Membros</span><span class="sxs-lookup"><span data-stu-id="bf15b-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="bf15b-108">**Saída**</span><span class="sxs-lookup"><span data-stu-id="bf15b-108">**Output**</span></span>
</dt> <dd>

<span data-ttu-id="bf15b-109">Uma estrutura de [**\_ \_ saída de consulta D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) que contém um Message Authentication Code (Mac) e outros dados.</span><span class="sxs-lookup"><span data-stu-id="bf15b-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="bf15b-110">**DeviceHandle**</span><span class="sxs-lookup"><span data-stu-id="bf15b-110">**DeviceHandle**</span></span>
</dt> <dd>

<span data-ttu-id="bf15b-111">Um identificador para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bf15b-111">A handle to the device.</span></span>

</dd> <dt>

<span data-ttu-id="bf15b-112">**CryptoSessionHandle**</span><span class="sxs-lookup"><span data-stu-id="bf15b-112">**CryptoSessionHandle**</span></span>
</dt> <dd>

<span data-ttu-id="bf15b-113">Um identificador para a sessão de criptografia.</span><span class="sxs-lookup"><span data-stu-id="bf15b-113">A handle to the cryptographic session.</span></span>

</dd> <dt>

<span data-ttu-id="bf15b-114">**NumOutputIDs**</span><span class="sxs-lookup"><span data-stu-id="bf15b-114">**NumOutputIDs**</span></span>
</dt> <dd>

<span data-ttu-id="bf15b-115">O número de IDs de saída associadas ao dispositivo especificado e à sessão criptográfica.</span><span class="sxs-lookup"><span data-stu-id="bf15b-115">The number of output IDs associated with the specified device and cryptographic session.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bf15b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf15b-116">Requirements</span></span>



| <span data-ttu-id="bf15b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf15b-117">Requirement</span></span> | <span data-ttu-id="bf15b-118">Valor</span><span class="sxs-lookup"><span data-stu-id="bf15b-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf15b-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bf15b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bf15b-120">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="bf15b-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="bf15b-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bf15b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bf15b-122">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="bf15b-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="bf15b-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bf15b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf15b-124"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf15b-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf15b-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="bf15b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf15b-126">Estruturas de vídeo do Direct3D</span><span class="sxs-lookup"><span data-stu-id="bf15b-126">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="bf15b-127">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="bf15b-127">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




