---
description: Causa uma exceção de ponto de interrupção e registra a cadeia de caracteres especificada usando a macro DbgLog. Ignorado em compilações de varejo.
ms.assetid: 475810db-692b-4727-9ef1-ece74e9618d0
title: Macro KDbgBreak (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KDbgBreak
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 9631dc8d956652137810b25ae5923cc1c6927bee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757877"
---
# <a name="kdbgbreak-macro"></a><span data-ttu-id="8caa2-104">Macro KDbgBreak</span><span class="sxs-lookup"><span data-stu-id="8caa2-104">KDbgBreak macro</span></span>

<span data-ttu-id="8caa2-105">Causa uma exceção de ponto de interrupção e registra a cadeia de caracteres especificada usando a macro [**DbgLog**](dbglog.md) .</span><span class="sxs-lookup"><span data-stu-id="8caa2-105">Causes a breakpoint exception, and logs the specified string using the [**DbgLog**](dbglog.md) macro.</span></span> <span data-ttu-id="8caa2-106">Ignorado em compilações de varejo.</span><span class="sxs-lookup"><span data-stu-id="8caa2-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="8caa2-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8caa2-107">Syntax</span></span>


```C++
void KDbgBreak(
    strLiteral
);
```



## <a name="parameters"></a><span data-ttu-id="8caa2-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8caa2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8caa2-109">*strLiteral*</span><span class="sxs-lookup"><span data-stu-id="8caa2-109">*strLiteral*</span></span> 
</dt> <dd>

<span data-ttu-id="8caa2-110">Cadeia de texto.</span><span class="sxs-lookup"><span data-stu-id="8caa2-110">Text string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8caa2-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8caa2-111">Return value</span></span>

<span data-ttu-id="8caa2-112">Essa macro não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="8caa2-112">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8caa2-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="8caa2-113">Remarks</span></span>

<span data-ttu-id="8caa2-114">Ao contrário da macro [**DbgBreak**](dbgbreak.md) , essa macro não exibe uma caixa de mensagem solicitando o usuário.</span><span class="sxs-lookup"><span data-stu-id="8caa2-114">Unlike the [**DbgBreak**](dbgbreak.md) macro, this macro does not display a message box prompting the user.</span></span> <span data-ttu-id="8caa2-115">Em compilações de depuração, ele automaticamente faz com que ocorra uma exceção de ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="8caa2-115">In debug builds, it automatically causes a breakpoint exception to occur.</span></span>

## <a name="requirements"></a><span data-ttu-id="8caa2-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8caa2-116">Requirements</span></span>



| <span data-ttu-id="8caa2-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8caa2-117">Requirement</span></span> | <span data-ttu-id="8caa2-118">Valor</span><span class="sxs-lookup"><span data-stu-id="8caa2-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8caa2-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8caa2-119">Header</span></span><br/> | <dl> <span data-ttu-id="8caa2-120"><dt>Wxdebug. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8caa2-120"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8caa2-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="8caa2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8caa2-122">Macros Assert e Breakpoint</span><span class="sxs-lookup"><span data-stu-id="8caa2-122">Assert and Breakpoint Macros</span></span>](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




