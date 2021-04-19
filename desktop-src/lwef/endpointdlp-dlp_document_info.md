---
description: Especifica informações sobre um documento associado a uma operação de DLP de ponto de extremidade.
title: Estrutura de DLP_DOCUMENT_INFO (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DLP_DOCUMENT_INFO
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: d588b627a4d5a88162cb0af67df1b5bf4fd943f1
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495364"
---
# <a name="dlp_document_info-structure"></a><span data-ttu-id="fb891-103">Estrutura de DLP_DOCUMENT_INFO</span><span class="sxs-lookup"><span data-stu-id="fb891-103">DLP_DOCUMENT_INFO structure</span></span>

<span data-ttu-id="fb891-104">Especifica informações sobre um documento associado a uma operação de DLP de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="fb891-104">Specifies information about a document that is associated with an endpoint DLP operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb891-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fb891-105">Syntax</span></span>


```C++
typedef struct _DLP_DOCUMENT_INFO {

    DWORD Version;    
    LPCWSTR PersistentFileName;
    LPCWSTR LocalFileName;

}DLP_DOCUMENT_INFO, *PDLP_DOCUMENT_INFO;
```


## <a name="members"></a><span data-ttu-id="fb891-106">Membros</span><span class="sxs-lookup"><span data-stu-id="fb891-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="fb891-107">*Versão* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="fb891-107">*Version* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb891-108">Um DWORD que especifica a versão da API.</span><span class="sxs-lookup"><span data-stu-id="fb891-108">A DWORD specifying the API version.</span></span> <span data-ttu-id="fb891-109">Esse valor sempre deve ser **DLP_DOCUMENT_INFO_V_LATEST**.</span><span class="sxs-lookup"><span data-stu-id="fb891-109">This value should always be **DLP_DOCUMENT_INFO_V_LATEST**.</span></span> <span data-ttu-id="fb891-110">Essa constante é definida na listagem de arquivos de cabeçalho de exemplo endpointdlp. h no artigo [prevenção de perda de dados do ponto de extremidade](endpointdlp-endpoint-data-loss-prevention.md).</span><span class="sxs-lookup"><span data-stu-id="fb891-110">This constant is defined in the endpointdlp.h sample header file listing in the article [Endpoint data loss prevention](endpointdlp-endpoint-data-loss-prevention.md).</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="fb891-111">*PersistentFileName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fb891-111">*PersistentFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb891-112">Um LPCWSTR que especifica o caminho original do documento.</span><span class="sxs-lookup"><span data-stu-id="fb891-112">A LPCWSTR specifying the original path of the document.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="fb891-113">*LocalFileName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fb891-113">*LocalFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb891-114">Um LPCWSTR especificando o caminho para o arquivo de backup real do documento.</span><span class="sxs-lookup"><span data-stu-id="fb891-114">A LPCWSTR specifying the path to the real backing file of the document.</span></span>

</dd> </dl>



## <a name="remarks"></a><span data-ttu-id="fb891-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="fb891-115">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="fb891-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb891-116">Requirements</span></span>



| <span data-ttu-id="fb891-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb891-117">Requirement</span></span>          |    <span data-ttu-id="fb891-118">Valor</span><span class="sxs-lookup"><span data-stu-id="fb891-118">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb891-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fb891-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fb891-120">Windows 10, versão 1809 (10,0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="fb891-120">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |

