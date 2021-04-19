---
description: Fornece ao sistema informações sobre um documento quando um destino de soltar é inserido.
title: Função DlpNotifyEnterDropTarget (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyEnterDropTarget
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: ec1eee1cee7bbcc38ce3094e3e2f8b650cf3b2a9
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495344"
---
# <a name="dlpnotifyenterdroptarget-function"></a><span data-ttu-id="b731f-103">Função DlpNotifyEnterDropTarget</span><span class="sxs-lookup"><span data-stu-id="b731f-103">DlpNotifyEnterDropTarget function</span></span>

<span data-ttu-id="b731f-104">Fornece ao sistema informações sobre um documento quando um destino de soltar é inserido.</span><span class="sxs-lookup"><span data-stu-id="b731f-104">Provides the system with information about a document when a drop target is entered.</span></span>

## <a name="syntax"></a><span data-ttu-id="b731f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b731f-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyEnterDropTarget(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a><span data-ttu-id="b731f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b731f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b731f-107">*DocumentInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b731f-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b731f-108">Um ponteiro para uma estrutura de [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) que contém informações sobre o documento associado à operação de soltar.</span><span class="sxs-lookup"><span data-stu-id="b731f-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document associated with the drop operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="b731f-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b731f-109">Return value</span></span>

<span data-ttu-id="b731f-110">Retornar void.</span><span class="sxs-lookup"><span data-stu-id="b731f-110">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="b731f-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="b731f-111">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="b731f-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b731f-112">Requirements</span></span>



| <span data-ttu-id="b731f-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="b731f-113">Requirement</span></span>          |    <span data-ttu-id="b731f-114">Valor</span><span class="sxs-lookup"><span data-stu-id="b731f-114">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b731f-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b731f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="b731f-116">Windows 10, versão 1809 (10,0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="b731f-116">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="b731f-117">DLL</span><span class="sxs-lookup"><span data-stu-id="b731f-117">DLL</span></span><br/>                      | <span data-ttu-id="b731f-118">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="b731f-118">EndpointDlp.dll</span></span> |