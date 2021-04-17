---
title: Tratamento de erro COM em Java e Visual Basic
description: Tratamento de erro COM em Java e Visual Basic
ms.assetid: 1130a038-3c18-4530-a6d7-9f538352297f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea12dc040218e14098ce2394fbb5cd2ebeff1704
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104366763"
---
# <a name="com-error-handling-in-java-and-visual-basic"></a><span data-ttu-id="5ba62-103">Tratamento de erro COM em Java e Visual Basic</span><span class="sxs-lookup"><span data-stu-id="5ba62-103">COM Error Handling in Java and Visual Basic</span></span>

<span data-ttu-id="5ba62-104">Há três interfaces e três funções que podem ser usadas em COM para fornecer tratamento de erros durante a programação em Java ou Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="5ba62-104">There are three interfaces and three functions that can be used in COM to provide error handling when programming in Java or Microsoft Visual Basic.</span></span> <span data-ttu-id="5ba62-105">Em Java e Visual Basic, a chamada de método não retorna um **HRESULT** como o valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="5ba62-105">In Java and Visual Basic, the method call does not return an **HRESULT** as the return value.</span></span> <span data-ttu-id="5ba62-106">Em vez disso, esses idiomas usam as interfaces e funções COM para obter valores **HRESULT** e para tratar erros ou exceções.</span><span class="sxs-lookup"><span data-stu-id="5ba62-106">Instead, these languages use the COM interfaces and functions to obtain **HRESULT** values and to handle errors or exceptions.</span></span> <span data-ttu-id="5ba62-107">(Exceções são eventos além do controle do programa, como problemas de arquivo ou parâmetros inválidos.)</span><span class="sxs-lookup"><span data-stu-id="5ba62-107">(Exceptions are events beyond the program's control, such as file problems or invalid parameters.)</span></span>

<span data-ttu-id="5ba62-108">As três interfaces que fornecem suporte para **HRESULT** s são listadas e descritas brevemente na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="5ba62-108">The three interfaces that provide support for **HRESULT** s are listed and described briefly in the following table.</span></span>



|                                                                          |                                                                                                                      |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5ba62-109">**ICreateErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="5ba62-109">**ICreateErrorInfo**</span></span>](/windows/win32/api/oaidl/nn-oaidl-icreateerrorinfo)<br/>  | <span data-ttu-id="5ba62-110">Define informações de erro.</span><span class="sxs-lookup"><span data-stu-id="5ba62-110">Sets error information.</span></span><br/>                                                                                   |
| [<span data-ttu-id="5ba62-111">**IErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="5ba62-111">**IErrorInfo**</span></span>](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo)<br/>        | <span data-ttu-id="5ba62-112">Retorna informações de um objeto de erro.</span><span class="sxs-lookup"><span data-stu-id="5ba62-112">Returns information from an error object.</span></span><br/>                                                                 |
| [<span data-ttu-id="5ba62-113">**ISupportErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="5ba62-113">**ISupportErrorInfo**</span></span>](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo)<br/> | <span data-ttu-id="5ba62-114">Identifica o objeto como suporte à interface [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) .</span><span class="sxs-lookup"><span data-stu-id="5ba62-114">Identifies the object as supporting the [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) interface.</span></span><br/> |



 

<span data-ttu-id="5ba62-115">As três funções que fornecem suporte para **HRESULT** s são listadas e descritas brevemente na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="5ba62-115">The three functions that provide support for **HRESULT** s are listed and described briefly in the following table.</span></span>



|                                                                        |                                                                                                                                                                      |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5ba62-116">**CreateErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="5ba62-116">**CreateErrorInfo**</span></span>](/windows/win32/api/oleauto/nf-oleauto-createerrorinfo)<br/> | <span data-ttu-id="5ba62-117">Cria uma instância de um objeto de erro genérico.</span><span class="sxs-lookup"><span data-stu-id="5ba62-117">Creates an instance of a generic error object.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="5ba62-118">**GetErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="5ba62-118">**GetErrorInfo**</span></span>](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo)<br/>    | <span data-ttu-id="5ba62-119">Obtém o ponteiro de informações de erro definido pela chamada anterior para [**SetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo) no thread lógico atual.</span><span class="sxs-lookup"><span data-stu-id="5ba62-119">Obtains the error information pointer set by the previous call to [**SetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo) in the current logical thread.</span></span><br/> |
| [<span data-ttu-id="5ba62-120">**SetErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="5ba62-120">**SetErrorInfo**</span></span>](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo)<br/>    | <span data-ttu-id="5ba62-121">Define o objeto de informações de erro para o thread atual de execução.</span><span class="sxs-lookup"><span data-stu-id="5ba62-121">Sets the error information object for the current thread of execution.</span></span><br/>                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="5ba62-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5ba62-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ba62-123">Tratamento de erro em COM</span><span class="sxs-lookup"><span data-stu-id="5ba62-123">Error Handling in COM</span></span>](error-handling-in-com.md)
</dt> </dl>

 

