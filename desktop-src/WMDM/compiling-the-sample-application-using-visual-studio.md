---
title: Compilando o aplicativo de exemplo usando o Visual Studio
description: Compilando o aplicativo de exemplo usando o Visual Studio
ms.assetid: 78345cdb-5f0d-4ea8-9492-30386f5fa6ee
keywords:
- Gerenciador de Dispositivos de mídia do Windows, amostras
- Gerenciador de Dispositivos, exemplos
- aplicativos de área de trabalho, exemplos
- Windows Media Gerenciador de Dispositivos, exemplo de aplicativo da área de trabalho
- Gerenciador de Dispositivos, exemplo de aplicativo de desktop
- exemplos, aplicativos de desktop
- exemplos, compilando usando o Visual Studio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf47f7a45ad17711145df810926fafb0f2aedcec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005288"
---
# <a name="compiling-the-sample-application-using-visual-studio"></a><span data-ttu-id="48dd0-110">Compilando o aplicativo de exemplo usando o Visual Studio</span><span class="sxs-lookup"><span data-stu-id="48dd0-110">Compiling the Sample Application Using Visual Studio</span></span>

<span data-ttu-id="48dd0-111">O SDK do Windows Media Gerenciador de Dispositivos inclui uma solução do Visual Studio que é compatível com o Microsoft Visual Studio 2005.</span><span class="sxs-lookup"><span data-stu-id="48dd0-111">The Windows Media Device Manager SDK includes a Visual Studio solution that is compatible with Microsoft Visual Studio 2005.</span></span>

<span data-ttu-id="48dd0-112">Antes de compilar o aplicativo de exemplo, você deve renomear o arquivo de cabeçalho shtypes. h para evitar conflitos com um arquivo com o mesmo nome encontrado no SDK da plataforma Microsoft.</span><span class="sxs-lookup"><span data-stu-id="48dd0-112">Before you compile the sample application, you must rename the header file shtypes.h to prevent conflicts with a file of the same name that is found in the Microsoft Platform SDK.</span></span> <span data-ttu-id="48dd0-113">Por exemplo, você pode renomear <*caminho de instalação do SDK* > \\ WMFSDK11 \\ incluir \\ shtypes. h para <*caminho de instalação do SDK* > \\ WMFSDK11 \\ incluir \\ shtypes. h. backup.</span><span class="sxs-lookup"><span data-stu-id="48dd0-113">For example, you could rename <*SDK Installation Path*>\\WMFSDK11\\include\\shtypes.h to <*SDK Installation Path*>\\WMFSDK11\\include\\shtypes.h.backup.</span></span>

<span data-ttu-id="48dd0-114">Para compilar o aplicativo, inicie uma instância do Visual Studio 2005, abra o arquivo de solução, wmdmapp. sln, que está localizado na pasta <*caminho de instalação do SDK* > \\ WMFSDK11 \\ aplicativos \\ wmdmapp e escolha a opção de **solução compilar/compilar** .</span><span class="sxs-lookup"><span data-stu-id="48dd0-114">To build the application, start an instance of Visual Studio 2005, open the solution file, wmdmapp.sln, which is found in the folder <*SDK installation path*>\\WMFSDK11\\apps\\wmdmapp and choose the **Build/Build Solution** option.</span></span> <span data-ttu-id="48dd0-115">Isso criará dois arquivos de projeto: o projeto auxiliar, proghelp. vcproj, bem como o aplicativo principal wmdmapp. vcproj.</span><span class="sxs-lookup"><span data-stu-id="48dd0-115">This will create two project files: the helper project, proghelp.vcproj, as well as the main application wmdmapp.vcproj.</span></span> <span data-ttu-id="48dd0-116">Além disso, ele criará a DLL auxiliar de progresso e o aplicativo principal (WMDMApp.exe).</span><span class="sxs-lookup"><span data-stu-id="48dd0-116">In addition, it will create the progress helper DLL and the main application (WMDMApp.exe).</span></span>

## <a name="related-topics"></a><span data-ttu-id="48dd0-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="48dd0-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48dd0-118">**Aplicativo de desktop de exemplo**</span><span class="sxs-lookup"><span data-stu-id="48dd0-118">**Sample Desktop Application**</span></span>](sample-desktop-application.md)
</dt> </dl>

 

 




