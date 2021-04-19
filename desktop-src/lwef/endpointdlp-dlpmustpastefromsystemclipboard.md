---
description: Determina se o aplicativo deve extrair os dados da área de transferência do sistema em vez de retirá-los de seu cache interno.
title: Função DlpMustPasteFromSystemClipboard (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpMustPasteFromSystemClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 5863173b02cb5c63a2de46653c2d268464e82e65
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495349"
---
# <a name="dlpmustpastefromsystemclipboard-function"></a><span data-ttu-id="14e85-103">Função DlpMustPasteFromSystemClipboard</span><span class="sxs-lookup"><span data-stu-id="14e85-103">DlpMustPasteFromSystemClipboard function</span></span>

<span data-ttu-id="14e85-104">Determina se o aplicativo deve extrair os dados da área de transferência do sistema em vez de retirá-los de seu cache interno.</span><span class="sxs-lookup"><span data-stu-id="14e85-104">Determines whether the app must pull the data from the system clipboard rather than taking it from its internal cache.</span></span>

## <a name="syntax"></a><span data-ttu-id="14e85-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="14e85-105">Syntax</span></span>


```C++
BOOL WINAPI DlpMustPasteFromSystemClipboard();
```


## <a name="return-value"></a><span data-ttu-id="14e85-106">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="14e85-106">Return value</span></span>

<span data-ttu-id="14e85-107">TRUE se a chamada para a área de transferência do sistema operacional for obrigatória; caso contrário, FALSE.</span><span class="sxs-lookup"><span data-stu-id="14e85-107">TRUE if calling into the OS clipboard is mandatory; otherwise, FALSE.</span></span>

## <a name="remarks"></a><span data-ttu-id="14e85-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="14e85-108">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="14e85-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14e85-109">Requirements</span></span>



| <span data-ttu-id="14e85-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="14e85-110">Requirement</span></span>          |    <span data-ttu-id="14e85-111">Valor</span><span class="sxs-lookup"><span data-stu-id="14e85-111">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="14e85-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="14e85-112">Minimum supported client</span></span><br/> | <span data-ttu-id="14e85-113">Windows 10, versão 1809 (10,0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="14e85-113">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="14e85-114">DLL</span><span class="sxs-lookup"><span data-stu-id="14e85-114">DLL</span></span><br/>                      | <span data-ttu-id="14e85-115">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="14e85-115">EndpointDlp.dll</span></span> |