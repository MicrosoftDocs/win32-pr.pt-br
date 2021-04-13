---
description: 'Para criar um aplicativo para WMI usando C++: você deve inicializar COM, acessar e definir protocolos WMI e executar uma limpeza manual.'
ms.assetid: 0b9b7990-6982-4ba9-8dba-7470990405f7
ms.tgt_platform: multiple
title: Criando um aplicativo WMI usando C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baaa4f7e79828b2cb6cb496254d906182ff611ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297330"
---
# <a name="creating-a-wmi-application-using-c"></a><span data-ttu-id="6f09c-103">Criando um aplicativo WMI usando C++</span><span class="sxs-lookup"><span data-stu-id="6f09c-103">Creating a WMI Application Using C++</span></span>

<span data-ttu-id="6f09c-104">Para criar um aplicativo para WMI usando C++: você deve inicializar COM, acessar e definir protocolos WMI e executar uma limpeza manual.</span><span class="sxs-lookup"><span data-stu-id="6f09c-104">To create an application for WMI using C++: you must initialize COM, access and set WMI protocols, and perform a manual cleanup.</span></span> <span data-ttu-id="6f09c-105">No entanto, o C++ tem a vantagem de flexibilidade e potência.</span><span class="sxs-lookup"><span data-stu-id="6f09c-105">However, C++ does have the advantage of flexibility and power.</span></span> <span data-ttu-id="6f09c-106">Portanto, embora você esteja mais bem atendido no uso do Visual Basic Scripting Edition (VBScript) ou do Windows PowerShell para processos simples, o C++ funciona melhor para aplicativos mais sofisticados e é necessário para escrever [provedores](providing-data-to-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="6f09c-106">Therefore, while you are better served in using Visual Basic Scripting Edition (VBScript) or Windows PowerShell for simple processes, C++ works better for more sophisticated applications and is required for writing [providers](providing-data-to-wmi.md).</span></span>

<span data-ttu-id="6f09c-107">O procedimento a seguir descreve como criar um aplicativo WMI.</span><span class="sxs-lookup"><span data-stu-id="6f09c-107">The following procedure describes how to create a WMI application.</span></span>

<span data-ttu-id="6f09c-108">**Para criar um aplicativo WMI**</span><span class="sxs-lookup"><span data-stu-id="6f09c-108">**To create a WMI application**</span></span>

1.  <span data-ttu-id="6f09c-109">[Inicializar com](initializing-com-for-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="6f09c-109">[Initialize COM](initializing-com-for-a-wmi-application.md).</span></span>

    <span data-ttu-id="6f09c-110">Como o WMI é baseado em tecnologia COM, você deve executar chamadas para as funções [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) e [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) para acessar o WMI.</span><span class="sxs-lookup"><span data-stu-id="6f09c-110">Because WMI is based on COM technology, you must perform calls to the [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) and [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) functions to access WMI.</span></span>

2.  <span data-ttu-id="6f09c-111">[Crie uma conexão com um namespace WMI](creating-a-connection-to-a-wmi-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="6f09c-111">[Create a connection to a WMI namespace](creating-a-connection-to-a-wmi-namespace.md).</span></span>

    <span data-ttu-id="6f09c-112">Por definição, o WMI é executado em um processo diferente do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6f09c-112">By definition, WMI runs in a different process than your application.</span></span> <span data-ttu-id="6f09c-113">Portanto, você deve criar uma conexão entre seu aplicativo e o WMI.</span><span class="sxs-lookup"><span data-stu-id="6f09c-113">Therefore, you must create a connection between your application and WMI.</span></span>

3.  <span data-ttu-id="6f09c-114">[Defina os níveis de segurança na conexão WMI](setting-the-security-levels-on-a-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="6f09c-114">[Set the security levels on the WMI connection](setting-the-security-levels-on-a-wmi-connection.md).</span></span>

    <span data-ttu-id="6f09c-115">Para usar a conexão que você cria para o WMI, você deve definir os níveis de representação e de autenticação para seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6f09c-115">To use the connection you create to WMI, you must set the impersonation and authentication levels for your application.</span></span>

4.  <span data-ttu-id="6f09c-116">Implemente a finalidade do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6f09c-116">Implement the purpose of your application.</span></span>

    <span data-ttu-id="6f09c-117">O WMI expõe uma variedade de interfaces COM usadas para acessar e manipular dados em toda a sua empresa.</span><span class="sxs-lookup"><span data-stu-id="6f09c-117">WMI exposes a variety of COM interfaces use to access and manipulate data across your enterprise.</span></span> <span data-ttu-id="6f09c-118">Para obter mais informações, consulte [manipulando informações de classe e instância](manipulating-class-and-instance-information.md), [recebendo um evento WMI](receiving-a-wmi-event.md)e a [API com para WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="6f09c-118">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md), [Receiving a WMI Event](receiving-a-wmi-event.md), and [COM API for WMI](com-api-for-wmi.md).</span></span>

    <span data-ttu-id="6f09c-119">É aí que deve existir a maior parte do seu aplicativo cliente WMI, como acessar objetos WMI ou manipular dados.</span><span class="sxs-lookup"><span data-stu-id="6f09c-119">This is where the bulk of your WMI client application should exist, such as accessing WMI objects or manipulating data.</span></span>

5.  <span data-ttu-id="6f09c-120">[Limpe e desative seu aplicativo](cleaning-up-and-shutting-down-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="6f09c-120">[Cleanup and shut down your application](cleaning-up-and-shutting-down-a-wmi-application.md).</span></span>

    <span data-ttu-id="6f09c-121">Depois de concluir suas consultas para o WMI, você deve destruir todos os ponteiros COM e desligar o aplicativo corretamente.</span><span class="sxs-lookup"><span data-stu-id="6f09c-121">After you complete your queries to WMI, you should destroy all COM pointers and shut down your application correctly.</span></span>

<span data-ttu-id="6f09c-122">Para obter mais informações e um exemplo de código sobre como criar um aplicativo WMI, consulte [exemplo: Criando um aplicativo WMI](example-creating-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="6f09c-122">For more information and a code example about how to create a WMI application, see [Example: Creating a WMI Application](example-creating-a-wmi-application.md).</span></span>

 

 
