---
description: A função FilterAddObject adiciona um único objeto a um filtro de exibição.
ms.assetid: 796216f4-a407-4a8c-98b3-8c3761d91913
title: Função FilterAddObject (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FilterAddObject
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 7fc6c41a675bfe560c060e271e4f9f48f88cd58c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104460962"
---
# <a name="filteraddobject-function"></a><span data-ttu-id="e5812-103">Função FilterAddObject</span><span class="sxs-lookup"><span data-stu-id="e5812-103">FilterAddObject function</span></span>

<span data-ttu-id="e5812-104">A função **FilterAddObject** adiciona um único objeto a um [*filtro de exibição*](d.md).</span><span class="sxs-lookup"><span data-stu-id="e5812-104">The **FilterAddObject** function adds a single object to a [*display filter*](d.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e5812-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e5812-105">Syntax</span></span>


```C++
DWORD WINAPI FilterAddObject(
  _In_  HFILTER        hFilter,
  _Out_ LPFILTEROBJECT lpFilterObject
);
```



## <a name="parameters"></a><span data-ttu-id="e5812-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e5812-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5812-107">*hFilter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e5812-107">*hFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5812-108">Identificador para o filtro de exibição.</span><span class="sxs-lookup"><span data-stu-id="e5812-108">Handle to the display filter.</span></span>

</dd> <dt>

<span data-ttu-id="e5812-109">*lpFilterObject* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e5812-109">*lpFilterObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5812-110">Ponteiro para uma estrutura [filterobject](filterobject.md) que define o objeto a ser adicionado ao filtro.</span><span class="sxs-lookup"><span data-stu-id="e5812-110">Pointer to a [FILTEROBJECT](filterobject.md) structure that defines the object to be added to the filter.</span></span> <span data-ttu-id="e5812-111">Cada objeto pode ser um operador, valor ou propriedade.</span><span class="sxs-lookup"><span data-stu-id="e5812-111">Each object can be an operator, value, or property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5812-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e5812-112">Return value</span></span>

<span data-ttu-id="e5812-113">Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="e5812-113">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="e5812-114">Se a função não for bem-sucedida, o valor de retorno será um código de erro.</span><span class="sxs-lookup"><span data-stu-id="e5812-114">If the function is unsuccessful, the return value is an error code.</span></span>



| <span data-ttu-id="e5812-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="e5812-115">Return code</span></span>                                                                                              | <span data-ttu-id="e5812-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="e5812-116">Description</span></span>                                                                  |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e5812-117"><dt>**NMERR \_ \_ parâmetro inválido**</dt></span><span class="sxs-lookup"><span data-stu-id="e5812-117"><dt>**NMERR\_INVALID\_PARAMETER**</dt></span></span> </dl> | <span data-ttu-id="e5812-118">O parâmetro *hFilter* tem um valor inválido.</span><span class="sxs-lookup"><span data-stu-id="e5812-118">The *hFilter* parameter has an invalid value.</span></span><br/>                     |
| <dl> <span data-ttu-id="e5812-119"><dt>**NMERR \_ \_ de \_ memória insuficiente**</dt></span><span class="sxs-lookup"><span data-stu-id="e5812-119"><dt>**NMERR\_OUT\_OF\_MEMORY**</dt></span></span> </dl>    | <span data-ttu-id="e5812-120">Monitor de Rede não tem memória suficiente para criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="e5812-120">Network Monitor does not have enough memory to create the object.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e5812-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="e5812-121">Remarks</span></span>

<span data-ttu-id="e5812-122">Os [*especialistas*](e.md) e os [*analisadores*](p.md) podem chamar a função **FilterAddObject** .</span><span class="sxs-lookup"><span data-stu-id="e5812-122">[*Experts*](e.md) and [*parsers*](p.md) can call the **FilterAddObject** function.</span></span>

<span data-ttu-id="e5812-123">A função **FilterAddObject** é chamada cada vez que um objeto de filtro é adicionado ao filtro de exibição.</span><span class="sxs-lookup"><span data-stu-id="e5812-123">The **FilterAddObject** function is called each time a filter object is added to the display filter.</span></span> <span data-ttu-id="e5812-124">O filtro de exibição é uma pilha de sufixo de objetos que podem ser um operador, valor ou propriedade.</span><span class="sxs-lookup"><span data-stu-id="e5812-124">The display filter is a postfix stack of objects that can be an operator, value, or property.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5812-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5812-125">Requirements</span></span>



| <span data-ttu-id="e5812-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5812-126">Requirement</span></span> | <span data-ttu-id="e5812-127">Valor</span><span class="sxs-lookup"><span data-stu-id="e5812-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e5812-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5812-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e5812-129">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e5812-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="e5812-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5812-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e5812-131">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e5812-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e5812-132">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e5812-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5812-133"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5812-133"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="e5812-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e5812-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="e5812-135"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e5812-135"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="e5812-136">DLL</span><span class="sxs-lookup"><span data-stu-id="e5812-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5812-137"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5812-137"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5812-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="e5812-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5812-139">FILTERobject</span><span class="sxs-lookup"><span data-stu-id="e5812-139">FILTEROBJECT</span></span>](filterobject.md)
</dt> </dl>

 

 




