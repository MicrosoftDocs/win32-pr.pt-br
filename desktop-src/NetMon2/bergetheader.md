---
description: A função BERGetHeader decodifica um cabeçalho Choice.
ms.assetid: 2574a9b3-c28e-43d1-904f-d45888617584
title: Função BERGetHeader (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BERGetHeader
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 5e2213b15b6b4d2cbaa15b3b9aa9de028e20a62d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766365"
---
# <a name="bergetheader-function"></a><span data-ttu-id="05168-103">Função BERGetHeader</span><span class="sxs-lookup"><span data-stu-id="05168-103">BERGetHeader function</span></span>

<span data-ttu-id="05168-104">A função **BERGetHeader** decodifica um cabeçalho Choice.</span><span class="sxs-lookup"><span data-stu-id="05168-104">The **BERGetHeader** function decodes a choice header.</span></span>

## <a name="syntax"></a><span data-ttu-id="05168-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="05168-105">Syntax</span></span>


```C++
BOOL BERGetHeader(
   LPBYTE  pCurrentPointer,
   LPBYTE  pTag,
   LPDWORD pHeaderLength,
   LPDWORD pDataLength,
   LPBYTE  *ppNext
);
```



## <a name="parameters"></a><span data-ttu-id="05168-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="05168-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05168-107">*pCurrentPointer*</span><span class="sxs-lookup"><span data-stu-id="05168-107">*pCurrentPointer*</span></span> 
</dt> <dd>

<span data-ttu-id="05168-108">Ponteiro para o cabeçalho Choice.</span><span class="sxs-lookup"><span data-stu-id="05168-108">Pointer to the choice header.</span></span>

</dd> <dt>

<span data-ttu-id="05168-109">*pTag*</span><span class="sxs-lookup"><span data-stu-id="05168-109">*pTag*</span></span> 
</dt> <dd>

<span data-ttu-id="05168-110">Ponteiro para a marca retornada.</span><span class="sxs-lookup"><span data-stu-id="05168-110">Pointer to the returned tag.</span></span>

</dd> <dt>

<span data-ttu-id="05168-111">*pHeaderLength*</span><span class="sxs-lookup"><span data-stu-id="05168-111">*pHeaderLength*</span></span> 
</dt> <dd>

<span data-ttu-id="05168-112">Ponteiro para o comprimento do cabeçalho retornado.</span><span class="sxs-lookup"><span data-stu-id="05168-112">Pointer to the returned header length.</span></span>

</dd> <dt>

<span data-ttu-id="05168-113">*pDataLength*</span><span class="sxs-lookup"><span data-stu-id="05168-113">*pDataLength*</span></span> 
</dt> <dd>

<span data-ttu-id="05168-114">Ponteiro para o comprimento dos dados retornados.</span><span class="sxs-lookup"><span data-stu-id="05168-114">Pointer to the returned data length.</span></span>

</dd> <dt>

<span data-ttu-id="05168-115">*ppNext*</span><span class="sxs-lookup"><span data-stu-id="05168-115">*ppNext*</span></span> 
</dt> <dd>

<span data-ttu-id="05168-116">Ponteiro para o conteúdo do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="05168-116">Pointer to the header contents.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05168-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="05168-117">Return value</span></span>

<span data-ttu-id="05168-118">Se a função for bem-sucedida (ou seja, um cabeçalho de escolha válido do BER for encontrado) o valor de retorno será **true**.</span><span class="sxs-lookup"><span data-stu-id="05168-118">If the function is successful (that is, a valid BER choice header is found) the return value is **TRUE**.</span></span>

<span data-ttu-id="05168-119">Se a função não for bem-sucedida, o valor de retorno será **false**.</span><span class="sxs-lookup"><span data-stu-id="05168-119">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="05168-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05168-120">Requirements</span></span>



| <span data-ttu-id="05168-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="05168-121">Requirement</span></span> | <span data-ttu-id="05168-122">Valor</span><span class="sxs-lookup"><span data-stu-id="05168-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="05168-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="05168-123">Minimum supported client</span></span><br/> | <span data-ttu-id="05168-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="05168-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="05168-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="05168-125">Minimum supported server</span></span><br/> | <span data-ttu-id="05168-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="05168-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="05168-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="05168-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="05168-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="05168-128"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="05168-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="05168-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="05168-130"><dt>Parser. lib</dt></span><span class="sxs-lookup"><span data-stu-id="05168-130"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="05168-131">DLL</span><span class="sxs-lookup"><span data-stu-id="05168-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05168-132"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05168-132"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




