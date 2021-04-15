---
title: Tratamento de erro no COM (COM)
description: Tratamento de erro em COM
ms.assetid: 15f3ae3e-1794-4948-a7aa-6309a703364b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19af496eabf50833c99d462ff074254bc39bb7a0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104454577"
---
# <a name="error-handling-in-com-com"></a><span data-ttu-id="ff356-103">Tratamento de erro no COM (COM)</span><span class="sxs-lookup"><span data-stu-id="ff356-103">Error Handling in COM (COM)</span></span>

<span data-ttu-id="ff356-104">Quase todas as funções COM e métodos de interface retornam um valor do tipo **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="ff356-104">Almost all COM functions and interface methods return a value of the type **HRESULT**.</span></span> <span data-ttu-id="ff356-105">O **HRESULT** (para o *identificador de resultado*) é uma maneira de retornar valores de êxito, de aviso e de erro.</span><span class="sxs-lookup"><span data-stu-id="ff356-105">The **HRESULT** (for *result handle*) is a way of returning success, warning, and error values.</span></span> <span data-ttu-id="ff356-106">**HRESULT** s não são realmente identificadores para nada; Eles são apenas valores com vários campos codificados no valor.</span><span class="sxs-lookup"><span data-stu-id="ff356-106">**HRESULT** s are really not handles to anything; they are only values with several fields encoded in the value.</span></span> <span data-ttu-id="ff356-107">De acordo COM a especificação COM, um resultado de zero indica êxito e um resultado diferente de zero indica falha.</span><span class="sxs-lookup"><span data-stu-id="ff356-107">As per the COM specification, a result of zero indicates success and a nonzero result indicates failure.</span></span>

<span data-ttu-id="ff356-108">No nível do código-fonte, todos os valores de erro consistem em três partes, separadas por sublinhados.</span><span class="sxs-lookup"><span data-stu-id="ff356-108">At the source code level, all error values consist of three parts, separated by underscores.</span></span> <span data-ttu-id="ff356-109">A primeira parte é o prefixo que identifica o recurso associado ao erro, a segunda parte é E para erro e a terceira parte é uma cadeia de caracteres que descreve a condição real.</span><span class="sxs-lookup"><span data-stu-id="ff356-109">The first part is the prefix that identifies the facility associated with the error, the second part is E for error, and the third part is a string that describes the actual condition.</span></span> <span data-ttu-id="ff356-110">Por exemplo, **STG \_ E \_ MEDIUMFULL** é retornado quando não há nenhum espaço restante em um disco rígido.</span><span class="sxs-lookup"><span data-stu-id="ff356-110">For example, **STG\_E\_MEDIUMFULL** is returned when there is no space left on a hard disk.</span></span> <span data-ttu-id="ff356-111">O prefixo **STG** indica o recurso de armazenamento, o **E** indica que o código de status representa um erro e o **MEDIUMFULL** fornece informações específicas sobre o erro.</span><span class="sxs-lookup"><span data-stu-id="ff356-111">The **STG** prefix indicates the storage facility, the **E** indicates that the status code represents an error, and the **MEDIUMFULL** provides specific information about the error.</span></span> <span data-ttu-id="ff356-112">Muitos dos valores que você pode querer retornar de um método ou função de interface são definidos em Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="ff356-112">Many of the values that you might want to return from an interface method or function are defined in Winerror.h.</span></span>

<span data-ttu-id="ff356-113">Para obter mais informações sobre o tratamento de erros, consulte as seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="ff356-113">For more information about error handling, see the following sections:</span></span>

-   [<span data-ttu-id="ff356-114">Estrutura de códigos de erro COM</span><span class="sxs-lookup"><span data-stu-id="ff356-114">Structure of COM Error Codes</span></span>](structure-of-com-error-codes.md)
-   [<span data-ttu-id="ff356-115">Códigos no FACILITy \_ ITF</span><span class="sxs-lookup"><span data-stu-id="ff356-115">Codes in FACILITY\_ITF</span></span>](codes-in-facility-itf.md)
-   [<span data-ttu-id="ff356-116">Usando macros para tratamento de erro</span><span class="sxs-lookup"><span data-stu-id="ff356-116">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)
-   [<span data-ttu-id="ff356-117">Tratamento de erro COM em Java e Visual Basic</span><span class="sxs-lookup"><span data-stu-id="ff356-117">COM Error Handling in Java and Visual Basic</span></span>](com-error-handling-in-java-and-visual-basic.md)
-   [<span data-ttu-id="ff356-118">Estratégias de tratamento de erros</span><span class="sxs-lookup"><span data-stu-id="ff356-118">Error Handling Strategies</span></span>](error-handling-strategies.md)
-   [<span data-ttu-id="ff356-119">Manipulando erros desconhecidos</span><span class="sxs-lookup"><span data-stu-id="ff356-119">Handling Unknown Errors</span></span>](handling-unknown-errors.md)

## <a name="related-topics"></a><span data-ttu-id="ff356-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ff356-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff356-121">Códigos de erro COM</span><span class="sxs-lookup"><span data-stu-id="ff356-121">COM Error Codes</span></span>](com-error-codes.md)
</dt> </dl>

 

 




