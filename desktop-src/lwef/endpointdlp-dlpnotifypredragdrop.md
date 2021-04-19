---
description: Fornece ao sistema informações sobre um documento antes de uma operação arrastar e soltar ser iniciada.
title: Função DlpNotifyPreDragDrop (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPreDragDrop
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: d88a28c0dff4b13cf1c1848eeb8623c3acd1c024
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495324"
---
# <a name="dlpnotifypredragdrop-function"></a><span data-ttu-id="30d66-103">Função DlpNotifyPreDragDrop</span><span class="sxs-lookup"><span data-stu-id="30d66-103">DlpNotifyPreDragDrop function</span></span>

<span data-ttu-id="30d66-104">Fornece ao sistema informações sobre um documento antes de uma operação arrastar e soltar ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="30d66-104">Provides the system with information about a document before a drag drop operation is initiated.</span></span>

## <a name="syntax"></a><span data-ttu-id="30d66-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="30d66-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPreDragDrop(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a><span data-ttu-id="30d66-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="30d66-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30d66-107">*DocumentInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="30d66-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30d66-108">Um ponteiro para uma estrutura de [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) que contém informações sobre o documento associado à operação de arrastar e soltar.</span><span class="sxs-lookup"><span data-stu-id="30d66-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document associated with the drag drop operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="30d66-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="30d66-109">Return value</span></span>

<span data-ttu-id="30d66-110">Retornar void.</span><span class="sxs-lookup"><span data-stu-id="30d66-110">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="30d66-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="30d66-111">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="30d66-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30d66-112">Requirements</span></span>



| <span data-ttu-id="30d66-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="30d66-113">Requirement</span></span>          |    <span data-ttu-id="30d66-114">Valor</span><span class="sxs-lookup"><span data-stu-id="30d66-114">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="30d66-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="30d66-115">Minimum supported client</span></span><br/> | <span data-ttu-id="30d66-116">Windows 10, versão 1809 (10,0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="30d66-116">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="30d66-117">DLL</span><span class="sxs-lookup"><span data-stu-id="30d66-117">DLL</span></span><br/>                      | <span data-ttu-id="30d66-118">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="30d66-118">EndpointDlp.dll</span></span> |