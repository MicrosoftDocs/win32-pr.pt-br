---
description: A função VarLenSmallIntToDword converte um inteiro pequeno de comprimento variável em um DWORD.
ms.assetid: e26dc206-ac85-4346-9fcf-93ebc8948ced
title: Função VarLenSmallIntToDword (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VarLenSmallIntToDword
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 4b0e2fa0813c4b384b17ea45af45f9938bcd85c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810154"
---
# <a name="varlensmallinttodword-function"></a><span data-ttu-id="3732e-103">Função VarLenSmallIntToDword</span><span class="sxs-lookup"><span data-stu-id="3732e-103">VarLenSmallIntToDword function</span></span>

<span data-ttu-id="3732e-104">A função **VarLenSmallIntToDword** converte um inteiro pequeno de comprimento variável em um **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="3732e-104">The **VarLenSmallIntToDword** function converts a variable-length, small integer to a **DWORD**.</span></span>

## <a name="syntax"></a><span data-ttu-id="3732e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3732e-105">Syntax</span></span>


```C++
LPDWORD WINAPI VarLenSmallIntToDword(
   LPBYTE  pValue,
   WORD    ValueLen,
   BOOL    fIsByteswapped,
   LPDWORD lpDword
);
```



## <a name="parameters"></a><span data-ttu-id="3732e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3732e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3732e-107">*Valores*</span><span class="sxs-lookup"><span data-stu-id="3732e-107">*pValue*</span></span> 
</dt> <dd>

<span data-ttu-id="3732e-108">Ponteiro para o inteiro de comprimento variável e pequeno.</span><span class="sxs-lookup"><span data-stu-id="3732e-108">Pointer to the variable-length, small integer.</span></span>

</dd> <dt>

<span data-ttu-id="3732e-109">*ValueLen*</span><span class="sxs-lookup"><span data-stu-id="3732e-109">*ValueLen*</span></span> 
</dt> <dd>

<span data-ttu-id="3732e-110">Comprimento (em bytes) do comprimento variável, inteiro pequeno.</span><span class="sxs-lookup"><span data-stu-id="3732e-110">Length (in bytes) of the variable-length, small integer .</span></span>

</dd> <dt>

<span data-ttu-id="3732e-111">*fIsByteswapped*</span><span class="sxs-lookup"><span data-stu-id="3732e-111">*fIsByteswapped*</span></span> 
</dt> <dd>

<span data-ttu-id="3732e-112">Sinalizador que indica se o inteiro pequeno de comprimento variável é alternado por byte.</span><span class="sxs-lookup"><span data-stu-id="3732e-112">Flag that indicates whether the variable length small integer is byte-swapped.</span></span>

</dd> <dt>

<span data-ttu-id="3732e-113">*lpDword*</span><span class="sxs-lookup"><span data-stu-id="3732e-113">*lpDword*</span></span> 
</dt> <dd>

<span data-ttu-id="3732e-114">O **DWORD** para o qual o inteiro é convertido.</span><span class="sxs-lookup"><span data-stu-id="3732e-114">The **DWORD** that the integer is converted to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3732e-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3732e-115">Return value</span></span>

<span data-ttu-id="3732e-116">O valor de retorno é um ponteiro para o **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="3732e-116">The return value is a pointer to the **DWORD**.</span></span>

## <a name="requirements"></a><span data-ttu-id="3732e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3732e-117">Requirements</span></span>



| <span data-ttu-id="3732e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="3732e-118">Requirement</span></span> | <span data-ttu-id="3732e-119">Valor</span><span class="sxs-lookup"><span data-stu-id="3732e-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3732e-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3732e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3732e-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3732e-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="3732e-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3732e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3732e-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3732e-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3732e-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3732e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3732e-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="3732e-125"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="3732e-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3732e-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="3732e-127"><dt>Parser. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3732e-127"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="3732e-128">DLL</span><span class="sxs-lookup"><span data-stu-id="3732e-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3732e-129"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3732e-129"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




