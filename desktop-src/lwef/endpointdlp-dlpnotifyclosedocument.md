---
description: Fornece ao sistema informações sobre um documento antes da operação de fechamento do documento ser iniciada.
title: Função DlpNotifyCloseDocument (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyCloseDocument
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 06c2b2527833b498ab2b7f5f3fa0f5a662fe67d7
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495347"
---
# <a name="dlpnotifyclosedocument-function"></a><span data-ttu-id="1030c-103">Função DlpNotifyCloseDocument</span><span class="sxs-lookup"><span data-stu-id="1030c-103">DlpNotifyCloseDocument function</span></span>

<span data-ttu-id="1030c-104">Fornece ao sistema informações sobre um documento antes da operação de fechamento do documento ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="1030c-104">Provides the system with information about a document before the document close operation is initiated.</span></span>

## <a name="syntax"></a><span data-ttu-id="1030c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1030c-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyCloseDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a><span data-ttu-id="1030c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1030c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1030c-107">*DocumentInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1030c-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1030c-108">Um ponteiro para uma estrutura de [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) que contém informações sobre o documento a ser aberto.</span><span class="sxs-lookup"><span data-stu-id="1030c-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document to be opened.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="1030c-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1030c-109">Return value</span></span>

<span data-ttu-id="1030c-110">Retornar void.</span><span class="sxs-lookup"><span data-stu-id="1030c-110">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="1030c-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="1030c-111">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="1030c-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1030c-112">Requirements</span></span>



| <span data-ttu-id="1030c-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="1030c-113">Requirement</span></span>          |    <span data-ttu-id="1030c-114">Valor</span><span class="sxs-lookup"><span data-stu-id="1030c-114">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1030c-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1030c-115">Minimum supported client</span></span><br/> | <span data-ttu-id="1030c-116">Windows 10, versão 1809 (10,0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="1030c-116">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="1030c-117">DLL</span><span class="sxs-lookup"><span data-stu-id="1030c-117">DLL</span></span><br/>                      | <span data-ttu-id="1030c-118">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="1030c-118">EndpointDlp.dll</span></span> |