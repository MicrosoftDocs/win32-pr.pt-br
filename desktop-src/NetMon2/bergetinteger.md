---
description: A função BERGetInteger decodifica um inteiro codificado no BER.
ms.assetid: 1ab0dcec-05cf-4322-a44e-28aa9131495a
title: Função BERGetInteger (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BERGetInteger
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: c89cd5e3f4e4eb35157936f990939154f23966d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829343"
---
# <a name="bergetinteger-function"></a><span data-ttu-id="e1980-103">Função BERGetInteger</span><span class="sxs-lookup"><span data-stu-id="e1980-103">BERGetInteger function</span></span>

<span data-ttu-id="e1980-104">A função **BERGetInteger** decodifica um inteiro codificado no ber.</span><span class="sxs-lookup"><span data-stu-id="e1980-104">The **BERGetInteger** function decodes a BER-encoded integer.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1980-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e1980-105">Syntax</span></span>


```C++
BOOL BERGetInteger(
   LPBYTE  pCurrentPointer,
   LPBYTE  *ppValuePointer,
   LPDWORD pHeaderLength,
   LPDWORD pDataLength,
   LPBYTE  *ppNext
);
```



## <a name="parameters"></a><span data-ttu-id="e1980-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e1980-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1980-107">*pCurrentPointer*</span><span class="sxs-lookup"><span data-stu-id="e1980-107">*pCurrentPointer*</span></span> 
</dt> <dd>

<span data-ttu-id="e1980-108">Ponteiro para o número inteiro que é decodificado.</span><span class="sxs-lookup"><span data-stu-id="e1980-108">Pointer to the integer that is decoded.</span></span>

</dd> <dt>

<span data-ttu-id="e1980-109">*ppValuePointer*</span><span class="sxs-lookup"><span data-stu-id="e1980-109">*ppValuePointer*</span></span> 
</dt> <dd>

<span data-ttu-id="e1980-110">Ponteiro para o ponteiro para o valor retornado.</span><span class="sxs-lookup"><span data-stu-id="e1980-110">Pointer to the pointer to returned value.</span></span>

</dd> <dt>

<span data-ttu-id="e1980-111">*pHeaderLength*</span><span class="sxs-lookup"><span data-stu-id="e1980-111">*pHeaderLength*</span></span> 
</dt> <dd>

<span data-ttu-id="e1980-112">Ponteiro para o comprimento do cabeçalho retornado.</span><span class="sxs-lookup"><span data-stu-id="e1980-112">Pointer to the returned header length.</span></span>

</dd> <dt>

<span data-ttu-id="e1980-113">*pDataLength*</span><span class="sxs-lookup"><span data-stu-id="e1980-113">*pDataLength*</span></span> 
</dt> <dd>

<span data-ttu-id="e1980-114">Ponteiro para o comprimento dos dados.</span><span class="sxs-lookup"><span data-stu-id="e1980-114">Pointer to the data length.</span></span>

</dd> <dt>

<span data-ttu-id="e1980-115">*ppNext*</span><span class="sxs-lookup"><span data-stu-id="e1980-115">*ppNext*</span></span> 
</dt> <dd>

<span data-ttu-id="e1980-116">Ponteiro para o ponteiro para a próxima entrada do BER.</span><span class="sxs-lookup"><span data-stu-id="e1980-116">Pointer to the pointer to the next BER entry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1980-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e1980-117">Return value</span></span>

<span data-ttu-id="e1980-118">Se a função for bem-sucedida (ou seja, se um inteiro codificado válido do BER for encontrado e convertido), o valor de retorno será **true**.</span><span class="sxs-lookup"><span data-stu-id="e1980-118">If the function is successful (that is, if a valid BER encoded integer is found and converted), the return value is **TRUE**.</span></span>

<span data-ttu-id="e1980-119">Se a função não for bem-sucedida, o valor de retorno será **false**.</span><span class="sxs-lookup"><span data-stu-id="e1980-119">If function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1980-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1980-120">Requirements</span></span>



| <span data-ttu-id="e1980-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1980-121">Requirement</span></span> | <span data-ttu-id="e1980-122">Valor</span><span class="sxs-lookup"><span data-stu-id="e1980-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e1980-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e1980-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e1980-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e1980-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="e1980-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e1980-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e1980-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e1980-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e1980-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e1980-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1980-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1980-128"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="e1980-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e1980-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="e1980-130"><dt>Parser. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e1980-130"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="e1980-131">DLL</span><span class="sxs-lookup"><span data-stu-id="e1980-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1980-132"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1980-132"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




