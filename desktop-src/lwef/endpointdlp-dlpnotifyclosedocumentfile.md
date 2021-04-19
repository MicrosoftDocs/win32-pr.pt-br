---
description: Fornece ao sistema informações sobre um documento antes da operação de fechamento do arquivo de documento ser iniciada.
title: Função DlpNotifyCloseDocumentFile (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyCloseDocumentFile
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 2438829cde84e9029a86d74e4ed704e1e8d33511
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495346"
---
# <a name="dlpnotifyclosedocumentfile-function"></a><span data-ttu-id="df1db-103">Função DlpNotifyCloseDocumentFile</span><span class="sxs-lookup"><span data-stu-id="df1db-103">DlpNotifyCloseDocumentFile function</span></span>

<span data-ttu-id="df1db-104">Fornece ao sistema informações sobre um documento antes da operação de fechamento do arquivo de documento ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="df1db-104">Provides the system with information about a document before the document file close operation is initiated.</span></span>

## <a name="syntax"></a><span data-ttu-id="df1db-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="df1db-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyCloseDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a><span data-ttu-id="df1db-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="df1db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df1db-107">*DocumentInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="df1db-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df1db-108">Um ponteiro para uma estrutura de [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) que contém informações sobre o documento a ser aberto.</span><span class="sxs-lookup"><span data-stu-id="df1db-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document to be opened.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="df1db-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="df1db-109">Return value</span></span>

<span data-ttu-id="df1db-110">Retornar void.</span><span class="sxs-lookup"><span data-stu-id="df1db-110">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="df1db-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="df1db-111">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="df1db-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df1db-112">Requirements</span></span>


| <span data-ttu-id="df1db-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="df1db-113">Requirement</span></span>          |    <span data-ttu-id="df1db-114">Valor</span><span class="sxs-lookup"><span data-stu-id="df1db-114">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="df1db-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="df1db-115">Minimum supported client</span></span><br/> | <span data-ttu-id="df1db-116">Windows 10, versão 1809 (10,0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="df1db-116">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="df1db-117">DLL</span><span class="sxs-lookup"><span data-stu-id="df1db-117">DLL</span></span><br/>                      | <span data-ttu-id="df1db-118">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="df1db-118">EndpointDlp.dll</span></span> |