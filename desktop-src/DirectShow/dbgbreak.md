---
description: Exibe uma caixa de mensagem com a cadeia de caracteres especificada, o nome do arquivo de origem e o número da linha. O usuário pode ignorar a mensagem, inserir o depurador ou sair do aplicativo. Ignorado em compilações de varejo.
ms.assetid: ac4da7da-f9d0-44ae-9ad1-9a5908b288fb
title: Macro DbgBreak (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgBreak
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 099344a295de2657b40218b993ab9c4cb6411353
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751880"
---
# <a name="dbgbreak-macro"></a><span data-ttu-id="57722-105">Macro DbgBreak</span><span class="sxs-lookup"><span data-stu-id="57722-105">DbgBreak macro</span></span>

<span data-ttu-id="57722-106">Exibe uma caixa de mensagem com a cadeia de caracteres especificada, o nome do arquivo de origem e o número da linha.</span><span class="sxs-lookup"><span data-stu-id="57722-106">Displays a message box with the specified string, the name of the source file, and the line number.</span></span> <span data-ttu-id="57722-107">O usuário pode ignorar a mensagem, inserir o depurador ou sair do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="57722-107">The user can ignore the message, enter the debugger, or quit the application.</span></span> <span data-ttu-id="57722-108">Ignorado em compilações de varejo.</span><span class="sxs-lookup"><span data-stu-id="57722-108">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="57722-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="57722-109">Syntax</span></span>


```C++
void DbgBreak(
    strLiteral
);
```



## <a name="parameters"></a><span data-ttu-id="57722-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="57722-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57722-111">*strLiteral*</span><span class="sxs-lookup"><span data-stu-id="57722-111">*strLiteral*</span></span> 
</dt> <dd>

<span data-ttu-id="57722-112">Cadeia de texto.</span><span class="sxs-lookup"><span data-stu-id="57722-112">Text string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57722-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="57722-113">Return value</span></span>

<span data-ttu-id="57722-114">Essa macro não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="57722-114">This macro does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="57722-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="57722-115">Examples</span></span>


```C++
DbgBreak("Unrecoverable error occurred.");
```



## <a name="requirements"></a><span data-ttu-id="57722-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57722-116">Requirements</span></span>



| <span data-ttu-id="57722-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="57722-117">Requirement</span></span> | <span data-ttu-id="57722-118">Valor</span><span class="sxs-lookup"><span data-stu-id="57722-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57722-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="57722-119">Header</span></span><br/> | <dl> <span data-ttu-id="57722-120"><dt>Wxdebug. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="57722-120"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57722-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="57722-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57722-122">Macros Assert e Breakpoint</span><span class="sxs-lookup"><span data-stu-id="57722-122">Assert and Breakpoint Macros</span></span>](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




