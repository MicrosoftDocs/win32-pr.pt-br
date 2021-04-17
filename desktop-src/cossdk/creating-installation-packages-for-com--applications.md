---
description: Criando pacotes de instalação para aplicativos COM+
ms.assetid: 3ef7b280-b521-4cd2-9906-013c9dfe16ab
title: Criando pacotes de instalação para aplicativos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ec34852ab405d965fa1ad8f8fb5892616d1347
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782643"
---
# <a name="creating-installation-packages-for-com-applications"></a><span data-ttu-id="3c2c9-103">Criando pacotes de instalação para aplicativos COM+</span><span class="sxs-lookup"><span data-stu-id="3c2c9-103">Creating Installation Packages for COM+ Applications</span></span>

<span data-ttu-id="3c2c9-104">Você pode usar a ferramenta administrativa serviços de componentes ou a biblioteca de administração COM+ para criar pacotes de instalação para aplicativos COM+ e proxies de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3c2c9-104">You can use the Component Services administrative tool or the COM+ Administration Library to create installation packages for COM+ applications and application proxies.</span></span>

<span data-ttu-id="3c2c9-105">O COM+ gera Windows Installer pacotes de instalação, que em um único arquivo contém todas as partes necessárias para instalar um aplicativo COM+ em outro computador.</span><span class="sxs-lookup"><span data-stu-id="3c2c9-105">COM+ generates Windows Installer installation packages, which in a single file contain all the necessary pieces to install a COM+ application on another computer.</span></span>

<span data-ttu-id="3c2c9-106">Ao exportar um aplicativo COM+, a ferramenta administrativa serviços de componentes determina o conjunto de classes, componentes e seus atributos do aplicativo, bem como atributos de nível de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3c2c9-106">When exporting a COM+ application, the Component Services administrative tool determines the application's set of classes, components, and their attributes, as well as application-level attributes.</span></span> <span data-ttu-id="3c2c9-107">A partir dessas informações, a ferramenta administrativa serviços de componentes gera um único arquivo. msi, que contém o seguinte:</span><span class="sxs-lookup"><span data-stu-id="3c2c9-107">From this information, the Component Services administrative tool generates a single .msi file, which contains the following:</span></span>

-   <span data-ttu-id="3c2c9-108">Windows Installer tabelas com informações de registro COM (consulte a documentação do Windows Installer para obter detalhes).</span><span class="sxs-lookup"><span data-stu-id="3c2c9-108">Windows Installer tables with COM registration information (see the Windows Installer documentation for details).</span></span>
-   <span data-ttu-id="3c2c9-109">Um arquivo. gráfica que contém os atributos do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3c2c9-109">An .apl file containing the application's attributes.</span></span> <span data-ttu-id="3c2c9-110">(Esse é um arquivo interno; o formato desse arquivo não está documentado.)</span><span class="sxs-lookup"><span data-stu-id="3c2c9-110">(This is an internal file; the format of this file is not documented.)</span></span>
-   <span data-ttu-id="3c2c9-111">DLLs e bibliotecas de tipos que descrevem as interfaces implementadas pelas classes do aplicativo COM+.</span><span class="sxs-lookup"><span data-stu-id="3c2c9-111">DLLs and type libraries that describe the interfaces implemented by the COM+ application's classes.</span></span>

<span data-ttu-id="3c2c9-112">Além do arquivo. msi, a ferramenta administrativa serviços de componentes gera um arquivo de gabinete (. cab).</span><span class="sxs-lookup"><span data-stu-id="3c2c9-112">In addition to the .msi file, the Component Services administrative tool generates a cabinet (.cab) file.</span></span> <span data-ttu-id="3c2c9-113">Esse arquivo encapsula o arquivo. msi, permitindo que o desenvolvedor implante o aplicativo COM+ por meio do Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="3c2c9-113">This file wraps the .msi file, allowing the developer to deploy the COM+ application through Microsoft Internet Explorer.</span></span>

