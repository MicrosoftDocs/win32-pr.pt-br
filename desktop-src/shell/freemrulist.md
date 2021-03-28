---
description: Libera o identificador associado à lista MRU (usados mais recentemente) e grava os dados armazenados em cache no registro.
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
ms.openlocfilehash: 8140586d5f428a66f27a71ea665ae6761380e3a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967925"
---
# <a name="freemrulist-function"></a><span data-ttu-id="d6491-103">Função FreeMRUList</span><span class="sxs-lookup"><span data-stu-id="d6491-103">FreeMRUList function</span></span>

<span data-ttu-id="d6491-104">Libera o identificador associado à lista MRU (usados mais recentemente) e grava os dados armazenados em cache no registro.</span><span class="sxs-lookup"><span data-stu-id="d6491-104">Frees the handle associated with the most recently used (MRU) list and writes cached data to the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6491-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d6491-105">Syntax</span></span>


```C++
int FreeMRUList(
  _In_ HANDLE hMRU
);
```



## <a name="parameters"></a><span data-ttu-id="d6491-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d6491-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6491-107">*hMRU* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d6491-107">*hMRU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6491-108">Tipo: **identificador**</span><span class="sxs-lookup"><span data-stu-id="d6491-108">Type: **HANDLE**</span></span>

<span data-ttu-id="d6491-109">O identificador da lista MRU como livre.</span><span class="sxs-lookup"><span data-stu-id="d6491-109">The handle of the MRU list to free.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6491-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d6491-110">Return value</span></span>

<span data-ttu-id="d6491-111">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="d6491-111">Type: **int**</span></span>

<span data-ttu-id="d6491-112">Retorna um valor não negativo se for bem-sucedido,-1 caso contrário.</span><span class="sxs-lookup"><span data-stu-id="d6491-112">Returns a non-negative value if successful, -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6491-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="d6491-113">Remarks</span></span>

<span data-ttu-id="d6491-114">Se a lista MRU tiver sido criada usando o sinalizador **\_ CACHEWRITE MRU** , chamar **FreeMRUList** fará com que todas as alterações ainda não gravadas na versão da lista MRU armazenada no registro sejam gravadas neste momento.</span><span class="sxs-lookup"><span data-stu-id="d6491-114">If the MRU list was created using the **MRU\_CACHEWRITE** flag, calling **FreeMRUList** causes any changes not yet written to the version of the MRU list stored in registry to be written at this time.</span></span>

<span data-ttu-id="d6491-115">Essa função não está incluída em um cabeçalho ou biblioteca pública.</span><span class="sxs-lookup"><span data-stu-id="d6491-115">This function is not included in a public header or library.</span></span> <span data-ttu-id="d6491-116">Ele deve ser extraído de comctl32.dll pelo ordinal 152.</span><span class="sxs-lookup"><span data-stu-id="d6491-116">It must be extracted from comctl32.dll by ordinal 152.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6491-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6491-117">Requirements</span></span>



| <span data-ttu-id="d6491-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6491-118">Requirement</span></span> | <span data-ttu-id="d6491-119">Valor</span><span class="sxs-lookup"><span data-stu-id="d6491-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6491-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d6491-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d6491-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d6491-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d6491-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d6491-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d6491-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d6491-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d6491-124">DLL</span><span class="sxs-lookup"><span data-stu-id="d6491-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6491-125"><dt>Comctl32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="d6491-125"><dt>Comctl32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




