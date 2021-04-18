---
title: Estrutura de WM_INDIVIDUALIZE_STATUS (Drmexternals. h)
description: A \_ estrutura de status de individualização do WM \_ registra o status do processo de individualização.
ms.assetid: 3779ed6f-c133-4a9d-b60c-ef8c41fcc4af
keywords:
- Formato de mídia do Windows de estrutura de WM_INDIVIDUALIZE_STATUS
topic_type:
- apiref
api_name:
- WM_INDIVIDUALIZE_STATUS
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddec51fbdfecd407a68b3e168a82af449decce6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105814095"
---
# <a name="wm_individualize_status-structure-drmexternalsh"></a><span data-ttu-id="51bf9-104">Estrutura de WM_INDIVIDUALIZE_STATUS (Drmexternals. h)</span><span class="sxs-lookup"><span data-stu-id="51bf9-104">WM_INDIVIDUALIZE_STATUS structure (Drmexternals.h)</span></span>

<span data-ttu-id="51bf9-105">A estrutura de **\_ \_ status de individualização do WM** registra o status do processo de [*individualização*](wmformat-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="51bf9-105">The **WM\_INDIVIDUALIZE\_STATUS** structure records the status of the [*individualization*](wmformat-glossary.md) process.</span></span>

## <a name="syntax"></a><span data-ttu-id="51bf9-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="51bf9-106">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="51bf9-107">Membros</span><span class="sxs-lookup"><span data-stu-id="51bf9-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="51bf9-108">**h**</span><span class="sxs-lookup"><span data-stu-id="51bf9-108">**hr**</span></span>
</dt> <dd>

<span data-ttu-id="51bf9-109">Código de retorno **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="51bf9-109">**HRESULT** return code.</span></span>

</dd> <dt>

<span data-ttu-id="51bf9-110">**enIndiStatus**</span><span class="sxs-lookup"><span data-stu-id="51bf9-110">**enIndiStatus**</span></span>
</dt> <dd>

<span data-ttu-id="51bf9-111">Valor do tipo de enumeração de [**\_ \_ status de individualização de DRM**](drm-individualization-status.md) .</span><span class="sxs-lookup"><span data-stu-id="51bf9-111">Value from the [**DRM\_INDIVIDUALIZATION\_STATUS**](drm-individualization-status.md) enumeration type.</span></span>

</dd> <dt>

<span data-ttu-id="51bf9-112">**pszIndiRespUrl**</span><span class="sxs-lookup"><span data-stu-id="51bf9-112">**pszIndiRespUrl**</span></span>
</dt> <dd>

<span data-ttu-id="51bf9-113">Ponteiro para uma cadeia de caracteres terminada em nulo que contém a URL de resposta de individualização.</span><span class="sxs-lookup"><span data-stu-id="51bf9-113">Pointer to a null-terminated string containing the individualization response URL.</span></span>

</dd> <dt>

<span data-ttu-id="51bf9-114">**dwHTTPRequest**</span><span class="sxs-lookup"><span data-stu-id="51bf9-114">**dwHTTPRequest**</span></span>
</dt> <dd>

<span data-ttu-id="51bf9-115">**DWORD** que indica o número de viagens de ida e volta http para o serviço de individualização que foram concluídas.</span><span class="sxs-lookup"><span data-stu-id="51bf9-115">**DWORD** that indicates the number of HTTP round trips to the individualization service that have been completed..</span></span>

</dd> <dt>

<span data-ttu-id="51bf9-116">**enHTTPStatus**</span><span class="sxs-lookup"><span data-stu-id="51bf9-116">**enHTTPStatus**</span></span>
</dt> <dd>

<span data-ttu-id="51bf9-117">Valor do tipo de enumeração de [**\_ \_ status http DRM**](drm-http-status.md) .</span><span class="sxs-lookup"><span data-stu-id="51bf9-117">Value from the [**DRM\_HTTP\_STATUS**](drm-http-status.md) enumeration type.</span></span>

</dd> <dt>

<span data-ttu-id="51bf9-118">**dwHTTPReadProgress**</span><span class="sxs-lookup"><span data-stu-id="51bf9-118">**dwHTTPReadProgress**</span></span>
</dt> <dd>

<span data-ttu-id="51bf9-119">**DWORD** que contém o número de bytes baixados até agora..</span><span class="sxs-lookup"><span data-stu-id="51bf9-119">**DWORD** containing the number of bytes downloaded until now..</span></span>

</dd> <dt>

<span data-ttu-id="51bf9-120">**dwHTTPReadTotal**</span><span class="sxs-lookup"><span data-stu-id="51bf9-120">**dwHTTPReadTotal**</span></span>
</dt> <dd>

<span data-ttu-id="51bf9-121">**DWORD** que contém o número total de bytes a serem baixados.</span><span class="sxs-lookup"><span data-stu-id="51bf9-121">**DWORD** containing the total number of bytes to be downloaded.</span></span> <span data-ttu-id="51bf9-122">Use esse valor e **dwHTTPReadProgress** para exibir uma interface do usuário que indica a quantidade de download concluído e quanto resta ser feito.</span><span class="sxs-lookup"><span data-stu-id="51bf9-122">Use this value and **dwHTTPReadProgress** to display a user interface indicating how much of the download has completed and how much remains to be done.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="51bf9-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="51bf9-123">Remarks</span></span>

<span data-ttu-id="51bf9-124">Essa estrutura é preenchida pelos componentes de tempo de execução do DRM e é enviada para aplicativos no *parâmetro época* do método Applications [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) quando o evento é igual a WMT \_ individualize.</span><span class="sxs-lookup"><span data-stu-id="51bf9-124">This structure is filled in by the DRM run-time components and is sent to applications in the *pValue* parameter of the applications [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) method when the event equals WMT\_INDIVIDUALIZE.</span></span> <span data-ttu-id="51bf9-125">O aplicativo recebe esse evento várias vezes durante o processo de download.</span><span class="sxs-lookup"><span data-stu-id="51bf9-125">The application receives this event multiple times during the download process.</span></span>

## <a name="requirements"></a><span data-ttu-id="51bf9-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51bf9-126">Requirements</span></span>



| <span data-ttu-id="51bf9-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="51bf9-127">Requirement</span></span> | <span data-ttu-id="51bf9-128">Valor</span><span class="sxs-lookup"><span data-stu-id="51bf9-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="51bf9-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="51bf9-129">Minimum supported client</span></span><br/> | <span data-ttu-id="51bf9-130">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="51bf9-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="51bf9-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="51bf9-131">Minimum supported server</span></span><br/> | <span data-ttu-id="51bf9-132">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="51bf9-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="51bf9-133">Versão</span><span class="sxs-lookup"><span data-stu-id="51bf9-133">Version</span></span><br/>                  | <span data-ttu-id="51bf9-134">SDK do Windows Media Format 7 ou versões posteriores do SDK</span><span class="sxs-lookup"><span data-stu-id="51bf9-134">Windows Media Format 7 SDK, or later versions of the SDK</span></span><br/>                       |
| <span data-ttu-id="51bf9-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="51bf9-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="51bf9-136"><dt>Drmexternals. h</dt></span><span class="sxs-lookup"><span data-stu-id="51bf9-136"><dt>Drmexternals.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51bf9-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="51bf9-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51bf9-138">**\_status do http DRM \_**</span><span class="sxs-lookup"><span data-stu-id="51bf9-138">**DRM\_HTTP\_STATUS**</span></span>](drm-http-status.md)
</dt> <dt>

[<span data-ttu-id="51bf9-139">**Estruturas**</span><span class="sxs-lookup"><span data-stu-id="51bf9-139">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





