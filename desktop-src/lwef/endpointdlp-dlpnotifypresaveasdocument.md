---
description: Fornece ao sistema informações sobre um documento antes de uma operação salvar como ser iniciada.
title: Função DlpNotifyPreSaveAsDocument (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPreSaveAsDocument
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 5226ed63227e2d9dd01155066e2e6e19f77e063f
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495307"
---
# <a name="dlpnotifypresaveasdocument-function"></a><span data-ttu-id="9f1cc-103">Função DlpNotifyPreSaveAsDocument</span><span class="sxs-lookup"><span data-stu-id="9f1cc-103">DlpNotifyPreSaveAsDocument function</span></span>

<span data-ttu-id="9f1cc-104">Fornece ao sistema informações sobre um documento antes de uma operação salvar como ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="9f1cc-104">Provides the system with information about a document before a save as operation is initiated.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f1cc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9f1cc-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPreSaveAsDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ LPCWSTR Destination);
```



## <a name="parameters"></a><span data-ttu-id="9f1cc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9f1cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f1cc-107">*DocumentInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9f1cc-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f1cc-108">Um ponteiro para uma estrutura de [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) que contém informações sobre o documento a ser salvo.</span><span class="sxs-lookup"><span data-stu-id="9f1cc-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document to be saved.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="9f1cc-109">*Destino* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9f1cc-109">*Destination* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f1cc-110">Um **LPCWSTR** que contém o caminho de destino do documento a ser salvo.</span><span class="sxs-lookup"><span data-stu-id="9f1cc-110">A **LPCWSTR** containing the destination path of the document to be saved.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="9f1cc-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9f1cc-111">Return value</span></span>

<span data-ttu-id="9f1cc-112">Retornar void.</span><span class="sxs-lookup"><span data-stu-id="9f1cc-112">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f1cc-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="9f1cc-113">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="9f1cc-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f1cc-114">Requirements</span></span>



| <span data-ttu-id="9f1cc-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f1cc-115">Requirement</span></span>          |    <span data-ttu-id="9f1cc-116">Valor</span><span class="sxs-lookup"><span data-stu-id="9f1cc-116">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f1cc-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9f1cc-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9f1cc-118">Windows 10, versão 1809 (10,0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="9f1cc-118">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="9f1cc-119">DLL</span><span class="sxs-lookup"><span data-stu-id="9f1cc-119">DLL</span></span><br/>                      | <span data-ttu-id="9f1cc-120">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="9f1cc-120">EndpointDlp.dll</span></span> |