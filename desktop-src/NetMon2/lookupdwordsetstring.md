---
description: A função LookupDwordSetString retorna a cadeia de caracteres correspondente ao valor especificado de um conjunto rotulado.
ms.assetid: ee2b1b7a-6b64-4c8c-a71d-de970b66d46e
title: Função LookupDwordSetString (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LookupDwordSetString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 57688edab7421f939e03322b8b244219b00d31fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647321"
---
# <a name="lookupdwordsetstring-function"></a><span data-ttu-id="e35f2-103">Função LookupDwordSetString</span><span class="sxs-lookup"><span data-stu-id="e35f2-103">LookupDwordSetString function</span></span>

<span data-ttu-id="e35f2-104">A função **LookupDwordSetString** retorna a cadeia de caracteres correspondente ao valor especificado de um conjunto rotulado.</span><span class="sxs-lookup"><span data-stu-id="e35f2-104">The **LookupDwordSetString** function returns the string corresponding to the specified value of a labeled set.</span></span>

## <a name="syntax"></a><span data-ttu-id="e35f2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e35f2-105">Syntax</span></span>


```C++
LPBYTE WINAPI LookupDwordSetString(
   LPSET lpSet,
   DWORD Value
);
```



## <a name="parameters"></a><span data-ttu-id="e35f2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e35f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e35f2-107">*lpSet*</span><span class="sxs-lookup"><span data-stu-id="e35f2-107">*lpSet*</span></span> 
</dt> <dd>

<span data-ttu-id="e35f2-108">Conjunto rotulado, do qual você pode extrair o rótulo do valor.</span><span class="sxs-lookup"><span data-stu-id="e35f2-108">Labeled set, from which you can extract the value's label.</span></span>

</dd> <dt>

<span data-ttu-id="e35f2-109">*Valor*</span><span class="sxs-lookup"><span data-stu-id="e35f2-109">*Value*</span></span> 
</dt> <dd>

<span data-ttu-id="e35f2-110">Valor de um conjunto rotulado.</span><span class="sxs-lookup"><span data-stu-id="e35f2-110">Value of a labeled set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e35f2-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e35f2-111">Return value</span></span>

<span data-ttu-id="e35f2-112">Se a função for bem-sucedida, o valor de retorno será a cadeia de caracteres que corresponde ao valor especificado.</span><span class="sxs-lookup"><span data-stu-id="e35f2-112">If the function is successful, the return value is the string that corresponds to the specified value.</span></span>

<span data-ttu-id="e35f2-113">Se a função não for bem-sucedida, o valor especificado não estará no conjunto, o valor de retorno será **nulo**.</span><span class="sxs-lookup"><span data-stu-id="e35f2-113">If the function is unsuccessful, the specified value is not in the set, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e35f2-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e35f2-114">Requirements</span></span>



| <span data-ttu-id="e35f2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e35f2-115">Requirement</span></span> | <span data-ttu-id="e35f2-116">Valor</span><span class="sxs-lookup"><span data-stu-id="e35f2-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e35f2-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e35f2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e35f2-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e35f2-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="e35f2-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e35f2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e35f2-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e35f2-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e35f2-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e35f2-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e35f2-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e35f2-122"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="e35f2-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e35f2-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="e35f2-124"><dt>Parser. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e35f2-124"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="e35f2-125">DLL</span><span class="sxs-lookup"><span data-stu-id="e35f2-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e35f2-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e35f2-126"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