> [!Note]  
> <span data-ttu-id="3c2c9-114">Ao exportar um aplicativo COM+, a ferramenta administrativa serviços de componentes empacota apenas as partes COM+ padrão do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3c2c9-114">When exporting a COM+ application, the Component Services administrative tool packages only the standard COM+ parts of the application.</span></span> <span data-ttu-id="3c2c9-115">Ele não empacota, por exemplo, quaisquer arquivos de dados ou DLL dependentes.</span><span class="sxs-lookup"><span data-stu-id="3c2c9-115">It does not package, for example, any dependent DLL or data files.</span></span> <span data-ttu-id="3c2c9-116">Os arquivos DLL dependentes devem ser instalados primeiro em um computador antes da instalação do aplicativo COM+.</span><span class="sxs-lookup"><span data-stu-id="3c2c9-116">The dependent DLL files must first be installed on a computer prior to installing the COM+ application.</span></span> <span data-ttu-id="3c2c9-117">Como alternativa, você pode usar a ferramenta de criação de Windows Installer para adicionar esses arquivos dependentes ao arquivo. msi gerado pela ferramenta administrativa serviços de componentes.</span><span class="sxs-lookup"><span data-stu-id="3c2c9-117">Alternatively, you can use the Windows Installer authoring tool to add these dependent files to the .msi file generated by the Component Services administrative tool.</span></span> <span data-ttu-id="3c2c9-118">(Consulte a documentação do Windows Installer para obter detalhes.)</span><span class="sxs-lookup"><span data-stu-id="3c2c9-118">(See the Windows Installer documentation for details.)</span></span>

 

## <a name="installing-com-applications-on-other-computers"></a><span data-ttu-id="3c2c9-119">Instalando aplicativos COM+ em outros computadores</span><span class="sxs-lookup"><span data-stu-id="3c2c9-119">Installing COM+ Applications on Other Computers</span></span>

<span data-ttu-id="3c2c9-120">O arquivo de Windows Installer (. msi) gerado pela ferramenta administrativa serviços de componentes pode ser usado para instalar o aplicativo COM+ em outro computador.</span><span class="sxs-lookup"><span data-stu-id="3c2c9-120">The Windows Installer (.msi) file generated by the Component Services administrative tool can be used to install the COM+ application on another computer.</span></span> <span data-ttu-id="3c2c9-121">O arquivo. msi que contém um aplicativo COM+ pode ser instalado somente em computadores que dão suporte a serviços COM+.</span><span class="sxs-lookup"><span data-stu-id="3c2c9-121">The .msi file containing a COM+ application can be installed only on computers that support COM+ services.</span></span> <span data-ttu-id="3c2c9-122">Para obter procedimentos detalhados sobre a implantação de aplicativos COM+, consulte "Instalando aplicativos COM+" na ajuda da administração de serviços de componentes.</span><span class="sxs-lookup"><span data-stu-id="3c2c9-122">For detailed procedures on deploying COM+ applications, see "Installing COM+ Applications," in the Component Services Administration Help.</span></span>

<span data-ttu-id="3c2c9-123">A menos que o arquivo. msi seja modificado usando uma ferramenta de criação de Windows Installer, os aplicativos COM+ instalados usando o Windows Installer aparecem no painel de controle adicionar ou remover programas.</span><span class="sxs-lookup"><span data-stu-id="3c2c9-123">Unless the .msi file is modified using a Windows Installer authoring tool, COM+ applications installed by using the Windows Installer appear in the Add/Remove Programs control panel.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c2c9-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3c2c9-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c2c9-125">Implantando proxies de aplicativo</span><span class="sxs-lookup"><span data-stu-id="3c2c9-125">Deploying Application Proxies</span></span>](deploying-application-proxies.md)
</dt> <dt>

[<span data-ttu-id="3c2c9-126">O catálogo COM+</span><span class="sxs-lookup"><span data-stu-id="3c2c9-126">The COM+ Catalog</span></span>](the-com--catalog.md)
</dt> </dl>

 

 



