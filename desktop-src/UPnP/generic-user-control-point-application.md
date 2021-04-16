---
title: Aplicativo de ponto de controle de usuário genérico
description: O aplicativo genérico do UCP (ponto de controle do usuário) permite que você descubra dispositivos, controle esses dispositivos descobertos e exiba as informações de eventos relacionadas, tudo usando uma interface gráfica.
ms.assetid: 18ac23df-9d69-4a28-91e5-991eb4f3e6ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee56710cc1fafcc8551b34cb53df531f1f8cb601
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104552395"
---
# <a name="generic-user-control-point-application"></a><span data-ttu-id="73ba4-103">Aplicativo de ponto de controle de usuário genérico</span><span class="sxs-lookup"><span data-stu-id="73ba4-103">Generic User Control Point Application</span></span>

<span data-ttu-id="73ba4-104">O aplicativo genérico do UCP (ponto de controle do usuário) permite que você descubra dispositivos, controle esses dispositivos descobertos e exiba as informações de eventos relacionadas, tudo usando uma interface gráfica.</span><span class="sxs-lookup"><span data-stu-id="73ba4-104">The generic user control point (UCP) application allows you to discover devices, control those discovered devices, and view the related eventing information, all using a graphical interface.</span></span>

<span data-ttu-id="73ba4-105">**Para iniciar o aplicativo UCP genérico**</span><span class="sxs-lookup"><span data-stu-id="73ba4-105">**To start the generic UCP application**</span></span>

1.  <span data-ttu-id="73ba4-106">Crie e configure o arquivo de exemplos \\ netds \\ upnp \\ GenericUCP \\ \\devtype.txt cpp (ou \\ o \\ arquivo VisualBasicdevtype.txt) com as informações do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="73ba4-106">Create and configure the samples\\netds\\upnp\\GenericUCP\\CPP\\devtype.txt file (or the \\VisualBasic\\devtype.txt file) with device information.</span></span> <span data-ttu-id="73ba4-107">Esse arquivo permite que você configure o UCP genérico para as pesquisas "localizar por tipo" e "localização assíncrona".</span><span class="sxs-lookup"><span data-stu-id="73ba4-107">This file allows you to configure the generic UCP for the "find by type" and "async find" searches.</span></span> <span data-ttu-id="73ba4-108">Cada linha do arquivo deve conter um tipo de dispositivo e a Descrição relacionada.</span><span class="sxs-lookup"><span data-stu-id="73ba4-108">Each line of the file must contain a device type and the related description.</span></span> <span data-ttu-id="73ba4-109">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="73ba4-109">For example:</span></span>

    ``` syntax
    upnp:rootdevice All Root Devices
    urn:schemas-upnp-org:device:mediaplayer:1    Media Player
    ```

    <span data-ttu-id="73ba4-110">Este exemplo é para um dispositivo de player de mídia fictício.</span><span class="sxs-lookup"><span data-stu-id="73ba4-110">This example is for a fictitious media player device.</span></span> <span data-ttu-id="73ba4-111">O "Player de mídia" no final da segunda linha não faz parte do tipo de dispositivo, é para fins informativos no aplicativo UCP genérico.</span><span class="sxs-lookup"><span data-stu-id="73ba4-111">The "Media Player" at the end of the second line is not a part of the device type, it is for informational purposes in the Generic UCP application.</span></span> <span data-ttu-id="73ba4-112">O mesmo se aplica a "todos os dispositivos raiz" na primeira linha.</span><span class="sxs-lookup"><span data-stu-id="73ba4-112">The same applies to "All Root Devices" in the first line.</span></span>

    <span data-ttu-id="73ba4-113">Adicione uma linha que contenha o tipo de dispositivo e a descrição específicos para cada dispositivo.</span><span class="sxs-lookup"><span data-stu-id="73ba4-113">Add a line that contains your specific device type and description for each device.</span></span>

2.  <span data-ttu-id="73ba4-114">Crie e configure o \\ arquivo netds \\ UPnP \\ GenericUCP \\ cpp \\udn.txt (ou o \\ arquivo VISUALBASIC \\udn.txt) com informações de UDN para seus dispositivos.</span><span class="sxs-lookup"><span data-stu-id="73ba4-114">Create and configure the samples\\netds\\upnp\\GenericUCP\\CPP\\udn.txt file (or the \\VisualBasic\\udn.txt file) with UDN information for your devices.</span></span> <span data-ttu-id="73ba4-115">Esse arquivo permite que você configure o UCP genérico para a pesquisa "localizar por UDN".</span><span class="sxs-lookup"><span data-stu-id="73ba4-115">This file allows you to configure the generic UCP for the "find by UDN" search.</span></span> <span data-ttu-id="73ba4-116">Cada linha usa a seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="73ba4-116">Each line uses the following form:</span></span>

    ``` syntax
    uuid:{7d50b574-4213-4b88-84d9-e5c9241fcb3a}
    ```

    <span data-ttu-id="73ba4-117">Adicione uma linha que contém seu UDN específico para cada dispositivo.</span><span class="sxs-lookup"><span data-stu-id="73ba4-117">Add a line that contains your specific UDN for each device.</span></span>

3.  <span data-ttu-id="73ba4-118">Execute GenericUCP.exe.</span><span class="sxs-lookup"><span data-stu-id="73ba4-118">Run GenericUCP.exe.</span></span> <span data-ttu-id="73ba4-119">A janela **UCP genérica** é exibida.</span><span class="sxs-lookup"><span data-stu-id="73ba4-119">The **Generic UCP** window appears.</span></span>

    ![janela UCP genérica](images/generic-ucp.png)

> [!Note]  
> <span data-ttu-id="73ba4-121">A funcionalidade **Exibir apresentação** e **Exibir serviço desc.** não está implementada no código de exemplo C++.</span><span class="sxs-lookup"><span data-stu-id="73ba4-121">The **View Presentation** and **View Service Desc.** functionality is not implemented in the C++ sample code.</span></span>

 

 

 




