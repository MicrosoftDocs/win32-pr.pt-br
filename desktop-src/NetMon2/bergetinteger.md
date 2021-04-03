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
# <a name="bergetinteger-function"></a><span data-ttu-id="c22d2-103">Função BERGetInteger</span><span class="sxs-lookup"><span data-stu-id="c22d2-103">BERGetInteger function</span></span>

<span data-ttu-id="c22d2-104">A função **BERGetInteger** decodifica um inteiro codificado no ber.</span><span class="sxs-lookup"><span data-stu-id="c22d2-104">The **BERGetInteger** function decodes a BER-encoded integer.</span></span>

## <a name="syntax"></a><span data-ttu-id="c22d2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c22d2-105">Syntax</span></span>


```C++
BOOL BERGetInteger(
   LPBYTE  pCurrentPointer,
   LPBYTE  *ppValuePointer,
   LPDWORD pHeaderLength,
   LPDWORD pDataLength,
   LPBYTE  *ppNext
);
```



## <a name="parameters"></a><span data-ttu-id="c22d2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c22d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c22d2-107">*pCurrentPointer*</span><span class="sxs-lookup"><span data-stu-id="c22d2-107">*pCurrentPointer*</span></span> 
</dt> <dd>

<span data-ttu-id="c22d2-108">Ponteiro para o número inteiro que é decodificado.</span><span class="sxs-lookup"><span data-stu-id="c22d2-108">Pointer to the integer that is decoded.</span></span>

</dd> <dt>

<span data-ttu-id="c22d2-109">*ppValuePointer*</span><span class="sxs-lookup"><span data-stu-id="c22d2-109">*ppValuePointer*</span></span> 
</dt> <dd>

<span data-ttu-id="c22d2-110">Ponteiro para o ponteiro para o valor retornado.</span><span class="sxs-lookup"><span data-stu-id="c22d2-110">Pointer to the pointer to returned value.</span></span>

</dd> <dt>

<span data-ttu-id="c22d2-111">*pHeaderLength*</span><span class="sxs-lookup"><span data-stu-id="c22d2-111">*pHeaderLength*</span></span> 
</dt> <dd>

<span data-ttu-id="c22d2-112">Ponteiro para o comprimento do cabeçalho retornado.</span><span class="sxs-lookup"><span data-stu-id="c22d2-112">Pointer to the returned header length.</span></span>

</dd> <dt>

<span data-ttu-id="c22d2-113">*pDataLength*</span><span class="sxs-lookup"><span data-stu-id="c22d2-113">*pDataLength*</span></span> 
</dt> <dd>

<span data-ttu-id="c22d2-114">Ponteiro para o comprimento dos dados.</span><span class="sxs-lookup"><span data-stu-id="c22d2-114">Pointer to the data length.</span></span>

</dd> <dt>

<span data-ttu-id="c22d2-115">*ppNext*</span><span class="sxs-lookup"><span data-stu-id="c22d2-115">*ppNext*</span></span> 
</dt> <dd>

<span data-ttu-id="c22d2-116">Ponteiro para o ponteiro para a próxima entrada do BER.</span><span class="sxs-lookup"><span data-stu-id="c22d2-116">Pointer to the pointer to the next BER entry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c22d2-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c22d2-117">Return value</span></span>

<span data-ttu-id="c22d2-118">Se a função for bem-sucedida (ou seja, se um inteiro codificado válido do BER for encontrado e convertido), o valor de retorno será **true**.</span><span class="sxs-lookup"><span data-stu-id="c22d2-118">If the function is successful (that is, if a valid BER encoded integer is found and converted), the return value is **TRUE**.</span></span>

<span data-ttu-id="c22d2-119">Se a função não for bem-sucedida, o valor de retorno será **false**.</span><span class="sxs-lookup"><span data-stu-id="c22d2-119">If function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c22d2-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c22d2-120">Requirements</span></span>



| <span data-ttu-id="c22d2-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c22d2-121">Requirement</span></span> | <span data-ttu-id="c22d2-122">Valor</span><span class="sxs-lookup"><span data-stu-id="c22d2-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c22d2-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c22d2-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c22d2-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c22d2-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="c22d2-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c22d2-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c22d2-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c22d2-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c22d2-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c22d2-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c22d2-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c22d2-128"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="c22d2-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c22d2-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="c22d2-130"><dt>Parser. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c22d2-130"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="c22d2-131">DLL</span><span class="sxs-lookup"><span data-stu-id="c22d2-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c22d2-132"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c22d2-132"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




