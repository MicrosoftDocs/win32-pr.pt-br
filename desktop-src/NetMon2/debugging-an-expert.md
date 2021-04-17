---
description: Use o procedimento a seguir para depurar especialistas escritos em Microsoft Visual C++.
ms.assetid: 7356fcae-3cfe-4a5b-86dd-bebee859fa19
title: Depurando um especialista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e1a7e6b3998eb18d3ea9c5ef25600a6fc08f1eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105770369"
---
# <a name="debugging-an-expert"></a><span data-ttu-id="1fe20-103">Depurando um especialista</span><span class="sxs-lookup"><span data-stu-id="1fe20-103">Debugging an Expert</span></span>

<span data-ttu-id="1fe20-104">Use o procedimento a seguir para depurar especialistas escritos em Microsoft Visual C++.</span><span class="sxs-lookup"><span data-stu-id="1fe20-104">Use the following procedure to debug experts written in Microsoft Visual C++.</span></span>

<span data-ttu-id="1fe20-105">**Depurando um especialista**</span><span class="sxs-lookup"><span data-stu-id="1fe20-105">**Debugging an Expert**</span></span>

1.  <span data-ttu-id="1fe20-106">Instale o especialista (arquivo DLL) e o arquivo de banco de dados do programa (. pdb) gerado quando você compilou o especialista no local correto.</span><span class="sxs-lookup"><span data-stu-id="1fe20-106">Install the expert (DLL file) and the program database file (.pdb) generated when you compiled the expert in the correct location.</span></span> <span data-ttu-id="1fe20-107">Para obter mais detalhes, consulte [instalando um especialista para Monitor de Rede 2,1](installing-an-expert-to-network-monitor-2-1.md).</span><span class="sxs-lookup"><span data-stu-id="1fe20-107">For further details, see [Installing an Expert to Network Monitor 2.1](installing-an-expert-to-network-monitor-2-1.md).</span></span>
2.  <span data-ttu-id="1fe20-108">Iniciar Microsoft Visual C++.</span><span class="sxs-lookup"><span data-stu-id="1fe20-108">Start Microsoft Visual C++.</span></span>
3.  <span data-ttu-id="1fe20-109">No menu **arquivo** , clique em **abrir** e selecione o nome da sua DLL de especialista.</span><span class="sxs-lookup"><span data-stu-id="1fe20-109">From the **File** menu, click **Open** and select the name of your expert DLL.</span></span>
4.  <span data-ttu-id="1fe20-110">Depois que Microsoft Visual C++ for carregado, clique no menu **projeto** e em **configurações**.</span><span class="sxs-lookup"><span data-stu-id="1fe20-110">After Microsoft Visual C++ loads, click the **Project** menu and then click **Settings**.</span></span>
5.  <span data-ttu-id="1fe20-111">Clique em **depurar**.</span><span class="sxs-lookup"><span data-stu-id="1fe20-111">Click **Debug**.</span></span> <span data-ttu-id="1fe20-112">Em **executável para sessão de depuração**, digite o caminho completo de Netmon.exe, por exemplo:</span><span class="sxs-lookup"><span data-stu-id="1fe20-112">Under **Executable for debug session**, type the full path of Netmon.exe, for example:</span></span>

    ``` syntax
    C:\Program files\Netmon2\Netmon.exe
    ```

6.  <span data-ttu-id="1fe20-113">Defina os pontos de interrupção no seu código.</span><span class="sxs-lookup"><span data-stu-id="1fe20-113">Set the breakpoints in your code.</span></span>

 

 



