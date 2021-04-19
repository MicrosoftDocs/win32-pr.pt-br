---
description: Fornece ao sistema informações sobre um documento após a conclusão da operação salvar como.
title: Função DlpNotifyPostSaveAsDocument (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostSaveAsDocument
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 564e7173cbfe72a020f1c7e12a60ceda25fd845c
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495328"
---
# <a name="dlpnotifypostsaveasdocument-function"></a><span data-ttu-id="1069a-103">Função DlpNotifyPostSaveAsDocument</span><span class="sxs-lookup"><span data-stu-id="1069a-103">DlpNotifyPostSaveAsDocument function</span></span>

<span data-ttu-id="1069a-104">Fornece ao sistema informações sobre um documento após a conclusão da operação salvar como.</span><span class="sxs-lookup"><span data-stu-id="1069a-104">Provides the system with information about a document after the save as operation is completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="1069a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1069a-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPostSaveAsDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ LPCWSTR Destination, _In_ const PDLP_POSTOP_STATUS OpStatus); 
```

## <a name="parameters"></a><span data-ttu-id="1069a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1069a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1069a-107">*DocumentInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1069a-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1069a-108">Um ponteiro para uma estrutura de [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) que contém informações sobre o documento que foi salvo.</span><span class="sxs-lookup"><span data-stu-id="1069a-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document that was saved.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="1069a-109">*Destino* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1069a-109">*Destination* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1069a-110">Um **LPCWSTR** que contém o caminho de destino do documento que foi salvo.</span><span class="sxs-lookup"><span data-stu-id="1069a-110">A **LPCWSTR** containing the destination path the document that was saved.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="1069a-111">*OpStatus* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1069a-111">*OpStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1069a-112">Um ponteiro para uma estrutura de [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) que contém informações de status sobre a operação salvar como.</span><span class="sxs-lookup"><span data-stu-id="1069a-112">A pointer to a [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) structure containing status information about the save as operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="1069a-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1069a-113">Return value</span></span>

<span data-ttu-id="1069a-114">Retornar void.</span><span class="sxs-lookup"><span data-stu-id="1069a-114">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="1069a-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="1069a-115">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="1069a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1069a-116">Requirements</span></span>



| <span data-ttu-id="1069a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1069a-117">Requirement</span></span>          |    <span data-ttu-id="1069a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="1069a-118">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1069a-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1069a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1069a-120">Windows 10, versão 1809 (10,0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="1069a-120">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="1069a-121">DLL</span><span class="sxs-lookup"><span data-stu-id="1069a-121">DLL</span></span><br/>                      | <span data-ttu-id="1069a-122">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="1069a-122">EndpointDlp.dll</span></span> |