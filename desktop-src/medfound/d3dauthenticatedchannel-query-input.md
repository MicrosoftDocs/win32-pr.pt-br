---
description: 'Contém dados de entrada para o método IDirect3DAuthenticatedChannel9:: Query.'
ms.assetid: 6a484652-8da2-4074-96b2-6fe49f4d4200
title: Estrutura de D3DAUTHENTICATEDCHANNEL_QUERY_INPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERY_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: a0bec356b20569b5638848407eff27e930ef76b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164203"
---
# <a name="d3dauthenticatedchannel_query_input-structure"></a><span data-ttu-id="92741-103">Estrutura de entrada de \_ consulta D3DAUTHENTICATEDCHANNEL \_</span><span class="sxs-lookup"><span data-stu-id="92741-103">D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT structure</span></span>

<span data-ttu-id="92741-104">Contém dados de entrada para o método [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) .</span><span class="sxs-lookup"><span data-stu-id="92741-104">Contains input data for the [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="92741-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="92741-105">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERY_INPUT {
  GUID           QueryType;
  hChannel       HANDLE;
  SequenceNumber UINT;
} D3DAUTHENTICATEDCHANNEL_QUERY_INPUT;
```



## <a name="members"></a><span data-ttu-id="92741-106">Membros</span><span class="sxs-lookup"><span data-stu-id="92741-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="92741-107">**QueryType**</span><span class="sxs-lookup"><span data-stu-id="92741-107">**QueryType**</span></span>
</dt> <dd>

<span data-ttu-id="92741-108">Um GUID que especifica a consulta.</span><span class="sxs-lookup"><span data-stu-id="92741-108">A GUID that specifies the query.</span></span> <span data-ttu-id="92741-109">Para obter uma lista de valores, consulte [proteção de conteúdo consultas](content-protection-queries.md).</span><span class="sxs-lookup"><span data-stu-id="92741-109">For a list of values, see [Content Protection Queries](content-protection-queries.md).</span></span>

</dd> <dt>

<span data-ttu-id="92741-110">**PROCESSAMENTO**</span><span class="sxs-lookup"><span data-stu-id="92741-110">**HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="92741-111">Um identificador para o canal autenticado.</span><span class="sxs-lookup"><span data-stu-id="92741-111">A handle to the authenticated channel.</span></span> <span data-ttu-id="92741-112">Para obter o identificador, chame [**IDirect3DDevice9Video:: CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel).</span><span class="sxs-lookup"><span data-stu-id="92741-112">To get the handle, call [**IDirect3DDevice9Video::CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel).</span></span>

</dd> <dt>

<span data-ttu-id="92741-113">**UINT**</span><span class="sxs-lookup"><span data-stu-id="92741-113">**UINT**</span></span>
</dt> <dd>

<span data-ttu-id="92741-114">O número de sequência da consulta.</span><span class="sxs-lookup"><span data-stu-id="92741-114">The query sequence number.</span></span> <span data-ttu-id="92741-115">No início da sessão, gere um número aleatório de 32 bits de segurança criptograficamente seguro para usar como o número de sequência inicial.</span><span class="sxs-lookup"><span data-stu-id="92741-115">At the start of the session, generate a cryptographically secure 32-bit random number to use as the starting sequence number.</span></span> <span data-ttu-id="92741-116">Para cada consulta, aumente o número de sequência em 1.</span><span class="sxs-lookup"><span data-stu-id="92741-116">For each query, increment the sequence number by 1.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="92741-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92741-117">Requirements</span></span>



| <span data-ttu-id="92741-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="92741-118">Requirement</span></span> | <span data-ttu-id="92741-119">Valor</span><span class="sxs-lookup"><span data-stu-id="92741-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="92741-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="92741-120">Minimum supported client</span></span><br/> | <span data-ttu-id="92741-121">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="92741-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="92741-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="92741-122">Minimum supported server</span></span><br/> | <span data-ttu-id="92741-123">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="92741-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="92741-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="92741-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="92741-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="92741-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92741-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="92741-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92741-127">Estruturas de vídeo do Direct3D</span><span class="sxs-lookup"><span data-stu-id="92741-127">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="92741-128">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="92741-128">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




