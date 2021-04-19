---
description: Fornece ao sistema informações sobre um documento após a conclusão de uma operação de arrastar e soltar.
title: Função DlpNotifyPostDragDrop (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPreDragDrop
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 468255cee3c3fef44e44dd033b541e317db3d268
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495342"
---
# <a name="dlpnotifypostdragdrop-function"></a><span data-ttu-id="740ed-103">Função DlpNotifyPostDragDrop</span><span class="sxs-lookup"><span data-stu-id="740ed-103">DlpNotifyPostDragDrop function</span></span>

<span data-ttu-id="740ed-104">Fornece ao sistema informações sobre um documento após a conclusão de uma operação de arrastar e soltar.</span><span class="sxs-lookup"><span data-stu-id="740ed-104">Provides the system with information about a document after a drag drop operation is completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="740ed-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="740ed-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPostDragDrop(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);
```



## <a name="parameters"></a><span data-ttu-id="740ed-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="740ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="740ed-107">*DocumentInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="740ed-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="740ed-108">Um ponteiro para uma estrutura de [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) que contém informações sobre o documento associado à operação de arrastar e soltar.</span><span class="sxs-lookup"><span data-stu-id="740ed-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document associated with the drag drop operation.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="740ed-109">*OpStatus* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="740ed-109">*OpStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="740ed-110">Um ponteiro para uma estrutura de [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) que contém informações de status sobre o arrastar e soltar.</span><span class="sxs-lookup"><span data-stu-id="740ed-110">A pointer to a [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) structure containing status information about the drag drop.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="740ed-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="740ed-111">Return value</span></span>

<span data-ttu-id="740ed-112">Retornar void.</span><span class="sxs-lookup"><span data-stu-id="740ed-112">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="740ed-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="740ed-113">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="740ed-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="740ed-114">Requirements</span></span>



| <span data-ttu-id="740ed-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="740ed-115">Requirement</span></span>          |    <span data-ttu-id="740ed-116">Valor</span><span class="sxs-lookup"><span data-stu-id="740ed-116">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="740ed-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="740ed-117">Minimum supported client</span></span><br/> | <span data-ttu-id="740ed-118">Windows 10, versão 1809 (10,0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="740ed-118">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="740ed-119">DLL</span><span class="sxs-lookup"><span data-stu-id="740ed-119">DLL</span></span><br/>                      | <span data-ttu-id="740ed-120">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="740ed-120">EndpointDlp.dll</span></span> |