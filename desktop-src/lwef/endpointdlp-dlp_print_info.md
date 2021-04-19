---
description: Especifica informações sobre um documento que está associado a uma operação de impressão de DLP de ponto de extremidade.
title: Estrutura de DLP_PRINT_INFO (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DLP_PRINT_INFO
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: 37bde9f62de07083aac6a3d2fb367b021caf3732
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495363"
---
# <a name="dlp_print_info-structure"></a><span data-ttu-id="c5706-103">Estrutura de DLP_PRINT_INFO</span><span class="sxs-lookup"><span data-stu-id="c5706-103">DLP_PRINT_INFO structure</span></span>

<span data-ttu-id="c5706-104">Especifica informações sobre um documento que está associado a uma operação de impressão de DLP de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="c5706-104">Specifies information about a document that is associated with an endpoint DLP print operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5706-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c5706-105">Syntax</span></span>


```C++
typedef struct _DLP_PRINT_INFO {
    DWORD Version;
    LPCWSTR PrinterName;
    LPCWSTR JobName;
    LPCWSTR OutputFileName;
    
}DLP_PRINT_INFO, *PDLP_PRINT_INFO;
```


## <a name="members"></a><span data-ttu-id="c5706-106">Membros</span><span class="sxs-lookup"><span data-stu-id="c5706-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c5706-107">*Versão* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="c5706-107">*Version* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5706-108">Um DWORD que especifica a versão da API.</span><span class="sxs-lookup"><span data-stu-id="c5706-108">A DWORD specifying the API version.</span></span> <span data-ttu-id="c5706-109">Esse valor sempre deve ser **DLP_PRINT_INFO_V_LATEST**.</span><span class="sxs-lookup"><span data-stu-id="c5706-109">This value should always be **DLP_PRINT_INFO_V_LATEST**.</span></span> <span data-ttu-id="c5706-110">Essa constante é definida na listagem de arquivos de cabeçalho de exemplo endpointdlp. h no artigo [prevenção de perda de dados do ponto de extremidade](endpointdlp-endpoint-data-loss-prevention.md).</span><span class="sxs-lookup"><span data-stu-id="c5706-110">This constant is defined in the endpointdlp.h sample header file listing in the article [Endpoint data loss prevention](endpointdlp-endpoint-data-loss-prevention.md).</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="c5706-111">*PrinterName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c5706-111">*PrinterName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5706-112">Um LPCWSTR que identifica a impressora de destino.</span><span class="sxs-lookup"><span data-stu-id="c5706-112">A LPCWSTR identifying the destination printer.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="c5706-113">*JobName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c5706-113">*JobName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5706-114">Um LPCWSTR especificando o nome do trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="c5706-114">A LPCWSTR specifying print job name.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="c5706-115">*NomeDoArquivoDeSaída* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c5706-115">*OutputFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5706-116">Um LPCWSTR que especifica o caminho para o arquivo de saída ao imprimir em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="c5706-116">A LPCWSTR specifying the path to the output file, when printing to a file.</span></span>

</dd> </dl>



## <a name="remarks"></a><span data-ttu-id="c5706-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="c5706-117">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="c5706-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5706-118">Requirements</span></span>



| <span data-ttu-id="c5706-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5706-119">Requirement</span></span>          |    <span data-ttu-id="c5706-120">Valor</span><span class="sxs-lookup"><span data-stu-id="c5706-120">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5706-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c5706-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c5706-122">Windows 10, versão 1809 (10,0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="c5706-122">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |

