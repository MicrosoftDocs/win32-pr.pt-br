---
description: A função BERGetString decodifica uma cadeia de caracteres codificada em BER.
ms.assetid: 1f72f061-c0ed-4634-9709-e08c2b9468bb
title: Função BERGetString (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BERGetString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 6f8f864b8042ad49502ae53061e157575192e7bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828232"
---
# <a name="bergetstring-function"></a><span data-ttu-id="8dafa-103">Função BERGetString</span><span class="sxs-lookup"><span data-stu-id="8dafa-103">BERGetString function</span></span>

<span data-ttu-id="8dafa-104">A função **BERGetString** decodifica uma cadeia de caracteres codificada em ber.</span><span class="sxs-lookup"><span data-stu-id="8dafa-104">The **BERGetString** function decodes a BER-encoded string.</span></span>

## <a name="syntax"></a><span data-ttu-id="8dafa-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8dafa-105">Syntax</span></span>


```C++
BOOL BERGetString(
   LPBYTE  pCurrentPointer,
   LPBYTE  *ppValuePointer,
   LPDWORD pHeaderLength,
   LPDWORD pDataLength,
   LPBYTE  *ppNext
);
```



## <a name="parameters"></a><span data-ttu-id="8dafa-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8dafa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8dafa-107">*pCurrentPointer*</span><span class="sxs-lookup"><span data-stu-id="8dafa-107">*pCurrentPointer*</span></span> 
</dt> <dd>

<span data-ttu-id="8dafa-108">Ponteiro para a cadeia de caracteres decodificada.</span><span class="sxs-lookup"><span data-stu-id="8dafa-108">Pointer to the string that is decoded.</span></span>

</dd> <dt>

<span data-ttu-id="8dafa-109">*ppValuePointer*</span><span class="sxs-lookup"><span data-stu-id="8dafa-109">*ppValuePointer*</span></span> 
</dt> <dd>

<span data-ttu-id="8dafa-110">Ponteiro para o ponteiro da cadeia de caracteres decodificada.</span><span class="sxs-lookup"><span data-stu-id="8dafa-110">Pointer to the pointer of the decoded string.</span></span>

</dd> <dt>

<span data-ttu-id="8dafa-111">*pHeaderLength*</span><span class="sxs-lookup"><span data-stu-id="8dafa-111">*pHeaderLength*</span></span> 
</dt> <dd>

<span data-ttu-id="8dafa-112">Ponteiro para o comprimento do cabeçalho retornado.</span><span class="sxs-lookup"><span data-stu-id="8dafa-112">Pointer to the returned header length.</span></span>

</dd> <dt>

<span data-ttu-id="8dafa-113">*pDataLength*</span><span class="sxs-lookup"><span data-stu-id="8dafa-113">*pDataLength*</span></span> 
</dt> <dd>

<span data-ttu-id="8dafa-114">Ponteiro para o comprimento da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="8dafa-114">Pointer to the string length.</span></span>

</dd> <dt>

<span data-ttu-id="8dafa-115">*ppNext*</span><span class="sxs-lookup"><span data-stu-id="8dafa-115">*ppNext*</span></span> 
</dt> <dd>

<span data-ttu-id="8dafa-116">Ponteiro para o ponteiro da próxima entrada do BER.</span><span class="sxs-lookup"><span data-stu-id="8dafa-116">Pointer to the pointer of the next BER entry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8dafa-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8dafa-117">Return value</span></span>

<span data-ttu-id="8dafa-118">Se a função for bem-sucedida (ou seja, se uma cadeia de caracteres codificada em BER válida for decodificada), o valor de retorno será **true**.</span><span class="sxs-lookup"><span data-stu-id="8dafa-118">If the function is successful (that is, if a valid BER-encoded string is decoded), the return value is **TRUE**.</span></span>

<span data-ttu-id="8dafa-119">Se a função não for bem-sucedida, o valor de retorno será **false**.</span><span class="sxs-lookup"><span data-stu-id="8dafa-119">If function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8dafa-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8dafa-120">Requirements</span></span>



| <span data-ttu-id="8dafa-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="8dafa-121">Requirement</span></span> | <span data-ttu-id="8dafa-122">Valor</span><span class="sxs-lookup"><span data-stu-id="8dafa-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8dafa-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8dafa-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8dafa-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8dafa-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="8dafa-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8dafa-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8dafa-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8dafa-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8dafa-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8dafa-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="8dafa-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="8dafa-128"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="8dafa-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8dafa-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="8dafa-130"><dt>Parser. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8dafa-130"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="8dafa-131">DLL</span><span class="sxs-lookup"><span data-stu-id="8dafa-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8dafa-132"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8dafa-132"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




