---
description: Contém a resposta a uma \_ consulta D3DAUTHENTICATEDQUERY DEVICEHANDLE.
ms.assetid: f2e0ae6c-dc97-46f7-933f-6c14d83adf18
title: Estrutura de D3DAUTHENTICATEDCHANNEL_QUERYDEVICEHANDLE_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYDEVICEHANDLE_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b862523c54dc9f483e63cee525dc61c5f469602d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770574"
---
# <a name="d3dauthenticatedchannel_querydevicehandle_output-structure"></a><span data-ttu-id="28d4b-103">Estrutura de saída do D3DAUTHENTICATEDCHANNEL \_ QUERYDEVICEHANDLE \_</span><span class="sxs-lookup"><span data-stu-id="28d4b-103">D3DAUTHENTICATEDCHANNEL\_QUERYDEVICEHANDLE\_OUTPUT structure</span></span>

<span data-ttu-id="28d4b-104">Contém a resposta a uma consulta [**D3DAUTHENTICATEDQUERY \_ DEVICEHANDLE**](d3dauthenticatedquery-devicehandle.md) .</span><span class="sxs-lookup"><span data-stu-id="28d4b-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_DEVICEHANDLE**](d3dauthenticatedquery-devicehandle.md) query.</span></span>

<span data-ttu-id="28d4b-105">Para enviar essa consulta, chame [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="28d4b-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="28d4b-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="28d4b-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYDEVICEHANDLE_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  HANDLE                               DeviceHandle;
} D3DAUTHENTICATEDCHANNEL_QUERYDEVICEHANDLE_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="28d4b-107">Membros</span><span class="sxs-lookup"><span data-stu-id="28d4b-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="28d4b-108">**Saída**</span><span class="sxs-lookup"><span data-stu-id="28d4b-108">**Output**</span></span>
</dt> <dd>

<span data-ttu-id="28d4b-109">Uma estrutura de [**\_ \_ saída de consulta D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) que contém um Message Authentication Code (Mac) e outros dados.</span><span class="sxs-lookup"><span data-stu-id="28d4b-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="28d4b-110">**DeviceHandle**</span><span class="sxs-lookup"><span data-stu-id="28d4b-110">**DeviceHandle**</span></span>
</dt> <dd>

<span data-ttu-id="28d4b-111">Um identificador para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="28d4b-111">A handle to the device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="28d4b-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28d4b-112">Requirements</span></span>



| <span data-ttu-id="28d4b-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="28d4b-113">Requirement</span></span> | <span data-ttu-id="28d4b-114">Valor</span><span class="sxs-lookup"><span data-stu-id="28d4b-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="28d4b-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="28d4b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="28d4b-116">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="28d4b-116">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="28d4b-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="28d4b-117">Minimum supported server</span></span><br/> | <span data-ttu-id="28d4b-118">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="28d4b-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="28d4b-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="28d4b-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="28d4b-120"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="28d4b-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28d4b-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="28d4b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28d4b-122">Estruturas de vídeo do Direct3D</span><span class="sxs-lookup"><span data-stu-id="28d4b-122">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="28d4b-123">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="28d4b-123">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




