---
title: Estrutura de WM_INDIVIDUALIZE_STATUS (wmdrmsdk. h)
description: A \_ estrutura de status de individualização do WM \_ contém informações sobre um processo de individualização pendente.
ms.assetid: af7e8758-489b-461f-b241-d7e40c8d61da
keywords:
- Formato de mídia do Windows de estrutura de WM_INDIVIDUALIZE_STATUS
topic_type:
- apiref
api_name:
- WM_INDIVIDUALIZE_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ef7617fe6dcddf3397ab1a123132e843f0b1461
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788997"
---
# <a name="wm_individualize_status-structure-wmdrmsdkh"></a><span data-ttu-id="84568-104">Estrutura de WM_INDIVIDUALIZE_STATUS (wmdrmsdk. h)</span><span class="sxs-lookup"><span data-stu-id="84568-104">WM_INDIVIDUALIZE_STATUS structure (Wmdrmsdk.h)</span></span>

<span data-ttu-id="84568-105">A estrutura de **\_ \_ status de individualização do WM** contém informações sobre um processo de individualização pendente.</span><span class="sxs-lookup"><span data-stu-id="84568-105">The **WM\_INDIVIDUALIZE\_STATUS** structure holds information about a pending individualization process.</span></span>

## <a name="syntax"></a><span data-ttu-id="84568-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="84568-106">Syntax</span></span>


```C++
typedef struct _WMIndividualizeStatus {
  HRESULT                      hr;
  DRM_INDIVIDUALIZATION_STATUS enIndiStatus;
  LPSTR                        pszIndiRespUrl;
  DWORD                        dwHTTPRequest;
  DRM_HTTP_STATUS              enHTTPStatus;
  DWORD                        dwHTTPReadProgress;
  DWORD                        dwHTTPReadTotal;
} WM_INDIVIDUALIZE_STATUS;
```



## <a name="members"></a><span data-ttu-id="84568-107">Membros</span><span class="sxs-lookup"><span data-stu-id="84568-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="84568-108">**h**</span><span class="sxs-lookup"><span data-stu-id="84568-108">**hr**</span></span>
</dt> <dd>

<span data-ttu-id="84568-109">Código de retorno **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="84568-109">**HRESULT** return code.</span></span>

</dd> <dt>

<span data-ttu-id="84568-110">**enIndiStatus**</span><span class="sxs-lookup"><span data-stu-id="84568-110">**enIndiStatus**</span></span>
</dt> <dd>

<span data-ttu-id="84568-111">Valor do tipo de enumeração de [**\_ \_ status de individualização de DRM**](drmdrm-individualization-status.md) que indica o status atual do processo de individualização.</span><span class="sxs-lookup"><span data-stu-id="84568-111">Value from the [**DRM\_INDIVIDUALIZATION\_STATUS**](drmdrm-individualization-status.md) enumeration type that indicates the current status of the individualization process.</span></span>

</dd> <dt>

<span data-ttu-id="84568-112">**pszIndiRespUrl**</span><span class="sxs-lookup"><span data-stu-id="84568-112">**pszIndiRespUrl**</span></span>
</dt> <dd>

<span data-ttu-id="84568-113">Ponteiro para uma cadeia de caracteres terminada em nulo que contém a URL de resposta de individualização.</span><span class="sxs-lookup"><span data-stu-id="84568-113">Pointer to a null-terminated string containing the individualization response URL.</span></span>

</dd> <dt>

<span data-ttu-id="84568-114">**dwHTTPRequest**</span><span class="sxs-lookup"><span data-stu-id="84568-114">**dwHTTPRequest**</span></span>
</dt> <dd>

<span data-ttu-id="84568-115">O número de viagens de ida e volta HTTP para o serviço de individualização que foram concluídas.</span><span class="sxs-lookup"><span data-stu-id="84568-115">The number of HTTP round trips to the individualization service that have been completed.</span></span>

</dd> <dt>

<span data-ttu-id="84568-116">**enHTTPStatus**</span><span class="sxs-lookup"><span data-stu-id="84568-116">**enHTTPStatus**</span></span>
</dt> <dd>

<span data-ttu-id="84568-117">Valor do tipo de enumeração de [**\_ \_ status http DRM**](drmdrm-http-status.md) .</span><span class="sxs-lookup"><span data-stu-id="84568-117">Value from the [**DRM\_HTTP\_STATUS**](drmdrm-http-status.md) enumeration type.</span></span>

</dd> <dt>

<span data-ttu-id="84568-118">**dwHTTPReadProgress**</span><span class="sxs-lookup"><span data-stu-id="84568-118">**dwHTTPReadProgress**</span></span>
</dt> <dd>

<span data-ttu-id="84568-119">O número de bytes baixados.</span><span class="sxs-lookup"><span data-stu-id="84568-119">The number of bytes downloaded.</span></span>

</dd> <dt>

<span data-ttu-id="84568-120">**dwHTTPReadTotal**</span><span class="sxs-lookup"><span data-stu-id="84568-120">**dwHTTPReadTotal**</span></span>
</dt> <dd>

<span data-ttu-id="84568-121">O número total de bytes a serem baixados.</span><span class="sxs-lookup"><span data-stu-id="84568-121">The total number of bytes to be downloaded.</span></span> <span data-ttu-id="84568-122">Você pode usar esse valor e **dwHTTPReadProgress** para exibir uma interface do usuário que indica a quantidade de download concluída e quanto resta.</span><span class="sxs-lookup"><span data-stu-id="84568-122">You can use this value and **dwHTTPReadProgress** to display a user interface indicating how much of the download has completed and how much remains to be done.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="84568-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="84568-123">Remarks</span></span>

<span data-ttu-id="84568-124">Essa estrutura é recebida quando você chama o método [**IWMDRMIndividualizationStatus:: GetStatus**](iwmdrmindividualizationstatus-getstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="84568-124">This structure is received when you call the [**IWMDRMIndividualizationStatus::GetStatus**](iwmdrmindividualizationstatus-getstatus.md) method.</span></span> <span data-ttu-id="84568-125">Ele contém o status do processo de individualização pendente no momento da chamada.</span><span class="sxs-lookup"><span data-stu-id="84568-125">It contains the status of the pending individualization process at the time of the call.</span></span>

## <a name="requirements"></a><span data-ttu-id="84568-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84568-126">Requirements</span></span>



| <span data-ttu-id="84568-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="84568-127">Requirement</span></span> | <span data-ttu-id="84568-128">Valor</span><span class="sxs-lookup"><span data-stu-id="84568-128">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="84568-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="84568-129">Header</span></span><br/> | <dl> <span data-ttu-id="84568-130"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="84568-130"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84568-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="84568-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84568-132">**Estruturas**</span><span class="sxs-lookup"><span data-stu-id="84568-132">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





