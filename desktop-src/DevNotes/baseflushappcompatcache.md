---
description: Libera o cache de compatibilidade de aplicativos.
ms.assetid: 03f47813-87f6-4b71-b453-77a2facab019
title: Função BaseFlushAppcompatCache
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BaseFlushAppcompatCache
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-appcompat-l1-1-0.dll
- KernelBase.dll
- API-MS-Win-Core-appcompat-l1-1-1.dll
ms.openlocfilehash: 6118c78784bb96b9f25e008cd2221112eeb646f3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089009"
---
# <a name="baseflushappcompatcache-function"></a><span data-ttu-id="e0f53-103">Função BaseFlushAppcompatCache</span><span class="sxs-lookup"><span data-stu-id="e0f53-103">BaseFlushAppcompatCache function</span></span>

<span data-ttu-id="e0f53-104">Libera o cache de compatibilidade de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="e0f53-104">Flushes the application compatibility cache.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0f53-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e0f53-105">Syntax</span></span>


```C++
BOOL WINAPI BaseFlushAppcompatCache(void);
```



## <a name="parameters"></a><span data-ttu-id="e0f53-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e0f53-106">Parameters</span></span>

<span data-ttu-id="e0f53-107">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="e0f53-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e0f53-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="e0f53-108">Return value</span></span>

<span data-ttu-id="e0f53-109">A função retornará **true** se for bem sucedido e **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="e0f53-109">The function returns **TRUE** if it succeeds and **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0f53-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="e0f53-110">Remarks</span></span>

<span data-ttu-id="e0f53-111">O chamador deve ser um administrador.</span><span class="sxs-lookup"><span data-stu-id="e0f53-111">The caller must be an administrator.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0f53-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0f53-112">Requirements</span></span>



| <span data-ttu-id="e0f53-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0f53-113">Requirement</span></span> | <span data-ttu-id="e0f53-114">Valor</span><span class="sxs-lookup"><span data-stu-id="e0f53-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0f53-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e0f53-115">Minimum supported client</span></span><br/> | <span data-ttu-id="e0f53-116">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e0f53-116">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e0f53-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e0f53-117">Minimum supported server</span></span><br/> | <span data-ttu-id="e0f53-118">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e0f53-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e0f53-119">DLL</span><span class="sxs-lookup"><span data-stu-id="e0f53-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0f53-120"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0f53-120"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0f53-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="e0f53-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0f53-122">**ShimFlushCache**</span><span class="sxs-lookup"><span data-stu-id="e0f53-122">**ShimFlushCache**</span></span>](shimflushcache.md)
</dt> </dl>

 

 




