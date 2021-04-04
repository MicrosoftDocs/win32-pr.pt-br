---
description: Recupera uma descrição independente de computador de uma exceção e informações sobre o estado do computador que existe para o thread quando a exceção ocorre. Essa função pode ser chamada somente de dentro da expressão de filtro de um manipulador de exceção.
ms.assetid: e982794a-d5f1-4fb4-a2b9-aa8da18cb8ae
title: Macro GetExceptionInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetExceptionInformation
api_type:
- NA
api_location: ''
ms.openlocfilehash: 243831a94a26b86df29d3a50413bfa9d6830a0e3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646497"
---
# <a name="getexceptioninformation-macro"></a><span data-ttu-id="abcf7-104">Macro GetExceptionInformation</span><span class="sxs-lookup"><span data-stu-id="abcf7-104">GetExceptionInformation macro</span></span>

<span data-ttu-id="abcf7-105">Recupera uma descrição independente de computador de uma exceção e informações sobre o estado do computador que existe para o thread quando a exceção ocorre.</span><span class="sxs-lookup"><span data-stu-id="abcf7-105">Retrieves a computer-independent description of an exception, and information about the computer state that exists for the thread when the exception occurs.</span></span> <span data-ttu-id="abcf7-106">Essa função pode ser chamada somente de dentro da expressão de filtro de um manipulador de exceção.</span><span class="sxs-lookup"><span data-stu-id="abcf7-106">This function can be called only from within the filter expression of an exception handler.</span></span>

> [!Note]  
> <span data-ttu-id="abcf7-107">O compilador de otimização do Microsoft C/C++ interpreta essa função como uma palavra-chave e seu uso fora da sintaxe apropriada de tratamento de exceção gera um erro de compilador.</span><span class="sxs-lookup"><span data-stu-id="abcf7-107">The Microsoft C/C++ Optimizing Compiler interprets this function as a keyword, and its use outside the appropriate exception-handling syntax generates a compiler error.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="abcf7-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="abcf7-108">Syntax</span></span>


```C++
LPEXCEPTION_POINTERS GetExceptionInformation(void);
```



## <a name="parameters"></a><span data-ttu-id="abcf7-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="abcf7-109">Parameters</span></span>

<span data-ttu-id="abcf7-110">Esta macro não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="abcf7-110">This macro has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="abcf7-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="abcf7-111">Return value</span></span>

<span data-ttu-id="abcf7-112">Um ponteiro para uma [**exceção \_ aponta**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) para uma estrutura que contém ponteiros para as duas estruturas a seguir:</span><span class="sxs-lookup"><span data-stu-id="abcf7-112">A pointer to an [**EXCEPTION\_POINTERS**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) structure that contains pointers to the following two structures:</span></span>

-   <span data-ttu-id="abcf7-113">[**Exceção \_**](/windows/desktop/api/WinNT/ns-winnt-exception_record) Estrutura de registro que contém uma descrição da exceção.</span><span class="sxs-lookup"><span data-stu-id="abcf7-113">[**EXCEPTION\_RECORD**](/windows/desktop/api/WinNT/ns-winnt-exception_record) structure that contains a description of the exception.</span></span>
-   <span data-ttu-id="abcf7-114">Estrutura de [**contexto**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) que contém as informações de estado do computador.</span><span class="sxs-lookup"><span data-stu-id="abcf7-114">[**CONTEXT**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) structure that contains the computer state information.</span></span>

## <a name="remarks"></a><span data-ttu-id="abcf7-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="abcf7-115">Remarks</span></span>

<span data-ttu-id="abcf7-116">A expressão de filtro (da qual a função é chamada) é avaliada se ocorre uma exceção durante a execução do bloco **\_ \_ try** e determina se o bloco **\_ \_ Except** será ou não executado.</span><span class="sxs-lookup"><span data-stu-id="abcf7-116">The filter expression (from which the function is called) is evaluated if an exception occurs during execution of the **\_\_try** block, and it determines whether or not the **\_\_except** block is executed.</span></span>

<span data-ttu-id="abcf7-117">A expressão de filtro pode invocar uma função de filtro.</span><span class="sxs-lookup"><span data-stu-id="abcf7-117">The filter expression can invoke a filter function.</span></span> <span data-ttu-id="abcf7-118">A função Filter não pode chamar **GetExceptionInformation**.</span><span class="sxs-lookup"><span data-stu-id="abcf7-118">The filter function cannot call **GetExceptionInformation**.</span></span> <span data-ttu-id="abcf7-119">No entanto, o valor de retorno de **GetExceptionInformation** pode ser passado como um parâmetro para uma função de filtro.</span><span class="sxs-lookup"><span data-stu-id="abcf7-119">However, the return value of **GetExceptionInformation** can be passed as a parameter to a filter function.</span></span>

