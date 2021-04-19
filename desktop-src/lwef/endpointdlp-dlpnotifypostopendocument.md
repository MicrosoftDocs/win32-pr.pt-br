---
description: Fornece ao sistema informações sobre um documento após a conclusão da operação de abertura.
title: Função DlpNotifyPostOpenDocument (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostOpenDocument
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 10121e69ddbdc41516e56ec07e87a2f6dd8148cd
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495341"
---
# <a name="dlpnotifypostopendocument-function"></a><span data-ttu-id="82f7a-103">Função DlpNotifyPostOpenDocument</span><span class="sxs-lookup"><span data-stu-id="82f7a-103">DlpNotifyPostOpenDocument function</span></span>

<span data-ttu-id="82f7a-104">Fornece ao sistema informações sobre um documento após a conclusão de uma operação de documento aberto.</span><span class="sxs-lookup"><span data-stu-id="82f7a-104">Provides the system with information about a document after an open document operation is completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="82f7a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="82f7a-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPostOpenDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus); 
```

## <a name="parameters"></a><span data-ttu-id="82f7a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="82f7a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82f7a-107">*DocumentInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="82f7a-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82f7a-108">Um ponteiro para uma estrutura de [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) que contém informações sobre o documento que foi aberto.</span><span class="sxs-lookup"><span data-stu-id="82f7a-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document that was opened.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="82f7a-109">*OpStatus* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="82f7a-109">*OpStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82f7a-110">Um ponteiro para uma estrutura de [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) que contém informações de status sobre a operação de abrir documento.</span><span class="sxs-lookup"><span data-stu-id="82f7a-110">A pointer to a [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) structure containing status information about the open document operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="82f7a-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="82f7a-111">Return value</span></span>

<span data-ttu-id="82f7a-112">Retornar void.</span><span class="sxs-lookup"><span data-stu-id="82f7a-112">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="82f7a-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="82f7a-113">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="82f7a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82f7a-114">Requirements</span></span>



| <span data-ttu-id="82f7a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="82f7a-115">Requirement</span></span>          |    <span data-ttu-id="82f7a-116">Valor</span><span class="sxs-lookup"><span data-stu-id="82f7a-116">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="82f7a-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="82f7a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="82f7a-118">Windows 10, versão 1809 (10,0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="82f7a-118">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="82f7a-119">DLL</span><span class="sxs-lookup"><span data-stu-id="82f7a-119">DLL</span></span><br/>                      | <span data-ttu-id="82f7a-120">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="82f7a-120">EndpointDlp.dll</span></span> |