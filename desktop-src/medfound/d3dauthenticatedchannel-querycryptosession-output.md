---
description: Contém a resposta a uma \_ consulta D3DAUTHENTICATEDQUERY CRYPTOSESSION.
ms.assetid: df9d9b41-8188-4597-9e83-d14065eb7fc7
title: Estrutura de D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: fb4e6ccad999f183e71f0f57d64544a70cef5534
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811414"
---
# <a name="d3dauthenticatedchannel_querycryptosession_output-structure"></a><span data-ttu-id="f8085-103">Estrutura de saída do D3DAUTHENTICATEDCHANNEL \_ QUERYCRYPTOSESSION \_</span><span class="sxs-lookup"><span data-stu-id="f8085-103">D3DAUTHENTICATEDCHANNEL\_QUERYCRYPTOSESSION\_OUTPUT structure</span></span>

<span data-ttu-id="f8085-104">Contém a resposta a uma consulta [**D3DAUTHENTICATEDQUERY \_ CRYPTOSESSION**](d3dauthenticatedquery-cryptosession.md) .</span><span class="sxs-lookup"><span data-stu-id="f8085-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_CRYPTOSESSION**](d3dauthenticatedquery-cryptosession.md) query.</span></span>

<span data-ttu-id="f8085-105">Para enviar essa consulta, chame [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="f8085-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="f8085-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f8085-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  HANDLE                               DXVA2DecodeHandle;
  HANDLE                               CryptoSessionHandle;
  HANDLE                               DeviceHandle;
} D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="f8085-107">Membros</span><span class="sxs-lookup"><span data-stu-id="f8085-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="f8085-108">**Saída**</span><span class="sxs-lookup"><span data-stu-id="f8085-108">**Output**</span></span>
</dt> <dd>

<span data-ttu-id="f8085-109">Uma estrutura de [**\_ \_ saída de consulta D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) que contém um Message Authentication Code (Mac) e outros dados.</span><span class="sxs-lookup"><span data-stu-id="f8085-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="f8085-110">**DXVA2DecodeHandle**</span><span class="sxs-lookup"><span data-stu-id="f8085-110">**DXVA2DecodeHandle**</span></span>
</dt> <dd>

<span data-ttu-id="f8085-111">Um identificador para um dispositivo de decodificador DXVA-2 (Video Acceleration) do DirectX.</span><span class="sxs-lookup"><span data-stu-id="f8085-111">A handle to a DirectX Video Acceleration 2 (DXVA-2) decoder device.</span></span>

</dd> <dt>

<span data-ttu-id="f8085-112">**CryptoSessionHandle**</span><span class="sxs-lookup"><span data-stu-id="f8085-112">**CryptoSessionHandle**</span></span>
</dt> <dd>

<span data-ttu-id="f8085-113">Um identificador para a sessão criptográfica associada ao dispositivo decodificador.</span><span class="sxs-lookup"><span data-stu-id="f8085-113">A handle to the cryptographic session that is associated with the decoder device.</span></span>

</dd> <dt>

<span data-ttu-id="f8085-114">**DeviceHandle**</span><span class="sxs-lookup"><span data-stu-id="f8085-114">**DeviceHandle**</span></span>
</dt> <dd>

<span data-ttu-id="f8085-115">Um identificador para o dispositivo Direct3D que está associado ao dispositivo decodificador.</span><span class="sxs-lookup"><span data-stu-id="f8085-115">A handle to the Direct3D device that is associated with the decoder device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f8085-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8085-116">Requirements</span></span>



| <span data-ttu-id="f8085-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8085-117">Requirement</span></span> | <span data-ttu-id="f8085-118">Valor</span><span class="sxs-lookup"><span data-stu-id="f8085-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8085-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f8085-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f8085-120">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f8085-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f8085-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f8085-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f8085-122">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="f8085-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f8085-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f8085-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8085-124"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8085-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8085-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="f8085-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8085-126">Estruturas de vídeo do Direct3D</span><span class="sxs-lookup"><span data-stu-id="f8085-126">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="f8085-127">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="f8085-127">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




