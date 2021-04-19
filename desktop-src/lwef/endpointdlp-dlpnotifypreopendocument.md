---
description: Fornece ao sistema informações sobre um documento antes de uma operação abrir ser iniciada.
title: Função DlpNotifyPreOpenDocument (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPreOpenDocument
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 557554ad55a3a520fa95fcf53c8044881eed8b21
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495323"
---
# <a name="dlpnotifypreopendocument-function"></a><span data-ttu-id="5d245-103">Função DlpNotifyPreOpenDocument</span><span class="sxs-lookup"><span data-stu-id="5d245-103">DlpNotifyPreOpenDocument function</span></span>

<span data-ttu-id="5d245-104">Fornece ao sistema informações sobre um documento antes de uma operação abrir ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="5d245-104">Provides the system with information about a document before an open operation is initiated.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d245-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5d245-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPreOpenDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a><span data-ttu-id="5d245-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5d245-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d245-107">*DocumentInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5d245-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d245-108">Um ponteiro para uma estrutura de [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) que contém informações sobre o documento a ser aberto.</span><span class="sxs-lookup"><span data-stu-id="5d245-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document to be opened.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="5d245-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5d245-109">Return value</span></span>

<span data-ttu-id="5d245-110">Retornar void.</span><span class="sxs-lookup"><span data-stu-id="5d245-110">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d245-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="5d245-111">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="5d245-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d245-112">Requirements</span></span>



| <span data-ttu-id="5d245-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d245-113">Requirement</span></span>          |    <span data-ttu-id="5d245-114">Valor</span><span class="sxs-lookup"><span data-stu-id="5d245-114">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d245-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d245-115">Minimum supported client</span></span><br/> | <span data-ttu-id="5d245-116">Windows 10, versão 1809 (10,0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="5d245-116">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="5d245-117">DLL</span><span class="sxs-lookup"><span data-stu-id="5d245-117">DLL</span></span><br/>                      | <span data-ttu-id="5d245-118">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="5d245-118">EndpointDlp.dll</span></span> |