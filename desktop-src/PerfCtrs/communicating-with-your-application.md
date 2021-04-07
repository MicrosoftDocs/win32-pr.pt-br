---
description: Normalmente, um provedor fornece dados em nome de um aplicativo.
ms.assetid: 65ea6099-79df-4baa-9752-7df032ccc9a0
title: Comunicando-se com seu aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6def58d3e03676f3b1b46ba3ebd756eb3adc6196
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828395"
---
# <a name="communicating-with-your-application"></a><span data-ttu-id="afaca-103">Comunicando-se com seu aplicativo</span><span class="sxs-lookup"><span data-stu-id="afaca-103">Communicating With Your Application</span></span>

<span data-ttu-id="afaca-104">Normalmente, um provedor fornece dados em nome de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="afaca-104">Typically, a provider provides data on behalf of an application.</span></span> <span data-ttu-id="afaca-105">Por exemplo, um servidor pode criar uma DLL de desempenho para fornecer seus dados de contador.</span><span class="sxs-lookup"><span data-stu-id="afaca-105">For example, a server might create a performance DLL to provide its counter data.</span></span> <span data-ttu-id="afaca-106">A comunicação entre um aplicativo e seu provedor é diferente para o modo de usuário e aplicativos de modo kernel.</span><span class="sxs-lookup"><span data-stu-id="afaca-106">Communication between an application and its provider differs for user-mode and kernel-mode applications.</span></span> <span data-ttu-id="afaca-107">Provedores são executados no modo de usuário.</span><span class="sxs-lookup"><span data-stu-id="afaca-107">Providers execute in user mode.</span></span> <span data-ttu-id="afaca-108">Por causa disso, aplicativos de modo de usuário, como aplicativos de impressão e exibição, podem usar qualquer técnica para comunicação entre processos, como pipes nomeados, mapeamento de arquivos ou RPC.</span><span class="sxs-lookup"><span data-stu-id="afaca-108">Because of this, user-mode applications, such as print and display applications, can use any technique for interprocess communication, such as named pipes, file mapping, or RPC.</span></span> <span data-ttu-id="afaca-109">No entanto, os aplicativos em modo kernel devem fornecer uma interface IOCTL que retorna os dados de desempenho para o provedor.</span><span class="sxs-lookup"><span data-stu-id="afaca-109">However, kernel-mode applications must provide an IOCTL interface that returns the performance data to the provider.</span></span>

> [!WARNING]
> <span data-ttu-id="afaca-110">Não use COM como o mecanismo IPC.</span><span class="sxs-lookup"><span data-stu-id="afaca-110">Do not use COM as the IPC mechanism.</span></span> <span data-ttu-id="afaca-111">O sistema não pode garantir o estado de inicialização COM do thread que chama a interface.</span><span class="sxs-lookup"><span data-stu-id="afaca-111">The system cannot guarantee the COM initialization state of the thread calling the interface.</span></span> <span data-ttu-id="afaca-112">Portanto, a DLL pode não conseguir inicializar com e coletar os dados com êxito.</span><span class="sxs-lookup"><span data-stu-id="afaca-112">Therefore, the DLL may not be able to successfully initialize COM and collect the data.</span></span>

 

 

 



