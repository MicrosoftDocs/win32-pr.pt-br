---
description: Fornece ao sistema informações sobre um documento antes de uma operação colar da área de transferência ser iniciada.
title: Função DlpNotifyPrePasteFromClipboard (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPrePasteFromClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: cfec6e7abbf2b94ce8bf78e0b1a10082ec54419d
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495304"
---
# <a name="dlpnotifyprepastefromclipboard-function"></a><span data-ttu-id="c36ea-103">Função DlpNotifyPrePasteFromClipboard</span><span class="sxs-lookup"><span data-stu-id="c36ea-103">DlpNotifyPrePasteFromClipboard function</span></span>

<span data-ttu-id="c36ea-104">Fornece ao sistema informações sobre um documento antes de uma operação colar da área de transferência ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="c36ea-104">Provides the system with information about a document before a paste from clipboard operation is initiated.</span></span>

## <a name="syntax"></a><span data-ttu-id="c36ea-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c36ea-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPrePasteFromClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a><span data-ttu-id="c36ea-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c36ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c36ea-107">*DocumentInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c36ea-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c36ea-108">Um ponteiro para uma estrutura de [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) que contém informações sobre o documento no qual o conteúdo está sendo colado.</span><span class="sxs-lookup"><span data-stu-id="c36ea-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document into which content is being pasted.</span></span>

</dd> </dl>




## <a name="return-value"></a><span data-ttu-id="c36ea-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c36ea-109">Return value</span></span>

<span data-ttu-id="c36ea-110">Retornar void.</span><span class="sxs-lookup"><span data-stu-id="c36ea-110">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="c36ea-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="c36ea-111">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="c36ea-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c36ea-112">Requirements</span></span>



| <span data-ttu-id="c36ea-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="c36ea-113">Requirement</span></span>          |    <span data-ttu-id="c36ea-114">Valor</span><span class="sxs-lookup"><span data-stu-id="c36ea-114">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c36ea-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c36ea-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c36ea-116">Windows 10, versão 1809 (10,0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="c36ea-116">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="c36ea-117">DLL</span><span class="sxs-lookup"><span data-stu-id="c36ea-117">DLL</span></span><br/>                      | <span data-ttu-id="c36ea-118">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="c36ea-118">EndpointDlp.dll</span></span> |