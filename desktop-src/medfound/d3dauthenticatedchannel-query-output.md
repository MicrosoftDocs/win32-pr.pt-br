---
description: 'Contém a resposta do método IDirect3DAuthenticatedChannel9:: Query.'
ms.assetid: b2783b8e-0436-419a-a93e-93dc1b87024d
title: Estrutura de D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 79fe02a483ade1ff60107287799624017496887b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089764"
---
# <a name="d3dauthenticatedchannel_query_output-structure"></a><span data-ttu-id="36755-103">Estrutura de saída da \_ consulta D3DAUTHENTICATEDCHANNEL \_</span><span class="sxs-lookup"><span data-stu-id="36755-103">D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT structure</span></span>

<span data-ttu-id="36755-104">Contém a resposta do método [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) .</span><span class="sxs-lookup"><span data-stu-id="36755-104">Contains the response from the [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="36755-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="36755-105">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT {
  D3D_OMAC       omac;
  GUID           QueryType;
  hChannel       HANDLE;
  SequenceNumber UINT;
  HRESULT        ReturnCode;
} D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="36755-106">Membros</span><span class="sxs-lookup"><span data-stu-id="36755-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="36755-107">**omac**</span><span class="sxs-lookup"><span data-stu-id="36755-107">**omac**</span></span>
</dt> <dd>

<span data-ttu-id="36755-108">Uma [**estrutura \_ OMAC do D3D**](d3d-omac.md) que contém um Message Authentication Code (Mac) dos dados.</span><span class="sxs-lookup"><span data-stu-id="36755-108">A [**D3D\_OMAC**](d3d-omac.md) structure that contains a Message Authentication Code (MAC) of the data.</span></span> <span data-ttu-id="36755-109">O driver usa o MAC de CBC One-key baseado em AES (OMAC) para calcular esse valor para o bloco de dados que aparece após esse membro da estrutura.</span><span class="sxs-lookup"><span data-stu-id="36755-109">The driver uses AES-based one-key CBC MAC (OMAC) to calculate this value for the block of data that appears after this structure member.</span></span>

</dd> <dt>

<span data-ttu-id="36755-110">**QueryType**</span><span class="sxs-lookup"><span data-stu-id="36755-110">**QueryType**</span></span>
</dt> <dd>

<span data-ttu-id="36755-111">Um GUID que especifica a consulta.</span><span class="sxs-lookup"><span data-stu-id="36755-111">A GUID that specifies the query.</span></span> <span data-ttu-id="36755-112">Para obter uma lista de valores, consulte [proteção de conteúdo consultas](content-protection-queries.md).</span><span class="sxs-lookup"><span data-stu-id="36755-112">For a list of values, see [Content Protection Queries](content-protection-queries.md).</span></span>

</dd> <dt>

<span data-ttu-id="36755-113">**PROCESSAMENTO**</span><span class="sxs-lookup"><span data-stu-id="36755-113">**HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="36755-114">Um identificador para o canal autenticado.</span><span class="sxs-lookup"><span data-stu-id="36755-114">A handle to the authenticated channel.</span></span>

</dd> <dt>

<span data-ttu-id="36755-115">**UINT**</span><span class="sxs-lookup"><span data-stu-id="36755-115">**UINT**</span></span>
</dt> <dd>

<span data-ttu-id="36755-116">O número de sequência da consulta.</span><span class="sxs-lookup"><span data-stu-id="36755-116">The query sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="36755-117">**ReturnCode**</span><span class="sxs-lookup"><span data-stu-id="36755-117">**ReturnCode**</span></span>
</dt> <dd>

<span data-ttu-id="36755-118">O código de resultado da consulta.</span><span class="sxs-lookup"><span data-stu-id="36755-118">The result code for the query.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="36755-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="36755-119">Remarks</span></span>

<span data-ttu-id="36755-120">Para os membros **QueryType**, **hChannel** e **SequenceNumber** , o driver usa os mesmos valores que o aplicativo forneceu na estrutura de [**\_ \_ entrada de consulta D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-input.md) .</span><span class="sxs-lookup"><span data-stu-id="36755-120">For the **QueryType**, **hChannel**, and **SequenceNumber** members, the driver uses in the same values that the application provided in the [**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**](d3dauthenticatedchannel-query-input.md) structure.</span></span> <span data-ttu-id="36755-121">O aplicativo deve verificar se esses valores correspondem.</span><span class="sxs-lookup"><span data-stu-id="36755-121">The application should verify that these values match.</span></span>

## <a name="requirements"></a><span data-ttu-id="36755-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36755-122">Requirements</span></span>



| <span data-ttu-id="36755-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="36755-123">Requirement</span></span> | <span data-ttu-id="36755-124">Valor</span><span class="sxs-lookup"><span data-stu-id="36755-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="36755-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="36755-125">Minimum supported client</span></span><br/> | <span data-ttu-id="36755-126">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="36755-126">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="36755-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="36755-127">Minimum supported server</span></span><br/> | <span data-ttu-id="36755-128">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="36755-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="36755-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="36755-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="36755-130"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="36755-130"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36755-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="36755-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36755-132">Estruturas de vídeo do Direct3D</span><span class="sxs-lookup"><span data-stu-id="36755-132">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="36755-133">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="36755-133">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




