---
title: Tratamento de erro COM em Java e Visual Basic
description: Tratamento de erro COM em Java e Visual Basic
ms.assetid: 1130a038-3c18-4530-a6d7-9f538352297f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11c55c1c2414c69ff9398845858baadebd58cbf9
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424006"
---
# <a name="com-error-handling-in-java-and-visual-basic"></a><span data-ttu-id="42f18-103">Tratamento de erro COM em Java e Visual Basic</span><span class="sxs-lookup"><span data-stu-id="42f18-103">COM Error Handling in Java and Visual Basic</span></span>

<span data-ttu-id="42f18-104">Há três interfaces e três funções que podem ser usadas em COM para fornecer tratamento de erros durante a programação em Java ou Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="42f18-104">There are three interfaces and three functions that can be used in COM to provide error handling when programming in Java or Microsoft Visual Basic.</span></span> <span data-ttu-id="42f18-105">Em Java e Visual Basic, a chamada de método não retorna um **HRESULT** como o valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="42f18-105">In Java and Visual Basic, the method call does not return an **HRESULT** as the return value.</span></span> <span data-ttu-id="42f18-106">Em vez disso, esses idiomas usam as interfaces e funções COM para obter valores **HRESULT** e para tratar erros ou exceções.</span><span class="sxs-lookup"><span data-stu-id="42f18-106">Instead, these languages use the COM interfaces and functions to obtain **HRESULT** values and to handle errors or exceptions.</span></span> <span data-ttu-id="42f18-107">(Exceções são eventos além do controle do programa, como problemas de arquivo ou parâmetros inválidos.)</span><span class="sxs-lookup"><span data-stu-id="42f18-107">(Exceptions are events beyond the program's control, such as file problems or invalid parameters.)</span></span>

<span data-ttu-id="42f18-108">As três interfaces que fornecem suporte para **HRESULT** s são listadas e descritas brevemente na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="42f18-108">The three interfaces that provide support for **HRESULT** s are listed and described briefly in the following table.</span></span>



|  <span data-ttu-id="42f18-109">Interface</span><span class="sxs-lookup"><span data-stu-id="42f18-109">Interface</span></span>                                                                        |  <span data-ttu-id="42f18-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="42f18-110">Description</span></span>                                                                                                                    |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="42f18-111">**ICreateErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="42f18-111">**ICreateErrorInfo**</span></span>](/windows/win32/api/oaidl/nn-oaidl-icreateerrorinfo)<br/>  | <span data-ttu-id="42f18-112">Define informações de erro.</span><span class="sxs-lookup"><span data-stu-id="42f18-112">Sets error information.</span></span><br/>                                                                                   |
| [<span data-ttu-id="42f18-113">**IErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="42f18-113">**IErrorInfo**</span></span>](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo)<br/>        | <span data-ttu-id="42f18-114">Retorna informações de um objeto de erro.</span><span class="sxs-lookup"><span data-stu-id="42f18-114">Returns information from an error object.</span></span><br/>                                                                 |
| [<span data-ttu-id="42f18-115">**ISupportErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="42f18-115">**ISupportErrorInfo**</span></span>](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo)<br/> | <span data-ttu-id="42f18-116">Identifica o objeto como suporte à interface [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) .</span><span class="sxs-lookup"><span data-stu-id="42f18-116">Identifies the object as supporting the [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) interface.</span></span><br/> |



 

<span data-ttu-id="42f18-117">As três funções que fornecem suporte para **HRESULT** s são listadas e descritas brevemente na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="42f18-117">The three functions that provide support for **HRESULT** s are listed and described briefly in the following table.</span></span>



|    <span data-ttu-id="42f18-118">Interface</span><span class="sxs-lookup"><span data-stu-id="42f18-118">Interface</span></span>       |       <span data-ttu-id="42f18-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="42f18-119">Description</span></span>       |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="42f18-120">**CreateErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="42f18-120">**CreateErrorInfo**</span></span>](/windows/win32/api/oleauto/nf-oleauto-createerrorinfo)<br/> | <span data-ttu-id="42f18-121">Cria uma instância de um objeto de erro genérico.</span><span class="sxs-lookup"><span data-stu-id="42f18-121">Creates an instance of a generic error object.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="42f18-122">**GetErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="42f18-122">**GetErrorInfo**</span></span>](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo)<br/>    | <span data-ttu-id="42f18-123">Obtém o ponteiro de informações de erro definido pela chamada anterior para [**SetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo) no thread lógico atual.</span><span class="sxs-lookup"><span data-stu-id="42f18-123">Obtains the error information pointer set by the previous call to [**SetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo) in the current logical thread.</span></span><br/> |
| [<span data-ttu-id="42f18-124">**SetErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="42f18-124">**SetErrorInfo**</span></span>](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo)<br/>    | <span data-ttu-id="42f18-125">Define o objeto de informações de erro para o thread atual de execução.</span><span class="sxs-lookup"><span data-stu-id="42f18-125">Sets the error information object for the current thread of execution.</span></span><br/>                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="42f18-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="42f18-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42f18-127">Tratamento de erro em COM</span><span class="sxs-lookup"><span data-stu-id="42f18-127">Error Handling in COM</span></span>](error-handling-in-com.md)
</dt> </dl>

 

