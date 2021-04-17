---
description: Ao criar um processo com a função CreateProcess, você pode especificar que o processo herde identificadores para mutex, evento, semáforo ou objetos de temporizador usando a \_ estrutura atributos de segurança.
ms.assetid: 36491a5c-7599-4f69-ab76-d3a62261a151
title: Herança de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6087ae3699e7628ab97871ede41cc2e406e40157
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755537"
---
# <a name="object-inheritance"></a><span data-ttu-id="5267e-103">Herança de objetos</span><span class="sxs-lookup"><span data-stu-id="5267e-103">Object Inheritance</span></span>

<span data-ttu-id="5267e-104">Ao criar um processo com a função [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) , você pode especificar que o processo herde identificadores para mutex, evento, semáforo ou objetos de temporizador usando a estrutura [**\_ atributos de segurança**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="5267e-104">When you create a process with the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) function, you can specify that the process inherit handles to mutex, event, semaphore, or timer objects using the [**SECURITY\_ATTRIBUTES**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) structure.</span></span> <span data-ttu-id="5267e-105">O identificador herdado pelo processo tem o mesmo acesso ao objeto que o identificador original.</span><span class="sxs-lookup"><span data-stu-id="5267e-105">The handle inherited by the process has the same access to the object as the original handle.</span></span> <span data-ttu-id="5267e-106">O identificador herdado aparece na tabela de identificadores do processo criado, mas você deve comunicar o valor do identificador para o processo criado.</span><span class="sxs-lookup"><span data-stu-id="5267e-106">The inherited handle appears in the handle table of the created process, but you must communicate the handle value to the created process.</span></span> <span data-ttu-id="5267e-107">Você pode fazer isso especificando o valor como um argumento de linha de comando ao chamar **CreateProcess**.</span><span class="sxs-lookup"><span data-stu-id="5267e-107">You can do this by specifying the value as a command-line argument when you call **CreateProcess**.</span></span> <span data-ttu-id="5267e-108">Em seguida, o processo criado usa a função [**GetCommandLine**](/windows/win32/api/processenv/nf-processenv-getcommandlinea) para recuperar a cadeia de caracteres de linha de comando e converter o argumento Handle em um identificador utilizável.</span><span class="sxs-lookup"><span data-stu-id="5267e-108">The created process then uses the [**GetCommandLine**](/windows/win32/api/processenv/nf-processenv-getcommandlinea) function to retrieve the command-line string and convert the handle argument into a usable handle.</span></span> <span data-ttu-id="5267e-109">Para obter mais informações, consulte [Herança](../procthread/inheritance.md).</span><span class="sxs-lookup"><span data-stu-id="5267e-109">For more information, see [Inheritance](../procthread/inheritance.md).</span></span>

 

 
