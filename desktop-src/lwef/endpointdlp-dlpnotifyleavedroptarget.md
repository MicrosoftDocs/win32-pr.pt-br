---
description: Fornece ao sistema informações sobre um documento quando um destino de soltar é encerrado.
title: Função DlpNotifyLeaveDropTarget (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyLeaveDropTarget
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 2f96ea9a825ca930631fe94dd1a3d632019dd9c1
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495345"
---
# <a name="dlpnotifyleavedroptarget-function"></a><span data-ttu-id="387c9-103">Função DlpNotifyLeaveDropTarget</span><span class="sxs-lookup"><span data-stu-id="387c9-103">DlpNotifyLeaveDropTarget function</span></span>

<span data-ttu-id="387c9-104">Fornece ao sistema informações sobre um documento quando um destino de soltar é encerrado.</span><span class="sxs-lookup"><span data-stu-id="387c9-104">Provides the system with information about a document when a drop target is exited.</span></span>

## <a name="syntax"></a><span data-ttu-id="387c9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="387c9-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyLeaveDropTarget(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);
```



## <a name="parameters"></a><span data-ttu-id="387c9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="387c9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="387c9-107">*DocumentInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="387c9-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="387c9-108">Um ponteiro para uma estrutura de [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) que contém informações sobre o documento associado à operação de soltar.</span><span class="sxs-lookup"><span data-stu-id="387c9-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document associated with the drop operation.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="387c9-109">*OpStatus* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="387c9-109">*OpStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="387c9-110">Um ponteiro para uma estrutura de [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) que contém informações de status sobre a operação de saída de destino drop.</span><span class="sxs-lookup"><span data-stu-id="387c9-110">A pointer to a [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) structure containing status information about the drop target exit operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="387c9-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="387c9-111">Return value</span></span>

<span data-ttu-id="387c9-112">Retornar void.</span><span class="sxs-lookup"><span data-stu-id="387c9-112">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="387c9-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="387c9-113">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="387c9-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="387c9-114">Requirements</span></span>



| <span data-ttu-id="387c9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="387c9-115">Requirement</span></span>          |    <span data-ttu-id="387c9-116">Valor</span><span class="sxs-lookup"><span data-stu-id="387c9-116">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="387c9-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="387c9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="387c9-118">Windows 10, versão 1809 (10,0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="387c9-118">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="387c9-119">DLL</span><span class="sxs-lookup"><span data-stu-id="387c9-119">DLL</span></span><br/>                      | <span data-ttu-id="387c9-120">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="387c9-120">EndpointDlp.dll</span></span> |