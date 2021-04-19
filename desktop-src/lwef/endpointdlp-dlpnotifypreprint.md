---
description: Fornece ao sistema informações sobre um documento antes de uma operação de impressão ser iniciada.
title: Função DlpNotifyPrePrint (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPrePrint
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: eef5e3a19a6b93a49ba8b600be77385a99d3153a
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495306"
---
# <a name="dlpnotifypreprint-function"></a><span data-ttu-id="be76e-103">Função DlpNotifyPrePrint</span><span class="sxs-lookup"><span data-stu-id="be76e-103">DlpNotifyPrePrint function</span></span>

<span data-ttu-id="be76e-104">Fornece ao sistema informações sobre um documento antes de uma operação de impressão ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="be76e-104">Provides the system with information about a document before a print operation is initiated.</span></span>

## <a name="syntax"></a><span data-ttu-id="be76e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="be76e-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPrePrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo);
```



## <a name="parameters"></a><span data-ttu-id="be76e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="be76e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be76e-107">*DocumentInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="be76e-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be76e-108">Um ponteiro para uma estrutura de [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) que contém informações sobre o documento a ser impresso.</span><span class="sxs-lookup"><span data-stu-id="be76e-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document to be printed.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="be76e-109">*Informações* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="be76e-109">*PrintInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be76e-110">Um ponteiro para uma estrutura de [DLP_PRINT_INFO](endpointdlp-dlp_print_info.md) que contém informações sobre a operação de impressão.</span><span class="sxs-lookup"><span data-stu-id="be76e-110">A pointer to a [DLP_PRINT_INFO](endpointdlp-dlp_print_info.md) structure containing information about print operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="be76e-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="be76e-111">Return value</span></span>

<span data-ttu-id="be76e-112">Retornar void.</span><span class="sxs-lookup"><span data-stu-id="be76e-112">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="be76e-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="be76e-113">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="be76e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be76e-114">Requirements</span></span>



| <span data-ttu-id="be76e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="be76e-115">Requirement</span></span>          |    <span data-ttu-id="be76e-116">Valor</span><span class="sxs-lookup"><span data-stu-id="be76e-116">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="be76e-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be76e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="be76e-118">Windows 10, versão 1809 (10,0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="be76e-118">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="be76e-119">DLL</span><span class="sxs-lookup"><span data-stu-id="be76e-119">DLL</span></span><br/>                      | <span data-ttu-id="be76e-120">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="be76e-120">EndpointDlp.dll</span></span> |