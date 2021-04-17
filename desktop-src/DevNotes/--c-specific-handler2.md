---
description: Chamado pelo compilador para implementar extensões de manipulação de exceção estruturada.
ms.assetid: 6EAE0B4E-35E1-48EB-A8A9-0C1DC5387B03
title: Função __C_specific_handler (WDM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __C_specific_handler
- __C_specific_handler
api_type:
- DllExport
api_location:
- ntoskrnl.exe
- NTDll.dll
- wpdupfltr.sys
ms.openlocfilehash: fc89105a6a68c920fccb123dd95a08ed4ddee696
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754790"
---
# <a name="__c_specific_handler-function"></a><span data-ttu-id="d1690-103">\_\_Função de manipulador de C \_ específico \_</span><span class="sxs-lookup"><span data-stu-id="d1690-103">\_\_C\_specific\_handler function</span></span>

<span data-ttu-id="d1690-104">Chamado pelo compilador para implementar extensões de manipulação de exceção estruturada.</span><span class="sxs-lookup"><span data-stu-id="d1690-104">Called by the compiler to implement structured exception handling extensions.</span></span>

<span data-ttu-id="d1690-105">O endereço relativo do manipulador específico de idioma está presente nas informações de desenrolamento, \_ sempre que sinalizadores UNW \_ Flag \_ EHANDLER ou UNW \_ Flag \_ UHANDLER estão definidos.</span><span class="sxs-lookup"><span data-stu-id="d1690-105">The relative address of the language specific handler is present in the UNWIND\_INFO whenever flags UNW\_FLAG\_EHANDLER or UNW\_FLAG\_UHANDLER are set.</span></span> <span data-ttu-id="d1690-106">O manipulador de idioma específico é chamado como parte da pesquisa de um manipulador de exceção ou como parte de um desenrolamento.</span><span class="sxs-lookup"><span data-stu-id="d1690-106">The language specific handler is called as part of the search for an exception handler or as part of an unwind.</span></span> <span data-ttu-id="d1690-107">Para obter mais informações, consulte [manipulador de linguagem específica](/cpp/build/language-specific-handler).</span><span class="sxs-lookup"><span data-stu-id="d1690-107">For more information see [Language Specific Handler](/cpp/build/language-specific-handler).</span></span>

## <a name="syntax"></a><span data-ttu-id="d1690-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d1690-108">Syntax</span></span>


```C++
_CRTIMP  __C_specific_handler(
  _In_    struct _EXCEPTION_RECORD   *ExceptionRecord,
  _In_    void                       *EstablisherFrame,
  _Inout_ struct _CONTEXT            *ContextRecord,
  _Inout_ struct _DISPATCHER_CONTEXT *DispatcherContext
);
```



## <a name="parameters"></a><span data-ttu-id="d1690-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d1690-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1690-110">*ExceptionRecord* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d1690-110">*ExceptionRecord* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1690-111">Fornece um ponteiro para um registro de exceção que tem a definição padrão de Win64.</span><span class="sxs-lookup"><span data-stu-id="d1690-111">Supplies a pointer to an exception record, which has the standard Win64 definition.</span></span>

</dd> <dt>

<span data-ttu-id="d1690-112">*EstablisherFrame* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d1690-112">*EstablisherFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1690-113">O endereço da base da alocação de pilha fixa para esta função.</span><span class="sxs-lookup"><span data-stu-id="d1690-113">The address of the base of the fixed stack allocation for this function.</span></span>

</dd> <dt>

<span data-ttu-id="d1690-114">*ContextRecord* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="d1690-114">*ContextRecord* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d1690-115">Aponta para o contexto de exceção no momento em que a exceção foi gerada (no caso do manipulador de exceção) ou no contexto "desenrolar" atual (no caso do manipulador de terminação).</span><span class="sxs-lookup"><span data-stu-id="d1690-115">Points to the exception context at the time the exception was raised (in the exception handler case) or the current "unwind" context (in the termination handler case).</span></span>

</dd> <dt>

<span data-ttu-id="d1690-116">*DispatcherContext* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="d1690-116">*DispatcherContext* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d1690-117">Aponta para o contexto do Dispatcher para esta função.</span><span class="sxs-lookup"><span data-stu-id="d1690-117">Points to the dispatcher context for this function.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d1690-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1690-118">Requirements</span></span>



| <span data-ttu-id="d1690-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1690-119">Requirement</span></span> | <span data-ttu-id="d1690-120">Valor</span><span class="sxs-lookup"><span data-stu-id="d1690-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1690-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d1690-121">Header</span></span><br/>  | <dl> <span data-ttu-id="d1690-122"><dt>WDM. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1690-122"><dt>Wdm.h</dt></span></span> </dl>        |
| <span data-ttu-id="d1690-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d1690-123">Library</span></span><br/> | <dl> <span data-ttu-id="d1690-124"><dt>NtosKrnl. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d1690-124"><dt>NtosKrnl.lib</dt></span></span> </dl> |
| <span data-ttu-id="d1690-125">DLL</span><span class="sxs-lookup"><span data-stu-id="d1690-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="d1690-126"><dt>Ntoskrnl.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d1690-126"><dt>Ntoskrnl.exe</dt></span></span> </dl> |



 

