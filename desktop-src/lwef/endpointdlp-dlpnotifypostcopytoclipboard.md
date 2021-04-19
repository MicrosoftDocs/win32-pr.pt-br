---
description: Fornece ao sistema informações sobre um documento após a conclusão de uma operação de cópia para a área de transferência.
title: Função DlpNotifyPostCopyToClipboard (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostCopyToClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: b4b1a375d68819fc36f82a530a7fe7a8abe881c0
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495343"
---
# <a name="dlpnotifypostcopytoclipboard-function"></a><span data-ttu-id="a0bb7-103">Função DlpNotifyPostCopyToClipboard</span><span class="sxs-lookup"><span data-stu-id="a0bb7-103">DlpNotifyPostCopyToClipboard function</span></span>

<span data-ttu-id="a0bb7-104">Fornece ao sistema informações sobre um documento após a conclusão de uma operação de cópia para a área de transferência.</span><span class="sxs-lookup"><span data-stu-id="a0bb7-104">Provides the system with information about a document after a copy to clipboard operation is completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0bb7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a0bb7-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPostCopyToClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);
```



## <a name="parameters"></a><span data-ttu-id="a0bb7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a0bb7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0bb7-107">*DocumentInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a0bb7-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0bb7-108">Um ponteiro para uma estrutura de [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) que contém informações sobre o documento do qual o conteúdo foi copiado.</span><span class="sxs-lookup"><span data-stu-id="a0bb7-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document from which content was copied.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="a0bb7-109">*OpStatus* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a0bb7-109">*OpStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0bb7-110">Um ponteiro para uma estrutura de [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) que contém informações de status sobre a operação de copiar para a área de transferência.</span><span class="sxs-lookup"><span data-stu-id="a0bb7-110">A pointer to a [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) structure containing status information about the copy to clipboard operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="a0bb7-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a0bb7-111">Return value</span></span>

<span data-ttu-id="a0bb7-112">Retornar void.</span><span class="sxs-lookup"><span data-stu-id="a0bb7-112">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0bb7-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="a0bb7-113">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="a0bb7-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0bb7-114">Requirements</span></span>



| <span data-ttu-id="a0bb7-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0bb7-115">Requirement</span></span>          |    <span data-ttu-id="a0bb7-116">Valor</span><span class="sxs-lookup"><span data-stu-id="a0bb7-116">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0bb7-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a0bb7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a0bb7-118">Windows 10, versão 1809 (10,0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="a0bb7-118">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="a0bb7-119">DLL</span><span class="sxs-lookup"><span data-stu-id="a0bb7-119">DLL</span></span><br/>                      | <span data-ttu-id="a0bb7-120">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="a0bb7-120">EndpointDlp.dll</span></span> |