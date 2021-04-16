---
description: O procedimento a seguir demonstra como depurar um monitor.
ms.assetid: 499f409c-e25a-4ab3-b0aa-e6b308fc7169
title: Depurando um monitor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4641818b7f1cd1740c2732ced5527a2e278793a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505849"
---
# <a name="debugging-a-monitor"></a><span data-ttu-id="13293-103">Depurando um monitor</span><span class="sxs-lookup"><span data-stu-id="13293-103">Debugging a Monitor</span></span>

<span data-ttu-id="13293-104">O procedimento a seguir demonstra como depurar um monitor.</span><span class="sxs-lookup"><span data-stu-id="13293-104">The following procedure demonstrates how to debug a monitor.</span></span>

<span data-ttu-id="13293-105">**Para depurar um monitor**</span><span class="sxs-lookup"><span data-stu-id="13293-105">**To debug a monitor**</span></span>

1.  <span data-ttu-id="13293-106">Instale a DLL do monitor e o arquivo do banco de dados do programa (. pdb) gerado quando você compilou o monitor no local correto.</span><span class="sxs-lookup"><span data-stu-id="13293-106">Install the monitor DLL and the program database (.pdb) file generated when you compiled the monitor in the correct location.</span></span> <span data-ttu-id="13293-107">Consulte [instalando um monitor para monitor de rede](installing-a-monitor-to-network-monitor.md) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="13293-107">See [Installing a Monitor to Network Monitor](installing-a-monitor-to-network-monitor.md) for further details.</span></span>
2.  <span data-ttu-id="13293-108">Verifique se o serviço de controle de monitor está configurado como um servidor, em vez de um serviço, selecionando Painel de controle, serviços.</span><span class="sxs-lookup"><span data-stu-id="13293-108">Verify that the Monitor Control Service is configured as a server instead of a service by selecting Control Panel, Services.</span></span>
3.  <span data-ttu-id="13293-109">Abra um prompt de comando e vá para o diretório Monitor de Rede.</span><span class="sxs-lookup"><span data-stu-id="13293-109">Open a command prompt and go to the Network Monitor directory.</span></span> <span data-ttu-id="13293-110">Tipo:</span><span class="sxs-lookup"><span data-stu-id="13293-110">Type:</span></span>

    <span data-ttu-id="13293-111">**Mcsvc.exe/RegServer**</span><span class="sxs-lookup"><span data-stu-id="13293-111">**Mcsvc.exe /RegServer**</span></span>

    <span data-ttu-id="13293-112">Depois que a sessão de depuração do monitor for concluída, você poderá retornar o MCSVC para sua condição padrão digitando:</span><span class="sxs-lookup"><span data-stu-id="13293-112">After the monitor debugging session is complete, you can return the MCSVC to its default condition by typing:</span></span>

    <span data-ttu-id="13293-113">**Mcsvc.exe/Service**</span><span class="sxs-lookup"><span data-stu-id="13293-113">**Mcsvc.exe /Service**</span></span>

4.  <span data-ttu-id="13293-114">Em Microsoft Visual Studio, inicie o Microsoft Visual C++.</span><span class="sxs-lookup"><span data-stu-id="13293-114">In Microsoft Visual Studio, launch Microsoft Visual C++.</span></span>
5.  <span data-ttu-id="13293-115">Na opção **arquivo**, **abrir** menu, selecione o nome da dll do monitor.</span><span class="sxs-lookup"><span data-stu-id="13293-115">From the **File**, **Open** menu option, select the name of your monitor DLL.</span></span>
6.  <span data-ttu-id="13293-116">Depois que Microsoft Visual C++ for carregado, clique em **projeto**, **configurações**.</span><span class="sxs-lookup"><span data-stu-id="13293-116">After Microsoft Visual C++ loads, click **Project**, **Settings**.</span></span>
7.  <span data-ttu-id="13293-117">Clique na guia **depurar** em **executável** para sessão de depuração e digite o caminho completo de Mcsvc.exe.</span><span class="sxs-lookup"><span data-stu-id="13293-117">Click the **Debug** tab under **Executable** for debug session and type the full path of Mcsvc.exe.</span></span> <span data-ttu-id="13293-118">Por exemplo, C: \\ Program Files \\ Netmon2 \\Mcsvc.exe.</span><span class="sxs-lookup"><span data-stu-id="13293-118">For example, C:\\Program files\\Netmon2\\Mcsvc.exe.</span></span>
8.  <span data-ttu-id="13293-119">Defina os pontos de interrupção no código.</span><span class="sxs-lookup"><span data-stu-id="13293-119">Set the breakpoints in the code.</span></span>

> [!Note]  
> <span data-ttu-id="13293-120">Não use uma caixa de mensagem para monitorar a depuração.</span><span class="sxs-lookup"><span data-stu-id="13293-120">Do not use a message box for monitor debugging.</span></span> <span data-ttu-id="13293-121">Se o MCSVC estiver sendo executado como um serviço, você não verá o Popup e o MCSVC parecerá travar.</span><span class="sxs-lookup"><span data-stu-id="13293-121">If the MCSVC is running as a service, you will not see the popup, and MCSVC will appear to hang.</span></span>

 

 

 



