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
ms.openlocfilehash: 34cd3dd9e5b9e62bbdd13b31d95e7205e4427de6
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843377"
---
# <a name="createmrulistw-function"></a><span data-ttu-id="46841-103">Função CreateMRUListW</span><span class="sxs-lookup"><span data-stu-id="46841-103">CreateMRUListW function</span></span>

<span data-ttu-id="46841-104">Cria uma nova lista MRU (usada mais recentemente).</span><span class="sxs-lookup"><span data-stu-id="46841-104">Creates a new most recently used (MRU) list.</span></span>

## <a name="syntax"></a><span data-ttu-id="46841-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="46841-105">Syntax</span></span>


```C++
int CreateMRUListW(
  _In_ LPMRUINFO lpmi
);
```



## <a name="parameters"></a><span data-ttu-id="46841-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="46841-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46841-107">*lpmi* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="46841-107">*lpmi* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46841-108">Tipo: **LPMRUINFO**</span><span class="sxs-lookup"><span data-stu-id="46841-108">Type: **LPMRUINFO**</span></span>

<span data-ttu-id="46841-109">Um ponteiro para uma estrutura [**MRUINFO**](mruinfo.md) que define a lista MRU.</span><span class="sxs-lookup"><span data-stu-id="46841-109">A pointer to an [**MRUINFO**](mruinfo.md) structure defining the MRU list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46841-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="46841-110">Return value</span></span>

<span data-ttu-id="46841-111">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="46841-111">Type: **int**</span></span>

<span data-ttu-id="46841-112">Retorna um identificador para a nova lista MRU ou 0 em caso de erro.</span><span class="sxs-lookup"><span data-stu-id="46841-112">Returns a handle to the new MRU list, or 0 in case of an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="46841-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="46841-113">Remarks</span></span>

<span data-ttu-id="46841-114">Essa função não está incluída em um cabeçalho ou biblioteca pública.</span><span class="sxs-lookup"><span data-stu-id="46841-114">This function is not included in a public header or library.</span></span> <span data-ttu-id="46841-115">Ele pode ser acessado por meio de [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) ou extraído de comctl32.dll por seu ordinal, que é 400 para **CreateMRUListW**.</span><span class="sxs-lookup"><span data-stu-id="46841-115">It can be accessed through [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) or extracted from comctl32.dll by its ordinal, which is 400 for **CreateMRUListW**.</span></span>

## <a name="requirements"></a><span data-ttu-id="46841-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46841-116">Requirements</span></span>



| <span data-ttu-id="46841-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="46841-117">Requirement</span></span> | <span data-ttu-id="46841-118">Valor</span><span class="sxs-lookup"><span data-stu-id="46841-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46841-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="46841-119">Minimum supported client</span></span><br/> | <span data-ttu-id="46841-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="46841-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="46841-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="46841-121">Minimum supported server</span></span><br/> | <span data-ttu-id="46841-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="46841-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="46841-123">DLL</span><span class="sxs-lookup"><span data-stu-id="46841-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46841-124"><dt>Comctl32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="46841-124"><dt>Comctl32.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="46841-125">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="46841-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="46841-126">**CreateMRUListW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="46841-126">**CreateMRUListW** (Unicode)</span></span><br/>                                                                        |



 

 
