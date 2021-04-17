---
description: A função LookupWordSetString retorna a cadeia de caracteres correspondente ao valor solicitado de um conjunto rotulado.
ms.assetid: e8d158a1-8544-4c10-b8e8-46888c1097e4
title: Função LookupWordSetString (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LookupWordSetString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 7487becb195571e1eb88044195293b2c0b226e8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501892"
---
# <a name="lookupwordsetstring-function"></a><span data-ttu-id="a44fa-103">Função LookupWordSetString</span><span class="sxs-lookup"><span data-stu-id="a44fa-103">LookupWordSetString function</span></span>

<span data-ttu-id="a44fa-104">A função **LookupWordSetString** retorna a cadeia de caracteres correspondente ao valor solicitado de um conjunto rotulado.</span><span class="sxs-lookup"><span data-stu-id="a44fa-104">The **LookupWordSetString** function returns the string corresponding to the requested value from a labeled set.</span></span>

## <a name="syntax"></a><span data-ttu-id="a44fa-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a44fa-105">Syntax</span></span>


```C++
LPBYTE WINAPI LookupWordSetString(
   LPSET lpSet,
   WORD  Value
);
```



## <a name="parameters"></a><span data-ttu-id="a44fa-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a44fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a44fa-107">*lpSet*</span><span class="sxs-lookup"><span data-stu-id="a44fa-107">*lpSet*</span></span> 
</dt> <dd>

<span data-ttu-id="a44fa-108">Rótulo definido a partir do qual você extrai o rótulo do valor.</span><span class="sxs-lookup"><span data-stu-id="a44fa-108">Labeled set from which you extract the value's label.</span></span>

</dd> <dt>

<span data-ttu-id="a44fa-109">*Valor*</span><span class="sxs-lookup"><span data-stu-id="a44fa-109">*Value*</span></span> 
</dt> <dd>

<span data-ttu-id="a44fa-110">Valor de um conjunto rotulado.</span><span class="sxs-lookup"><span data-stu-id="a44fa-110">Value of a labeled set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a44fa-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a44fa-111">Return value</span></span>

<span data-ttu-id="a44fa-112">Se a função for bem-sucedida, o valor de retorno será uma cadeia de caracteres que corresponde ao valor solicitado.</span><span class="sxs-lookup"><span data-stu-id="a44fa-112">If the function is successful, the return value is a string that corresponds to the requested value.</span></span>

<span data-ttu-id="a44fa-113">Se a função não for bem-sucedida, o valor especificado não estará no conjunto, o valor de retorno será **nulo**.</span><span class="sxs-lookup"><span data-stu-id="a44fa-113">If the function is unsuccessful, the specified value is not in the set, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a44fa-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a44fa-114">Requirements</span></span>



| <span data-ttu-id="a44fa-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a44fa-115">Requirement</span></span> | <span data-ttu-id="a44fa-116">Valor</span><span class="sxs-lookup"><span data-stu-id="a44fa-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a44fa-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a44fa-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a44fa-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a44fa-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="a44fa-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a44fa-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a44fa-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a44fa-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a44fa-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a44fa-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a44fa-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="a44fa-122"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="a44fa-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a44fa-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="a44fa-124"><dt>Parser. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a44fa-124"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="a44fa-125">DLL</span><span class="sxs-lookup"><span data-stu-id="a44fa-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a44fa-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a44fa-126"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




