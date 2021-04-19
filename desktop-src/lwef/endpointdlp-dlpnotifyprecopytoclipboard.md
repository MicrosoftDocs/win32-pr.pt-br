---
description: Fornece ao sistema informações sobre um documento antes de uma operação de cópia para a área de transferência ser iniciada.
title: Função DlpNotifyPreCopyToClipboard (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPreCopyToClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: b8e835e58d19570b9459d91ad131bbc0f38f378a
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495325"
---
# <a name="dlpnotifyprecopytoclipboard-function"></a><span data-ttu-id="a4a96-103">Função DlpNotifyPreCopyToClipboard</span><span class="sxs-lookup"><span data-stu-id="a4a96-103">DlpNotifyPreCopyToClipboard function</span></span>

<span data-ttu-id="a4a96-104">Fornece ao sistema informações sobre um documento antes de uma operação de cópia para a área de transferência ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="a4a96-104">Provides the system with information about a document before a copy to clipboard operation is initiated.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4a96-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a4a96-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPreCopyToClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a><span data-ttu-id="a4a96-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a4a96-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4a96-107">*DocumentInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a4a96-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4a96-108">Um ponteiro para uma estrutura de [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) que contém informações sobre o documento do qual o conteúdo está sendo copiado.</span><span class="sxs-lookup"><span data-stu-id="a4a96-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document from which content is being copied.</span></span>

</dd> </dl>




## <a name="return-value"></a><span data-ttu-id="a4a96-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a4a96-109">Return value</span></span>

<span data-ttu-id="a4a96-110">Retornar void.</span><span class="sxs-lookup"><span data-stu-id="a4a96-110">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4a96-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="a4a96-111">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="a4a96-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4a96-112">Requirements</span></span>



| <span data-ttu-id="a4a96-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4a96-113">Requirement</span></span>          |    <span data-ttu-id="a4a96-114">Valor</span><span class="sxs-lookup"><span data-stu-id="a4a96-114">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4a96-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a4a96-115">Minimum supported client</span></span><br/> | <span data-ttu-id="a4a96-116">Windows 10, versão 1809 (10,0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="a4a96-116">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="a4a96-117">DLL</span><span class="sxs-lookup"><span data-stu-id="a4a96-117">DLL</span></span><br/>                      | <span data-ttu-id="a4a96-118">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="a4a96-118">EndpointDlp.dll</span></span> |