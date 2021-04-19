---
description: Especifica informações de status sobre uma operação de DLP de ponto de extremidade.
title: Estrutura de DLP_POSTOP_STATUS (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DLP_POSTOP_STATUS
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: c0221926700fc8960de5ef4d25c36136c3fc9737
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495309"
---
# <a name="dlp_postop_status-structure"></a><span data-ttu-id="5e1c9-103">Estrutura de DLP_POSTOP_STATUS</span><span class="sxs-lookup"><span data-stu-id="5e1c9-103">DLP_POSTOP_STATUS structure</span></span>

<span data-ttu-id="5e1c9-104">Especifica informações de status sobre uma operação de DLP de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="5e1c9-104">Specifies status information about an endpoint DLP operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e1c9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5e1c9-105">Syntax</span></span>


```C++
typedef struct _DLP_POSTOP_STATUS {
    
    DWORD Version;    
    BOOL OperationSuccess;  

} DLP_POSTOP_STATUS, *PDLP_POSTOP_STATUS; 
```


## <a name="members"></a><span data-ttu-id="5e1c9-106">Membros</span><span class="sxs-lookup"><span data-stu-id="5e1c9-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="5e1c9-107">*Versão* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="5e1c9-107">*Version* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e1c9-108">Um DWORD que especifica a versão da API.</span><span class="sxs-lookup"><span data-stu-id="5e1c9-108">A DWORD specifying the API version.</span></span> <span data-ttu-id="5e1c9-109">Esse valor sempre deve ser **DLP_POSTOP_STATUS_V_LATEST**.</span><span class="sxs-lookup"><span data-stu-id="5e1c9-109">This value should always be **DLP_POSTOP_STATUS_V_LATEST**.</span></span> <span data-ttu-id="5e1c9-110">Essa constante é definida na listagem de arquivos de cabeçalho de exemplo endpointdlp. h no artigo [prevenção de perda de dados do ponto de extremidade](endpointdlp-endpoint-data-loss-prevention.md)</span><span class="sxs-lookup"><span data-stu-id="5e1c9-110">This constant is defined in the endpointdlp.h sample header file listing in the article [Endpoint data loss prevention](endpointdlp-endpoint-data-loss-prevention.md)</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="5e1c9-111">*OperationSuccess* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5e1c9-111">*OperationSuccess* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e1c9-112">Um BOOL que indica se a operação aberta foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="5e1c9-112">A BOOL indicating whether the open operation was successful.</span></span>

</dd> </dl>





## <a name="remarks"></a><span data-ttu-id="5e1c9-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="5e1c9-113">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="5e1c9-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e1c9-114">Requirements</span></span>



| <span data-ttu-id="5e1c9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e1c9-115">Requirement</span></span>          |    <span data-ttu-id="5e1c9-116">Valor</span><span class="sxs-lookup"><span data-stu-id="5e1c9-116">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e1c9-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e1c9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5e1c9-118">Windows 10, versão 1809 (10,0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="5e1c9-118">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