<span data-ttu-id="abcf7-120">Para passar as informações de [**\_ ponteiros de exceção**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) para o bloco de manipulador de exceção, a expressão de filtro ou a função de filtro deve copiar o ponteiro ou os dados para o armazenamento seguro que o manipulador pode acessar posteriormente.</span><span class="sxs-lookup"><span data-stu-id="abcf7-120">To pass the [**EXCEPTION\_POINTERS**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) information to the exception-handler block, the filter expression or filter function must copy the pointer or the data to safe storage that the handler can later access.</span></span>

<span data-ttu-id="abcf7-121">No caso de manipuladores aninhados, cada expressão de filtro é avaliada até que uma seja avaliada como **exceção \_ executar \_ manipulador** ou **exceção \_ continuar \_ execução**.</span><span class="sxs-lookup"><span data-stu-id="abcf7-121">In the case of nested handlers, each filter expression is evaluated until one is evaluated as **EXCEPTION\_EXECUTE\_HANDLER** or **EXCEPTION\_CONTINUE\_EXECUTION**.</span></span> <span data-ttu-id="abcf7-122">Cada expressão de filtro pode invocar **GetExceptionInformation** para obter informações de exceção.</span><span class="sxs-lookup"><span data-stu-id="abcf7-122">Each filter expression can invoke **GetExceptionInformation** to get exception information.</span></span>

## <a name="requirements"></a><span data-ttu-id="abcf7-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="abcf7-123">Requirements</span></span>



| <span data-ttu-id="abcf7-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="abcf7-124">Requirement</span></span> | <span data-ttu-id="abcf7-125">Valor</span><span class="sxs-lookup"><span data-stu-id="abcf7-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="abcf7-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="abcf7-126">Minimum supported client</span></span><br/> | <span data-ttu-id="abcf7-127">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="abcf7-127">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="abcf7-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="abcf7-128">Minimum supported server</span></span><br/> | <span data-ttu-id="abcf7-129">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="abcf7-129">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="abcf7-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="abcf7-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abcf7-131">**NOTICIOSO**</span><span class="sxs-lookup"><span data-stu-id="abcf7-131">**CONTEXT**</span></span>](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context)
</dt> <dt>

[<span data-ttu-id="abcf7-132">**\_ponteiros de exceção**</span><span class="sxs-lookup"><span data-stu-id="abcf7-132">**EXCEPTION\_POINTERS**</span></span>](/windows/desktop/api/WinNT/ns-winnt-exception_pointers)
</dt> <dt>

[<span data-ttu-id="abcf7-133">**registro de exceção \_**</span><span class="sxs-lookup"><span data-stu-id="abcf7-133">**EXCEPTION\_RECORD**</span></span>](/windows/desktop/api/WinNT/ns-winnt-exception_record)
</dt> <dt>

[<span data-ttu-id="abcf7-134">**GetExceptionCode**</span><span class="sxs-lookup"><span data-stu-id="abcf7-134">**GetExceptionCode**</span></span>](getexceptioncode.md)
</dt> <dt>

[<span data-ttu-id="abcf7-135">**GetXStateFeaturesMask**</span><span class="sxs-lookup"><span data-stu-id="abcf7-135">**GetXStateFeaturesMask**</span></span>](/windows/desktop/api/WinBase/nf-winbase-getxstatefeaturesmask)
</dt> <dt>

[<span data-ttu-id="abcf7-136">Funções de manipulação de exceção estruturada</span><span class="sxs-lookup"><span data-stu-id="abcf7-136">Structured Exception Handling Functions</span></span>](structured-exception-handling-functions.md)
</dt> <dt>

[<span data-ttu-id="abcf7-137">Visão geral da manipulação de exceção estruturada</span><span class="sxs-lookup"><span data-stu-id="abcf7-137">Structured Exception Handling Overview</span></span>](structured-exception-handling.md)
</dt> <dt>

[<span data-ttu-id="abcf7-138">Habilitar o suporte do Windows para Intel AVX</span><span class="sxs-lookup"><span data-stu-id="abcf7-138">Enable Windows Support for Intel AVX</span></span>](../win7appqual/enable-windows-7-support-for-intel-avx.md)
</dt> </dl>

 

 
