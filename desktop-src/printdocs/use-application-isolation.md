---
description: Os aplicativos podem declarar o isolamento de driver de impressora em seu manifesto de aplicativo para isolar o aplicativo do driver de impressora e melhorar a confiabilidade dos aplicativos.
ms.assetid: 80650C46-AC96-46FD-894A-4F34B056AB79
ms.topic: article
title: 'Como: usar o isolamento de aplicativos'
ms.date: 05/31/2018
ms.openlocfilehash: 28c2a143406e9501662e0ddf7294abfb25e362b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169453"
---
# <a name="how-to-use-application-isolation"></a><span data-ttu-id="53f1f-103">Como: usar o isolamento de aplicativos</span><span class="sxs-lookup"><span data-stu-id="53f1f-103">How To: Use Application Isolation</span></span>

<span data-ttu-id="53f1f-104">Os aplicativos podem declarar o isolamento de driver de impressora em seu manifesto de aplicativo para isolar o aplicativo do driver de impressora e melhorar a confiabilidade do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="53f1f-104">Apps can declare printer-driver isolation in their app manifest to isolate the app from the printer driver and improve the app's reliability.</span></span> <span data-ttu-id="53f1f-105">O serviço de impressão do Windows permite que os drivers de impressora sejam executados em processos separados do processo no qual o spooler de impressão é executado.</span><span class="sxs-lookup"><span data-stu-id="53f1f-105">The Windows print service allows printer drivers to run in processes that are separate from the process in which the print spooler runs.</span></span> <span data-ttu-id="53f1f-106">Usando esse recurso, seu aplicativo impede que ele falhe em caso de erro do driver de impressora.</span><span class="sxs-lookup"><span data-stu-id="53f1f-106">Using this feature your app prevents it from crashing in the event the printer driver has an error.</span></span>

<span data-ttu-id="53f1f-107">O isolamento do driver de impressora é implementado no Windows 7 e no Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="53f1f-107">Printer-driver isolation is implemented in Windows 7 and Windows Server 2008 R2.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="53f1f-108">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="53f1f-108">Prerequisites</span></span>

-   <span data-ttu-id="53f1f-109">Um aplicativo de código gerenciado ou da Windows Store que usa a impressão do Windows.</span><span class="sxs-lookup"><span data-stu-id="53f1f-109">A managed-code or Windows Store app that uses Windows printing.</span></span>

## <a name="instructions"></a><span data-ttu-id="53f1f-110">Instruções</span><span class="sxs-lookup"><span data-stu-id="53f1f-110">Instructions</span></span>

### <a name="update-the-app-manifest"></a><span data-ttu-id="53f1f-111">Atualizar o manifesto do aplicativo</span><span class="sxs-lookup"><span data-stu-id="53f1f-111">Update the app manifest</span></span>

<span data-ttu-id="53f1f-112">Habilitar o isolamento de driver de impressora exige que você adicione o elemento **printerDriverIsolation** ao manifesto do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="53f1f-112">Enabling printer-driver isolation requires you to add the **printerDriverIsolation** element to the app's manifest.</span></span> <span data-ttu-id="53f1f-113">Aqui está como:</span><span class="sxs-lookup"><span data-stu-id="53f1f-113">Here's how:</span></span>

1.  <span data-ttu-id="53f1f-114">Edite o manifesto do aplicativo, adicionando o elemento **printerDriverIsolation** com um valor de **true** para o elemento **windowsSettings** do elemento **Application** , conforme mostrado neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="53f1f-114">Edit the app manifest, adding the **printerDriverIsolation** element with a value of **true** to the **windowsSettings** element of the **application** element, as shown in this example.</span></span>
    ```XML
    <application xmlns="urn:schemas-microsoft-com:asm.v3">
        <windowsSettings>
            <printerDriverIsolation xmlns="http://schemas.microsoft.com/SMI/2011/WindowsSettings">true</printerDriverIsolation>
        </windowsSettings>
    </application>
    ```

    

2.  <span data-ttu-id="53f1f-115">Recompile seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="53f1f-115">Rebuild your app.</span></span>

 

 



