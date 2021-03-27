---
description: Cria uma nova lista MRU (usada mais recentemente).
title: Função CreateMRUListW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateMRUListW
- CreateMRUListW
api_type:
- DllExport
api_location:
- Comctl32.dll
ms.assetid: b2d9e3c7-8151-45ef-9658-bd33a87b4c9c
ms.openlocfilehash: 572e52f1461e3d48ab9eba1aa903c7fb690636d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646836"
---
# <a name="createmrulistw-function"></a><span data-ttu-id="e7100-103">Função CreateMRUListW</span><span class="sxs-lookup"><span data-stu-id="e7100-103">CreateMRUListW function</span></span>

<span data-ttu-id="e7100-104">Cria uma nova lista MRU (usada mais recentemente).</span><span class="sxs-lookup"><span data-stu-id="e7100-104">Creates a new most recently used (MRU) list.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7100-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e7100-105">Syntax</span></span>


```C++
int CreateMRUListW(
  _In_ LPMRUINFO lpmi
);
```



## <a name="parameters"></a><span data-ttu-id="e7100-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e7100-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7100-107">*lpmi* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e7100-107">*lpmi* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7100-108">Tipo: **LPMRUINFO**</span><span class="sxs-lookup"><span data-stu-id="e7100-108">Type: **LPMRUINFO**</span></span>

<span data-ttu-id="e7100-109">Um ponteiro para uma estrutura [**MRUINFO**](mruinfo.md) que define a lista MRU.</span><span class="sxs-lookup"><span data-stu-id="e7100-109">A pointer to an [**MRUINFO**](mruinfo.md) structure defining the MRU list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7100-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e7100-110">Return value</span></span>

<span data-ttu-id="e7100-111">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="e7100-111">Type: **int**</span></span>

<span data-ttu-id="e7100-112">Retorna um identificador para a nova lista MRU ou 0 em caso de erro.</span><span class="sxs-lookup"><span data-stu-id="e7100-112">Returns a handle to the new MRU list, or 0 in case of an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7100-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="e7100-113">Remarks</span></span>

<span data-ttu-id="e7100-114">Essa função não está incluída em um cabeçalho ou biblioteca pública.</span><span class="sxs-lookup"><span data-stu-id="e7100-114">This function is not included in a public header or library.</span></span> <span data-ttu-id="e7100-115">Ele pode ser acessado por meio de [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) ou extraído de comctl32.dll por seu ordinal, que é 400 para **CreateMRUListW**.</span><span class="sxs-lookup"><span data-stu-id="e7100-115">It can be accessed through [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) or extracted from comctl32.dll by its ordinal, which is 400 for **CreateMRUListW**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7100-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7100-116">Requirements</span></span>



| <span data-ttu-id="e7100-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7100-117">Requirement</span></span> | <span data-ttu-id="e7100-118">Valor</span><span class="sxs-lookup"><span data-stu-id="e7100-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7100-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e7100-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e7100-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e7100-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e7100-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e7100-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e7100-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e7100-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e7100-123">DLL</span><span class="sxs-lookup"><span data-stu-id="e7100-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7100-124"><dt>Comctl32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="e7100-124"><dt>Comctl32.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="e7100-125">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="e7100-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e7100-126">**CreateMRUListW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="e7100-126">**CreateMRUListW** (Unicode)</span></span><br/>                                                                        |



 

 
