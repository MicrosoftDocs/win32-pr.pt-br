---
description: Macros Assert e Breakpoint
ms.assetid: c34db182-1f65-4a2f-9534-268638c2502d
title: Macros Assert e Breakpoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4771fb7e302ec9e1093fca82d7842212e0b68e2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087882"
---
# <a name="assert-and-breakpoint-macros"></a><span data-ttu-id="d3b0e-103">Macros Assert e Breakpoint</span><span class="sxs-lookup"><span data-stu-id="d3b0e-103">Assert and Breakpoint Macros</span></span>

<span data-ttu-id="d3b0e-104">As [classes base do DirectShow](directshow-base-classes.md) fornecem várias macros que executam asserções ou causam pontos de interrupção.</span><span class="sxs-lookup"><span data-stu-id="d3b0e-104">The [DirectShow Base Classes](directshow-base-classes.md) provide several macros that perform asserts or cause breakpoints.</span></span>



| <span data-ttu-id="d3b0e-105">Macro</span><span class="sxs-lookup"><span data-stu-id="d3b0e-105">Macro</span></span>                                        | <span data-ttu-id="d3b0e-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="d3b0e-106">Description</span></span>                                                                                                                        |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d3b0e-107">**DECLARAR**</span><span class="sxs-lookup"><span data-stu-id="d3b0e-107">**ASSERT**</span></span>](assert.md)                     | <span data-ttu-id="d3b0e-108">Avalia uma expressão e exibe uma mensagem de diagnóstico se a expressão for **falsa**.</span><span class="sxs-lookup"><span data-stu-id="d3b0e-108">Evaluates an expression, and displays a diagnostic message if the expression is **FALSE**.</span></span>                                         |
| [<span data-ttu-id="d3b0e-109">**DbgAssertAligned**</span><span class="sxs-lookup"><span data-stu-id="d3b0e-109">**DbgAssertAligned**</span></span>](dbgassertaligned.md) | <span data-ttu-id="d3b0e-110">Testa se um ponteiro está alinhado a um limite especificado.</span><span class="sxs-lookup"><span data-stu-id="d3b0e-110">Tests whether a pointer is aligned to a specified boundary.</span></span>                                                                        |
| [<span data-ttu-id="d3b0e-111">**DbgBreak**</span><span class="sxs-lookup"><span data-stu-id="d3b0e-111">**DbgBreak**</span></span>](dbgbreak.md)                 | <span data-ttu-id="d3b0e-112">Exibe uma caixa de mensagem com a cadeia de caracteres especificada, o nome do arquivo de origem e o número da linha.</span><span class="sxs-lookup"><span data-stu-id="d3b0e-112">Displays a message box with the specified string, the name of the source file, and the line number.</span></span>                                |
| [<span data-ttu-id="d3b0e-113">**EXECUTAR \_ declaração**</span><span class="sxs-lookup"><span data-stu-id="d3b0e-113">**EXECUTE\_ASSERT**</span></span>](execute-assert.md)    | <span data-ttu-id="d3b0e-114">Avalia uma expressão em compilações de depuração e de varejo.</span><span class="sxs-lookup"><span data-stu-id="d3b0e-114">Evaluates an expression in debug and retail builds.</span></span> <span data-ttu-id="d3b0e-115">Em builds de depuração, exibe uma mensagem de diagnóstico se a expressão for **false**.</span><span class="sxs-lookup"><span data-stu-id="d3b0e-115">In debug builds, displays a diagnostic message if the expression is **FALSE**.</span></span> |
| [<span data-ttu-id="d3b0e-116">**KASSERT**</span><span class="sxs-lookup"><span data-stu-id="d3b0e-116">**KASSERT**</span></span>](kassert.md)                   | <span data-ttu-id="d3b0e-117">Avalia uma expressão e causa uma exceção de ponto de interrupção se a expressão for **falsa**.</span><span class="sxs-lookup"><span data-stu-id="d3b0e-117">Evaluates an expression, and causes a breakpoint exception if the expression is **FALSE**.</span></span>                                         |
| [<span data-ttu-id="d3b0e-118">**KDbgBreak**</span><span class="sxs-lookup"><span data-stu-id="d3b0e-118">**KDbgBreak**</span></span>](kdbgbreak.md)               | <span data-ttu-id="d3b0e-119">Causa uma exceção de ponto de interrupção e registra a cadeia de caracteres especificada.</span><span class="sxs-lookup"><span data-stu-id="d3b0e-119">Causes a breakpoint exception, and logs the specified string.</span></span>                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="d3b0e-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d3b0e-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3b0e-121">Utilitários de depuração</span><span class="sxs-lookup"><span data-stu-id="d3b0e-121">Debugging Utilities</span></span>](debugging-utilities.md)
</dt> </dl>

 

 



