---
description: Contém dados de entrada para uma \_ consulta D3DAUTHENTICATEDQUERY CRYPTOSESSION.
ms.assetid: 3a4dead8-fe23-41b4-a167-e0430d09248a
title: Estrutura de D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_INPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 76b9d09bcb03dbf3742d551c253d3f4982215757
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296154"
---
# <a name="d3dauthenticatedchannel_querycryptosession_input-structure"></a><span data-ttu-id="d1f86-103">Estrutura de entrada do D3DAUTHENTICATEDCHANNEL \_ QUERYCRYPTOSESSION \_</span><span class="sxs-lookup"><span data-stu-id="d1f86-103">D3DAUTHENTICATEDCHANNEL\_QUERYCRYPTOSESSION\_INPUT structure</span></span>

<span data-ttu-id="d1f86-104">Contém dados de entrada para uma consulta [**D3DAUTHENTICATEDQUERY \_ CRYPTOSESSION**](d3dauthenticatedquery-cryptosession.md) .</span><span class="sxs-lookup"><span data-stu-id="d1f86-104">Contains input data for a [**D3DAUTHENTICATEDQUERY\_CRYPTOSESSION**](d3dauthenticatedquery-cryptosession.md) query.</span></span>

<span data-ttu-id="d1f86-105">Para enviar essa consulta, chame [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="d1f86-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="d1f86-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d1f86-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_INPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_INPUT Input;
  HANDLE                              DXVA2DecodeHandle;
} D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_INPUT;
```



## <a name="members"></a><span data-ttu-id="d1f86-107">Membros</span><span class="sxs-lookup"><span data-stu-id="d1f86-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="d1f86-108">**Entrada**</span><span class="sxs-lookup"><span data-stu-id="d1f86-108">**Input**</span></span>
</dt> <dd>

<span data-ttu-id="d1f86-109">Uma estrutura de [**\_ \_ entrada de consulta D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-input.md) que contém o GUID para a consulta e outros dados.</span><span class="sxs-lookup"><span data-stu-id="d1f86-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**](d3dauthenticatedchannel-query-input.md) structure that contains the GUID for the query and other data.</span></span>

</dd> <dt>

<span data-ttu-id="d1f86-110">**DXVA2DecodeHandle**</span><span class="sxs-lookup"><span data-stu-id="d1f86-110">**DXVA2DecodeHandle**</span></span>
</dt> <dd>

<span data-ttu-id="d1f86-111">Um identificador para um dispositivo de decodificador DXVA-2 (Video Acceleration) do DirectX.</span><span class="sxs-lookup"><span data-stu-id="d1f86-111">A handle to a DirectX Video Acceleration 2 (DXVA-2) decoder device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d1f86-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1f86-112">Requirements</span></span>



| <span data-ttu-id="d1f86-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1f86-113">Requirement</span></span> | <span data-ttu-id="d1f86-114">Valor</span><span class="sxs-lookup"><span data-stu-id="d1f86-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1f86-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d1f86-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d1f86-116">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d1f86-116">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d1f86-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d1f86-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d1f86-118">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="d1f86-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d1f86-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d1f86-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1f86-120"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1f86-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1f86-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="d1f86-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1f86-122">Estruturas de vídeo do Direct3D</span><span class="sxs-lookup"><span data-stu-id="d1f86-122">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="d1f86-123">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="d1f86-123">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




