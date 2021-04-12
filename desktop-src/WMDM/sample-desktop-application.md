---
title: Aplicativo de desktop de exemplo
description: Aplicativo de desktop de exemplo
ms.assetid: 3736dd01-b02f-4056-b19b-0e7cc6c9aa67
keywords:
- Gerenciador de Dispositivos de mídia do Windows, amostras
- Gerenciador de Dispositivos, exemplos
- aplicativos de área de trabalho, exemplos
- Windows Media Gerenciador de Dispositivos, exemplo de aplicativo da área de trabalho
- Gerenciador de Dispositivos, exemplo de aplicativo de desktop
- aplicativo de exemplo wmdmapp
- exemplos, aplicativos de desktop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f4008a25ca4448d4d4be7c9f667c5a9e4f08023
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364052"
---
# <a name="sample-desktop-application"></a><span data-ttu-id="46287-110">Aplicativo de desktop de exemplo</span><span class="sxs-lookup"><span data-stu-id="46287-110">Sample Desktop Application</span></span>

<span data-ttu-id="46287-111">O Windows Media Gerenciador de Dispositivos é fornecido com um aplicativo de desktop de exemplo chamado wmdmapp.</span><span class="sxs-lookup"><span data-stu-id="46287-111">The Windows Media Device Manager ships with a sample desktop application called wmdmapp.</span></span> <span data-ttu-id="46287-112">Esse aplicativo tem uma interface gráfica do usuário que permite que você procure dispositivos conectados, crie listas de reprodução no dispositivo e arraste arquivos de mídia para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="46287-112">This application has a graphical user interface that allows you to browse connected devices, create playlists on the device, and drag media files to the device.</span></span>

<span data-ttu-id="46287-113">Este aplicativo de exemplo consiste em duas partes:</span><span class="sxs-lookup"><span data-stu-id="46287-113">This sample application consists of two pieces:</span></span>

-   <span data-ttu-id="46287-114">wmdapp.exe, um executável que exibe uma janela e executa a maior parte da interface do usuário e a funcionalidade básica do programa, e</span><span class="sxs-lookup"><span data-stu-id="46287-114">wmdapp.exe, an executable that displays a window and performs most of the user interface and basic functionality of the program, and</span></span>
-   <span data-ttu-id="46287-115">proghelp.dll, uma DLL auxiliar que executa funções de utilitário para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="46287-115">proghelp.dll, a helper DLL that performs utility functions for the application.</span></span> <span data-ttu-id="46287-116">Você deve registrar essa DLL depois de compilar o projeto.</span><span class="sxs-lookup"><span data-stu-id="46287-116">You must register this DLL after building the project.</span></span>

<span data-ttu-id="46287-117">Para compilar o aplicativo de exemplo, você pode usar o Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="46287-117">To compile the sample application, you can use Visual Studio.</span></span> <span data-ttu-id="46287-118">A seção a seguir descreve como isso é feito:</span><span class="sxs-lookup"><span data-stu-id="46287-118">The following section describes how this is done:</span></span>

-   [<span data-ttu-id="46287-119">Compilando o aplicativo de exemplo usando o Visual Studio</span><span class="sxs-lookup"><span data-stu-id="46287-119">Compiling the Sample Application Using Visual Studio</span></span>](compiling-the-sample-application-using-visual-studio.md)

<span data-ttu-id="46287-120">Depois de compilar o projeto, registre o arquivo de proghelp.dll.</span><span class="sxs-lookup"><span data-stu-id="46287-120">After compiling the project, register the proghelp.dll file.</span></span> <span data-ttu-id="46287-121">Para registrar essa DLL, abra um prompt de comando e navegue até o diretório que contém essa DLL e digite `regsvr32 proghelp.dll` .</span><span class="sxs-lookup"><span data-stu-id="46287-121">To register this DLL, open a command prompt and browse to the directory containing this DLL and type `regsvr32 proghelp.dll`.</span></span>

 

 




