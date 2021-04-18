---
description: Valor booliano que especifica se o bloqueio deve ser rastreado.
ms.assetid: 23417410-cfdc-426e-a662-7d6580b43a28
title: 'Membro CCritSec:: m_fTrace (Wxutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_fTrace
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 691e078bb3b502704aed585ba020d49b2bd99af1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751898"
---
# <a name="ccritsecm_ftrace-member"></a><span data-ttu-id="aba8a-103">Membro de CCritSec:: m \_ fTrace</span><span class="sxs-lookup"><span data-stu-id="aba8a-103">CCritSec::m\_fTrace member</span></span>

<span data-ttu-id="aba8a-104">Valor booliano que especifica se o bloqueio deve ser rastreado.</span><span class="sxs-lookup"><span data-stu-id="aba8a-104">Boolean value that specifies whether to trace this lock.</span></span>

## <a name="syntax"></a><span data-ttu-id="aba8a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aba8a-105">Syntax</span></span>


```C++
BOOL m_fTrace;
```



## <a name="remarks"></a><span data-ttu-id="aba8a-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="aba8a-106">Remarks</span></span>

<span data-ttu-id="aba8a-107">Essa variável de membro é definida somente na versão de depuração da classe base.</span><span class="sxs-lookup"><span data-stu-id="aba8a-107">This member variable is defined only in the debug version of the base class.</span></span> <span data-ttu-id="aba8a-108">Se o valor for **true**, um rastreamento do estado de bloqueio será gravado no log de depuração.</span><span class="sxs-lookup"><span data-stu-id="aba8a-108">If the value is **TRUE**, a trace of the lock state is written to the debug log.</span></span> <span data-ttu-id="aba8a-109">(O log de depuração para seções críticas deve estar ativo.) Para obter mais informações, consulte [**DbgLockTrace**](dbglocktrace.md).</span><span class="sxs-lookup"><span data-stu-id="aba8a-109">(Debug logging for critical sections must be active.) For more information, see [**DbgLockTrace**](dbglocktrace.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="aba8a-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aba8a-110">Requirements</span></span>



| <span data-ttu-id="aba8a-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="aba8a-111">Requirement</span></span> | <span data-ttu-id="aba8a-112">Valor</span><span class="sxs-lookup"><span data-stu-id="aba8a-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aba8a-113">parâmetro</span><span class="sxs-lookup"><span data-stu-id="aba8a-113">Header</span></span><br/>  | <dl> <span data-ttu-id="aba8a-114"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="aba8a-114"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="aba8a-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="aba8a-115">Library</span></span><br/> | <dl> <span data-ttu-id="aba8a-116"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="aba8a-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aba8a-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="aba8a-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aba8a-118">**Classe CCritSec**</span><span class="sxs-lookup"><span data-stu-id="aba8a-118">**CCritSec Class**</span></span>](ccritsec.md)
</dt> </dl>

 

 




