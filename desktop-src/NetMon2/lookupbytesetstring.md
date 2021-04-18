---
description: A função LookupByteSetString retorna a cadeia de caracteres correspondente ao valor especificado de um conjunto rotulado.
ms.assetid: 295891f9-dc8d-4dbe-aac9-7d0a96993cfa
title: Função LookupByteSetString (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LookupByteSetString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 7a2b5bffbfcb30ed8ec00da42fbc9ad6008fd5ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105778536"
---
# <a name="lookupbytesetstring-function"></a><span data-ttu-id="30f0b-103">Função LookupByteSetString</span><span class="sxs-lookup"><span data-stu-id="30f0b-103">LookupByteSetString function</span></span>

<span data-ttu-id="30f0b-104">A função **LookupByteSetString** retorna a cadeia de caracteres correspondente ao valor especificado de um conjunto rotulado.</span><span class="sxs-lookup"><span data-stu-id="30f0b-104">The **LookupByteSetString** function returns the string corresponding to the specified value of a labeled set.</span></span>

## <a name="syntax"></a><span data-ttu-id="30f0b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="30f0b-105">Syntax</span></span>


```C++
LPBYTE WINAPI LookupByteSetString(
   LPSET lpSet,
   BYTE  Value
);
```



## <a name="parameters"></a><span data-ttu-id="30f0b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="30f0b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30f0b-107">*lpSet*</span><span class="sxs-lookup"><span data-stu-id="30f0b-107">*lpSet*</span></span> 
</dt> <dd>

<span data-ttu-id="30f0b-108">Ponteiro para um conjunto rotulado, do qual você pode extrair o rótulo do valor.</span><span class="sxs-lookup"><span data-stu-id="30f0b-108">Pointer to a labeled set, from which you can extract the value's label.</span></span>

</dd> <dt>

<span data-ttu-id="30f0b-109">*Valor*</span><span class="sxs-lookup"><span data-stu-id="30f0b-109">*Value*</span></span> 
</dt> <dd>

<span data-ttu-id="30f0b-110">Valor de um conjunto rotulado.</span><span class="sxs-lookup"><span data-stu-id="30f0b-110">Value of a labeled set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30f0b-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="30f0b-111">Return value</span></span>

<span data-ttu-id="30f0b-112">Se a função for bem-sucedida, o valor de retorno será uma cadeia de caracteres correspondente ao valor fornecido.</span><span class="sxs-lookup"><span data-stu-id="30f0b-112">If the function is successful, the return value is a string corresponding to the value provided.</span></span>

<span data-ttu-id="30f0b-113">Se a função não for bem-sucedida, o valor de retorno será **nulo**.</span><span class="sxs-lookup"><span data-stu-id="30f0b-113">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="30f0b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30f0b-114">Requirements</span></span>



| <span data-ttu-id="30f0b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="30f0b-115">Requirement</span></span> | <span data-ttu-id="30f0b-116">Valor</span><span class="sxs-lookup"><span data-stu-id="30f0b-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="30f0b-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="30f0b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="30f0b-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="30f0b-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="30f0b-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="30f0b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="30f0b-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="30f0b-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="30f0b-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="30f0b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="30f0b-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="30f0b-122"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="30f0b-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="30f0b-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="30f0b-124"><dt>Parser. lib</dt></span><span class="sxs-lookup"><span data-stu-id="30f0b-124"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="30f0b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="30f0b-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30f0b-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30f0b-126"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




