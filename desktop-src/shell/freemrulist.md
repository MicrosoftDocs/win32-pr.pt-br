---
description: Libera o handle associado à lista de MRU (usados mais recentemente) e grava dados armazenados em cache no Registro.
title: Função FreeMRUList
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreeMRUList
api_type:
- DllExport
api_location:
- Comctl32.dll
ms.assetid: 51db9352-7188-4fb7-9c92-1d9579cd7250
ms.openlocfilehash: 7d31d261629853c3b82b9d1564c5e8755e047570
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840617"
---
# <a name="freemrulist-function"></a><span data-ttu-id="609b4-103">Função FreeMRUList</span><span class="sxs-lookup"><span data-stu-id="609b4-103">FreeMRUList function</span></span>

<span data-ttu-id="609b4-104">Libera o handle associado à lista de MRU (usados mais recentemente) e grava dados armazenados em cache no Registro.</span><span class="sxs-lookup"><span data-stu-id="609b4-104">Frees the handle associated with the most recently used (MRU) list and writes cached data to the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="609b4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="609b4-105">Syntax</span></span>


```C++
int FreeMRUList(
  _In_ HANDLE hMRU
);
```



## <a name="parameters"></a><span data-ttu-id="609b4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="609b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="609b4-107">*hMRU* \[ Em\]</span><span class="sxs-lookup"><span data-stu-id="609b4-107">*hMRU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="609b4-108">Tipo: **HANDLE**</span><span class="sxs-lookup"><span data-stu-id="609b4-108">Type: **HANDLE**</span></span>

<span data-ttu-id="609b4-109">O alça da lista mru para liberar.</span><span class="sxs-lookup"><span data-stu-id="609b4-109">The handle of the MRU list to free.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="609b4-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="609b4-110">Return value</span></span>

<span data-ttu-id="609b4-111">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="609b4-111">Type: **int**</span></span>

<span data-ttu-id="609b4-112">Retornará um valor não negativo se for bem-sucedido; caso contrário, -1.</span><span class="sxs-lookup"><span data-stu-id="609b4-112">Returns a non-negative value if successful, -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="609b4-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="609b4-113">Remarks</span></span>

<span data-ttu-id="609b4-114">Se a lista mru foi criada usando o sinalizador **\_ MRU CACHEWRITE,** chamar **FreeMRUList** faz com que todas as alterações ainda não gravadas na versão da lista mru armazenada no registro sejam gravadas no momento.</span><span class="sxs-lookup"><span data-stu-id="609b4-114">If the MRU list was created using the **MRU\_CACHEWRITE** flag, calling **FreeMRUList** causes any changes not yet written to the version of the MRU list stored in registry to be written at this time.</span></span>

<span data-ttu-id="609b4-115">Essa função não está incluída em um header ou biblioteca público.</span><span class="sxs-lookup"><span data-stu-id="609b4-115">This function is not included in a public header or library.</span></span> <span data-ttu-id="609b4-116">Ele deve ser extraído da comctl32.dll pelo ordinal 152.</span><span class="sxs-lookup"><span data-stu-id="609b4-116">It must be extracted from comctl32.dll by ordinal 152.</span></span>

## <a name="requirements"></a><span data-ttu-id="609b4-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="609b4-117">Requirements</span></span>



| <span data-ttu-id="609b4-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="609b4-118">Requirement</span></span> | <span data-ttu-id="609b4-119">Valor</span><span class="sxs-lookup"><span data-stu-id="609b4-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="609b4-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="609b4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="609b4-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="609b4-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="609b4-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="609b4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="609b4-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="609b4-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="609b4-124">DLL</span><span class="sxs-lookup"><span data-stu-id="609b4-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="609b4-125"><dt>Comctl32.dll (versão 5.0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="609b4-125"><dt>Comctl32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




