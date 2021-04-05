---
description: Os manipuladores de exceção em vetor são uma extensão da manipulação de exceção estruturada.
ms.assetid: e4cf8a88-1bdf-4666-8653-fe2e86c4d8ef
title: Manipulação de exceção em vetor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 011310b46ce8912e03b6481e9b12b986174a3ef0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826393"
---
# <a name="vectored-exception-handling"></a><span data-ttu-id="1a149-103">Manipulação de exceção em vetor</span><span class="sxs-lookup"><span data-stu-id="1a149-103">Vectored Exception Handling</span></span>

<span data-ttu-id="1a149-104">Os manipuladores de exceção em vetor são uma extensão da manipulação de exceção estruturada.</span><span class="sxs-lookup"><span data-stu-id="1a149-104">Vectored exception handlers are an extension to structured exception handling.</span></span> <span data-ttu-id="1a149-105">Um aplicativo pode registrar uma função para inspecionar ou manipular todas as exceções para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1a149-105">An application can register a function to watch or handle all exceptions for the application.</span></span> <span data-ttu-id="1a149-106">Os manipuladores vetoriais não são baseados em quadros, portanto, você pode adicionar um manipulador que será chamado independentemente de onde você estiver em um quadro de chamada.</span><span class="sxs-lookup"><span data-stu-id="1a149-106">Vectored handlers are not frame-based, therefore, you can add a handler that will be called regardless of where you are in a call frame.</span></span> <span data-ttu-id="1a149-107">Os manipuladores vetoriais são chamados na ordem em que foram adicionados, depois que o depurador obtém uma notificação de primeira chance, mas antes de o sistema começar a desenrolar a pilha.</span><span class="sxs-lookup"><span data-stu-id="1a149-107">Vectored handlers are called in the order that they were added, after the debugger gets a first chance notification, but before the system begins unwinding the stack.</span></span>

<span data-ttu-id="1a149-108">Para adicionar um manipulador de continuação em vetor, use a função [**AddVectoredContinueHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredcontinuehandler) .</span><span class="sxs-lookup"><span data-stu-id="1a149-108">To add a vectored continue handler, use the [**AddVectoredContinueHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredcontinuehandler) function.</span></span> <span data-ttu-id="1a149-109">Para remover esse manipulador, use a função [**RemoveVectoredContinueHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredcontinuehandler) .</span><span class="sxs-lookup"><span data-stu-id="1a149-109">To remove this handler, use the [**RemoveVectoredContinueHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredcontinuehandler) function.</span></span>

<span data-ttu-id="1a149-110">Para adicionar um manipulador de exceção em vetor, use a função [**AddVectoredExceptionHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredexceptionhandler) .</span><span class="sxs-lookup"><span data-stu-id="1a149-110">To add a vectored exception handler, use the [**AddVectoredExceptionHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredexceptionhandler) function.</span></span> <span data-ttu-id="1a149-111">Para remover esse manipulador, use a função [**RemoveVectoredExceptionHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredexceptionhandler) .</span><span class="sxs-lookup"><span data-stu-id="1a149-111">To remove this handler, use the [**RemoveVectoredExceptionHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredexceptionhandler) function.</span></span>

 

 
