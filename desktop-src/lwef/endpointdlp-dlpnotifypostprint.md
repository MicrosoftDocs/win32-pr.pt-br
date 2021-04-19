---
description: Fornece ao sistema informações sobre um documento após a conclusão de uma operação de impressão.
title: Função DlpNotifyPostPrint (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostPrint
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: b1206aa4e358e0763c10a0d9b5028acae25f5683
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495329"
---
# <a name="dlpnotifypostprint-function"></a><span data-ttu-id="9e9e9-103">Função DlpNotifyPostPrint</span><span class="sxs-lookup"><span data-stu-id="9e9e9-103">DlpNotifyPostPrint function</span></span>

<span data-ttu-id="9e9e9-104">Fornece ao sistema informações sobre um documento após a conclusão de uma operação de impressão.</span><span class="sxs-lookup"><span data-stu-id="9e9e9-104">Provides the system with information about a document after a print operation has completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e9e9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9e9e9-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPostPrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);
```

## <a name="parameters"></a><span data-ttu-id="9e9e9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9e9e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e9e9-107">*DocumentInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9e9e9-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e9e9-108">Um ponteiro para uma estrutura de [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) que contém informações sobre o documento associado à operação de impressão.</span><span class="sxs-lookup"><span data-stu-id="9e9e9-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document associated with the print operation.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="9e9e9-109">*Informações* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9e9e9-109">*PrintInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e9e9-110">Um ponteiro para uma estrutura de [DLP_PRINT_INFO](endpointdlp-dlp_print_info.md) que contém informações sobre a operação de impressão.</span><span class="sxs-lookup"><span data-stu-id="9e9e9-110">A pointer to a [DLP_PRINT_INFO](endpointdlp-dlp_print_info.md) structure containing information about the print operation.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="9e9e9-111">*OpStatus* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9e9e9-111">*OpStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e9e9-112">Um ponteiro para uma estrutura de [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) que contém informações de status sobre a operação de impressão.</span><span class="sxs-lookup"><span data-stu-id="9e9e9-112">A pointer to a [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) structure containing status information about the print operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="9e9e9-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9e9e9-113">Return value</span></span>

<span data-ttu-id="9e9e9-114">Retornar void.</span><span class="sxs-lookup"><span data-stu-id="9e9e9-114">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e9e9-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="9e9e9-115">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="9e9e9-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e9e9-116">Requirements</span></span>



| <span data-ttu-id="9e9e9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e9e9-117">Requirement</span></span>          |    <span data-ttu-id="9e9e9-118">Valor</span><span class="sxs-lookup"><span data-stu-id="9e9e9-118">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e9e9-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9e9e9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9e9e9-120">Windows 10, versão 1809 (10,0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="9e9e9-120">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="9e9e9-121">DLL</span><span class="sxs-lookup"><span data-stu-id="9e9e9-121">DLL</span></span><br/>                      | <span data-ttu-id="9e9e9-122">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="9e9e9-122">EndpointDlp.dll</span></span> |