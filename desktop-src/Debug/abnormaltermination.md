---
description: Indica se o \_ \_ bloco try de um manipulador de encerramento foi encerrado normalmente. A função pode ser chamada somente de dentro do \_ \_ bloco finally de um manipulador de encerramento.
ms.assetid: 0ddaef1f-03f0-45fc-9c5e-8d6a26a73245
title: Macro AbnormalTermination
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AbnormalTermination
api_type:
- NA
api_location: ''
ms.openlocfilehash: 7c4869f36d8ba70c8dcd8ca526949d489f455e8c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920515"
---
# <a name="abnormaltermination-macro"></a><span data-ttu-id="e4e32-104">Macro AbnormalTermination</span><span class="sxs-lookup"><span data-stu-id="e4e32-104">AbnormalTermination macro</span></span>

<span data-ttu-id="e4e32-105">Indica se o bloco **\_ \_ try** de um manipulador de encerramento foi encerrado normalmente.</span><span class="sxs-lookup"><span data-stu-id="e4e32-105">Indicates whether the **\_\_try** block of a termination handler terminated normally.</span></span> <span data-ttu-id="e4e32-106">A função pode ser chamada somente de dentro do bloco **\_ \_ finally** de um manipulador de encerramento.</span><span class="sxs-lookup"><span data-stu-id="e4e32-106">The function can be called only from within the **\_\_finally** block of a termination handler.</span></span>

> [!Note]  
> <span data-ttu-id="e4e32-107">O compilador de otimização do Microsoft C/C++ interpreta essa função como uma palavra-chave e seu uso fora da sintaxe apropriada de tratamento de exceção gera um erro de compilador.</span><span class="sxs-lookup"><span data-stu-id="e4e32-107">The Microsoft C/C++ Optimizing Compiler interprets this function as a keyword, and its use outside the appropriate exception-handling syntax generates a compiler error.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="e4e32-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e4e32-108">Syntax</span></span>


```C++
BOOL AbnormalTermination(void);
```



## <a name="parameters"></a><span data-ttu-id="e4e32-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4e32-109">Parameters</span></span>

<span data-ttu-id="e4e32-110">Esta macro não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="e4e32-110">This macro has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e4e32-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e4e32-111">Return value</span></span>

<span data-ttu-id="e4e32-112">Se o bloco **\_ \_ try** for encerrado de forma anormal, o valor de retorno será diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="e4e32-112">If the **\_\_try** block terminated abnormally, the return value is nonzero.</span></span>

<span data-ttu-id="e4e32-113">Se o bloco **\_ \_ try** for encerrado normalmente, o valor de retorno será zero.</span><span class="sxs-lookup"><span data-stu-id="e4e32-113">If the **\_\_try** block terminated normally, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4e32-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e4e32-114">Remarks</span></span>

<span data-ttu-id="e4e32-115">O bloco **\_ \_ try** será encerrado normalmente somente se a execução deixar o bloco sequencialmente após a execução da última instrução no bloco.</span><span class="sxs-lookup"><span data-stu-id="e4e32-115">The **\_\_try** block terminates normally only if execution leaves the block sequentially after executing the last statement in the block.</span></span> <span data-ttu-id="e4e32-116">Instruções (como **Return**, **goto**, **continue** ou **Break**) que causam a execução para deixar o bloco **\_ \_ try** resultam em finalização anormal do bloco.</span><span class="sxs-lookup"><span data-stu-id="e4e32-116">Statements (such as **return**, **goto**, **continue**, or **break**) that cause execution to leave the **\_\_try** block result in abnormal termination of the block.</span></span> <span data-ttu-id="e4e32-117">Esse é o caso, mesmo se essa instrução for a última instrução no bloco **\_ \_ try** .</span><span class="sxs-lookup"><span data-stu-id="e4e32-117">This is the case even if such a statement is the last statement in the **\_\_try** block.</span></span>

<span data-ttu-id="e4e32-118">A finalização anormal de um bloco **\_ \_ try** faz com que o sistema pesquise retroativamente por todos os quadros de pilha para determinar se os manipuladores de encerramento devem ser chamados.</span><span class="sxs-lookup"><span data-stu-id="e4e32-118">Abnormal termination of a **\_\_try** block causes the system to search backward through all stack frames to determine whether any termination handlers must be called.</span></span> <span data-ttu-id="e4e32-119">Isso pode resultar na execução de centenas de instruções, portanto, é importante evitar a finalização anormal de um bloco **\_ \_ try** devido a uma instrução **Return**, **goto**, **continue** ou **Break** .</span><span class="sxs-lookup"><span data-stu-id="e4e32-119">This can result in the execution of hundreds of instructions, so it is important to avoid abnormal termination of a **\_\_try** block due to a **return**, **goto**, **continue**, or **break** statement.</span></span> <span data-ttu-id="e4e32-120">Observe que essas instruções não geram uma exceção, embora o encerramento seja anormal.</span><span class="sxs-lookup"><span data-stu-id="e4e32-120">Note that these statements do not generate an exception, even though the termination is abnormal.</span></span>

<span data-ttu-id="e4e32-121">Para evitar a finalização anormal, a execução deve continuar no final do bloco.</span><span class="sxs-lookup"><span data-stu-id="e4e32-121">To avoid abnormal termination, execution should continue to the end of the block.</span></span> <span data-ttu-id="e4e32-122">Você também pode executar a instrução **\_ \_ Leave** .</span><span class="sxs-lookup"><span data-stu-id="e4e32-122">You can also execute the **\_\_leave** statement.</span></span> <span data-ttu-id="e4e32-123">A instrução **\_ \_ Leave** permite o encerramento imediato do bloco **\_ \_ try** sem causar um encerramento anormal e sua penalidade de desempenho.</span><span class="sxs-lookup"><span data-stu-id="e4e32-123">The **\_\_leave** statement allows for immediate termination of the **\_\_try** block without causing abnormal termination and its performance penalty.</span></span> <span data-ttu-id="e4e32-124">Verifique a documentação do compilador para determinar se a instrução **\_ \_ Leave** tem suporte.</span><span class="sxs-lookup"><span data-stu-id="e4e32-124">Check your compiler documentation to determine if the **\_\_leave** statement is supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4e32-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4e32-125">Requirements</span></span>



| <span data-ttu-id="e4e32-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4e32-126">Requirement</span></span> | <span data-ttu-id="e4e32-127">Valor</span><span class="sxs-lookup"><span data-stu-id="e4e32-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e4e32-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e4e32-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e4e32-129">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e4e32-129">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="e4e32-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e4e32-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e4e32-131">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e4e32-131">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e4e32-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="e4e32-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4e32-133">Funções de manipulação de exceção estruturada</span><span class="sxs-lookup"><span data-stu-id="e4e32-133">Structured Exception Handling Functions</span></span>](structured-exception-handling-functions.md)
</dt> <dt>

[<span data-ttu-id="e4e32-134">Visão geral da manipulação de exceção estruturada</span><span class="sxs-lookup"><span data-stu-id="e4e32-134">Structured Exception Handling Overview</span></span>](structured-exception-handling.md)
</dt> </dl>

 

 




