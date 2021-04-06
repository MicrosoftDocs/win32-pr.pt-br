---
description: Contém a resposta a uma \_ consulta D3DAUTHENTICATEDQUERY ENCRYPTIONWHENACCESSIBLEGUID.
ms.assetid: afe73f8e-3304-470c-a37a-17b6c767b2c0
title: Estrutura de D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 8fa46095c5075b0a36ed691978b73de1e7b8cade
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826732"
---
# <a name="d3dauthenticatedchannel_queryevictionencryptionguid_output-structure"></a><span data-ttu-id="5ef13-103">Estrutura de saída do D3DAUTHENTICATEDCHANNEL \_ QUERYEVICTIONENCRYPTIONGUID \_</span><span class="sxs-lookup"><span data-stu-id="5ef13-103">D3DAUTHENTICATEDCHANNEL\_QUERYEVICTIONENCRYPTIONGUID\_OUTPUT structure</span></span>

<span data-ttu-id="5ef13-104">Contém a resposta a uma consulta [**D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUID**](d3dauthenticatedquery-encryptionwhenaccessibleguid.md) .</span><span class="sxs-lookup"><span data-stu-id="5ef13-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_ENCRYPTIONWHENACCESSIBLEGUID**](d3dauthenticatedquery-encryptionwhenaccessibleguid.md) query.</span></span>

<span data-ttu-id="5ef13-105">Para enviar essa consulta, chame [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="5ef13-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="5ef13-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5ef13-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_OUTPUT {
  Output D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT;
  UINT   EncryptionGuidIndex;
  GUID   EncryptionGuid;
} D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="5ef13-107">Membros</span><span class="sxs-lookup"><span data-stu-id="5ef13-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="5ef13-108">**\_Saída de consulta D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="5ef13-108">**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**</span></span>
</dt> <dd>

<span data-ttu-id="5ef13-109">Uma estrutura de [**\_ \_ saída de consulta D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) que contém um Message Authentication Code (Mac) e outros dados.</span><span class="sxs-lookup"><span data-stu-id="5ef13-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="5ef13-110">**EncryptionGuidIndex**</span><span class="sxs-lookup"><span data-stu-id="5ef13-110">**EncryptionGuidIndex**</span></span>
</dt> <dd>

<span data-ttu-id="5ef13-111">O índice do GUID de criptografia.</span><span class="sxs-lookup"><span data-stu-id="5ef13-111">The index of the encryption GUID.</span></span>

</dd> <dt>

<span data-ttu-id="5ef13-112">**EncryptionGuid**</span><span class="sxs-lookup"><span data-stu-id="5ef13-112">**EncryptionGuid**</span></span>
</dt> <dd>

<span data-ttu-id="5ef13-113">Um GUID que especifica um tipo de criptografia com suporte.</span><span class="sxs-lookup"><span data-stu-id="5ef13-113">A GUID that specifies a supported encryption type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5ef13-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ef13-114">Requirements</span></span>



| <span data-ttu-id="5ef13-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ef13-115">Requirement</span></span> | <span data-ttu-id="5ef13-116">Valor</span><span class="sxs-lookup"><span data-stu-id="5ef13-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ef13-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5ef13-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5ef13-118">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="5ef13-118">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="5ef13-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5ef13-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5ef13-120">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="5ef13-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5ef13-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5ef13-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ef13-122"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ef13-122"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ef13-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="5ef13-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ef13-124">Estruturas de vídeo do Direct3D</span><span class="sxs-lookup"><span data-stu-id="5ef13-124">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="5ef13-125">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="5ef13-125">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




