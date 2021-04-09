---
description: Contém a resposta a uma \_ consulta outputid D3DAUTHENTICATEDQUERY.
ms.assetid: 4dfd1d65-b203-456a-bc9b-527906bcf87e
title: Estrutura de D3DAUTHENTICATEDCHANNEL_QUERYROUTPUTID_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 26686126fd2a5cb942c88ea485f753d2432499dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010317"
---
# <a name="d3dauthenticatedchannel_queryroutputid_output-structure"></a><span data-ttu-id="889f1-103">Estrutura de saída do D3DAUTHENTICATEDCHANNEL \_ QUERYROUTPUTID \_</span><span class="sxs-lookup"><span data-stu-id="889f1-103">D3DAUTHENTICATEDCHANNEL\_QUERYROUTPUTID\_OUTPUT structure</span></span>

<span data-ttu-id="889f1-104">Contém a resposta a uma [**consulta \_ outputid D3DAUTHENTICATEDQUERY**](d3dauthenticatedquery-outputid.md) .</span><span class="sxs-lookup"><span data-stu-id="889f1-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_OUTPUTID**](d3dauthenticatedquery-outputid.md) query.</span></span>

<span data-ttu-id="889f1-105">Para enviar essa consulta, chame [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="889f1-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="889f1-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="889f1-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_OUTPUT {
  Output D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT;
  HANDLE DeviceHandle;
  HANDLE CryptoSessionHandle;
  UINT   OutputIDIndex;
  UINT64 OutputID;
} D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="889f1-107">Membros</span><span class="sxs-lookup"><span data-stu-id="889f1-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="889f1-108">**\_Saída de consulta D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="889f1-108">**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**</span></span>
</dt> <dd>

<span data-ttu-id="889f1-109">Uma estrutura de [**\_ \_ saída de consulta D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) que contém um Message Authentication Code (Mac) e outros dados.</span><span class="sxs-lookup"><span data-stu-id="889f1-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="889f1-110">**DeviceHandle**</span><span class="sxs-lookup"><span data-stu-id="889f1-110">**DeviceHandle**</span></span>
</dt> <dd>

<span data-ttu-id="889f1-111">Um identificador para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="889f1-111">A handle to the device.</span></span>

</dd> <dt>

<span data-ttu-id="889f1-112">**CryptoSessionHandle**</span><span class="sxs-lookup"><span data-stu-id="889f1-112">**CryptoSessionHandle**</span></span>
</dt> <dd>

<span data-ttu-id="889f1-113">Um identificador para a sessão de criptografia.</span><span class="sxs-lookup"><span data-stu-id="889f1-113">A handle to the cryptographic session.</span></span>

</dd> <dt>

<span data-ttu-id="889f1-114">**OutputIDIndex**</span><span class="sxs-lookup"><span data-stu-id="889f1-114">**OutputIDIndex**</span></span>
</dt> <dd>

<span data-ttu-id="889f1-115">O índice da ID de saída fornecida no membro **outputid** .</span><span class="sxs-lookup"><span data-stu-id="889f1-115">The index of the output ID given in the **OutputID** member.</span></span>

</dd> <dt>

<span data-ttu-id="889f1-116">**Outputid**</span><span class="sxs-lookup"><span data-stu-id="889f1-116">**OutputID**</span></span>
</dt> <dd>

<span data-ttu-id="889f1-117">Uma ID de saída associada ao dispositivo especificado e à sessão criptográfica.</span><span class="sxs-lookup"><span data-stu-id="889f1-117">An output ID that is associated with the specified device and cryptographic session.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="889f1-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="889f1-118">Requirements</span></span>



| <span data-ttu-id="889f1-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="889f1-119">Requirement</span></span> | <span data-ttu-id="889f1-120">Valor</span><span class="sxs-lookup"><span data-stu-id="889f1-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="889f1-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="889f1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="889f1-122">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="889f1-122">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="889f1-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="889f1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="889f1-124">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="889f1-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="889f1-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="889f1-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="889f1-126"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="889f1-126"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="889f1-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="889f1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="889f1-128">Estruturas de vídeo do Direct3D</span><span class="sxs-lookup"><span data-stu-id="889f1-128">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="889f1-129">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="889f1-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




