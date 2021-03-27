---
description: A criação de um aplicativo habilitado para AutoRun é um procedimento simples. Este tópico usa o CD-ROM como um exemplo (foi a primeira mídia para implementar essa tecnologia), mas hoje há muitos tipos de mídia diferentes que podem usá-lo.
title: Criando um aplicativo AutoRun-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0d01f4a2-64c4-4b31-9fc9-361da6825ab8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 24a944b011c926d1638e5d0bcb0d35fc348e5783
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090030"
---
# <a name="creating-an-autorun-enabled-application"></a><span data-ttu-id="9153e-104">Criando um aplicativo AutoRun-Enabled</span><span class="sxs-lookup"><span data-stu-id="9153e-104">Creating an AutoRun-Enabled Application</span></span>

<span data-ttu-id="9153e-105">A criação de um aplicativo habilitado para AutoRun é um procedimento simples.</span><span class="sxs-lookup"><span data-stu-id="9153e-105">Creating an AutoRun-enabled application is a straightforward procedure.</span></span> <span data-ttu-id="9153e-106">Este tópico usa o CD-ROM como um exemplo (foi a primeira mídia para implementar essa tecnologia), mas hoje há muitos tipos de mídia diferentes que podem usá-lo.</span><span class="sxs-lookup"><span data-stu-id="9153e-106">This topic uses CD-ROM as an example (it was the first medium to implement this technology) but today there are many different media types that can use it.</span></span>

<span data-ttu-id="9153e-107">Para habilitar o AutoRun em seu aplicativo, você simplesmente inclui dois arquivos essenciais:</span><span class="sxs-lookup"><span data-stu-id="9153e-107">To enable AutoRun in your application, you simply include two essential files:</span></span>

-   <span data-ttu-id="9153e-108">Um arquivo autorun. inf</span><span class="sxs-lookup"><span data-stu-id="9153e-108">An Autorun.inf file</span></span>
-   <span data-ttu-id="9153e-109">Um aplicativo de inicialização</span><span class="sxs-lookup"><span data-stu-id="9153e-109">A startup application</span></span>

<span data-ttu-id="9153e-110">Quando um usuário insere um disco em uma unidade de CD-ROM em um computador compatível com AutoRun, o sistema verifica imediatamente se o disco tem um sistema de arquivos de computador pessoal.</span><span class="sxs-lookup"><span data-stu-id="9153e-110">When a user inserts a disc into a CD-ROM drive on a AutoRun-compatible computer, the system immediately checks to see if the disc has a personal computer file system.</span></span> <span data-ttu-id="9153e-111">Se tiver, o sistema pesquisará um arquivo chamado [autorun. inf](#creating-an-autoruninf-file).</span><span class="sxs-lookup"><span data-stu-id="9153e-111">If it does, the system searches for a file named [Autorun.inf](#creating-an-autoruninf-file).</span></span> <span data-ttu-id="9153e-112">Esse arquivo especifica um aplicativo de instalação que será executado junto com uma variedade de configurações opcionais.</span><span class="sxs-lookup"><span data-stu-id="9153e-112">This file specifies a setup application that will be run, along with a variety of optional settings.</span></span> <span data-ttu-id="9153e-113">O aplicativo de inicialização normalmente instala, desinstala, configura e, talvez, executa o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9153e-113">The startup application typically installs, uninstalls, configures, and perhaps runs the application.</span></span>

-   [<span data-ttu-id="9153e-114">Criando um arquivo autorun. inf</span><span class="sxs-lookup"><span data-stu-id="9153e-114">Creating an Autorun.inf File</span></span>](#creating-an-autoruninf-file)
-   <span data-ttu-id="9153e-115">[A \[ \] seção DeviceInstall](#the-deviceinstall-section)</span><span class="sxs-lookup"><span data-stu-id="9153e-115">[The \[DeviceInstall\] Section](#the-deviceinstall-section)</span></span>
-   [<span data-ttu-id="9153e-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9153e-116">Related topics</span></span>](#related-topics)

## <a name="creating-an-autoruninf-file"></a><span data-ttu-id="9153e-117">Criando um arquivo autorun. inf</span><span class="sxs-lookup"><span data-stu-id="9153e-117">Creating an Autorun.inf File</span></span>

<span data-ttu-id="9153e-118">Autorun. inf é um arquivo de texto localizado no diretório raiz do CD-ROM que contém seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9153e-118">Autorun.inf is a text file located in the root directory of the CD-ROM that contains your application.</span></span> <span data-ttu-id="9153e-119">Sua função principal é fornecer ao sistema o nome e o local do programa de inicialização do aplicativo que será executado quando o disco for inserido.</span><span class="sxs-lookup"><span data-stu-id="9153e-119">Its primary function is to provide the system with the name and location of the application's startup program that will be run when the disc is inserted.</span></span>

> [!Note]  
> <span data-ttu-id="9153e-120">Não há suporte para arquivos autorun. inf no Windows XP para unidades que retornam \_ removível de unidade de [**GetDriveType**](/windows/win32/api/fileapi/nf-fileapi-getdrivetypea).</span><span class="sxs-lookup"><span data-stu-id="9153e-120">Autorun.inf files are not supported under Windows XP for drives that return DRIVE\_REMOVABLE from [**GetDriveType**](/windows/win32/api/fileapi/nf-fileapi-getdrivetypea).</span></span>

 

<span data-ttu-id="9153e-121">O arquivo autorun. inf também pode conter informações opcionais, incluindo:</span><span class="sxs-lookup"><span data-stu-id="9153e-121">The Autorun.inf file can also contain optional information including:</span></span>

-   <span data-ttu-id="9153e-122">O nome de um arquivo que contém um ícone que representará a unidade de CD-ROM do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9153e-122">The name of a file that contains an icon that will represent your application's CD-ROM drive.</span></span> <span data-ttu-id="9153e-123">Esse ícone será exibido pelo Windows Explorer no lugar do ícone de unidade padrão.</span><span class="sxs-lookup"><span data-stu-id="9153e-123">This icon will be displayed by Windows Explorer in place of the standard drive icon.</span></span>
-   <span data-ttu-id="9153e-124">Comandos adicionais para o menu de atalho que é exibido quando o usuário clica com o botão direito do mouse no ícone do CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="9153e-124">Additional commands for the shortcut menu that is displayed when the user right-clicks the CD-ROM icon.</span></span> <span data-ttu-id="9153e-125">Você também pode especificar o comando padrão que é executado quando o usuário clica duas vezes no ícone.</span><span class="sxs-lookup"><span data-stu-id="9153e-125">You can also specify the default command that is run when the user double-clicks the icon.</span></span>

<span data-ttu-id="9153e-126">Os arquivos autorun. inf são semelhantes aos arquivos. ini.</span><span class="sxs-lookup"><span data-stu-id="9153e-126">Autorun.inf files are similar to .ini files.</span></span> <span data-ttu-id="9153e-127">Elas consistem em uma ou mais seções, cada uma com um nome entre colchetes.</span><span class="sxs-lookup"><span data-stu-id="9153e-127">They consist of one or more sections, each headed by a name enclosed in square brackets.</span></span> <span data-ttu-id="9153e-128">Cada seção contém uma série de comandos que serão executados pelo shell quando o disco for inserido.</span><span class="sxs-lookup"><span data-stu-id="9153e-128">Each section contains a series of commands that will be run by the Shell when the disc is inserted.</span></span> <span data-ttu-id="9153e-129">Há duas seções que estão definidas no momento para arquivos autorun. inf.</span><span class="sxs-lookup"><span data-stu-id="9153e-129">There are two sections that are currently defined for Autorun.inf files.</span></span>

-   <span data-ttu-id="9153e-130">A seção **\[ autorun \]** contém os comandos padrão de Autorun.</span><span class="sxs-lookup"><span data-stu-id="9153e-130">The **\[autorun\]** section contains the default AutoRun commands.</span></span> <span data-ttu-id="9153e-131">Todos os arquivos autorun. inf devem ter uma seção de **\[ autorun \]** .</span><span class="sxs-lookup"><span data-stu-id="9153e-131">All Autorun.inf files must have an **\[autorun\]** section.</span></span>
-   <span data-ttu-id="9153e-132">Uma seção opcional **\[ autorun. \] Alpha** pode ser incluída para sistemas em execução em computadores baseados em RISC.</span><span class="sxs-lookup"><span data-stu-id="9153e-132">An optional **\[autorun.alpha\]** section can be included for systems running on RISC-based computers.</span></span> <span data-ttu-id="9153e-133">Quando um disco é inserido em uma unidade de CD-ROM em um sistema baseado em RISC, o Shell executará os comandos nesta seção em vez daqueles na seção de **\[ autorun \]** .</span><span class="sxs-lookup"><span data-stu-id="9153e-133">When a disc is inserted in a CD-ROM drive on a RISC-based system, the Shell will run the commands in this section instead of those in the **\[autorun\]** section.</span></span>

> [!Note]  
> <span data-ttu-id="9153e-134">O Shell verifica primeiro uma seção específica da arquitetura.</span><span class="sxs-lookup"><span data-stu-id="9153e-134">The Shell checks for an architecture-specific section first.</span></span> <span data-ttu-id="9153e-135">Se ele não encontrar um, ele usará as informações na seção **\[ autorun \]** .</span><span class="sxs-lookup"><span data-stu-id="9153e-135">If it does not find one, it uses the information in the **\[autorun\]** section.</span></span> <span data-ttu-id="9153e-136">Depois que o Shell encontra uma seção, ele ignora todas as outras, portanto, cada seção deve ser independente.</span><span class="sxs-lookup"><span data-stu-id="9153e-136">After the Shell finds a section, it ignores all others, so each section must be self-contained.</span></span>

 

<span data-ttu-id="9153e-137">Cada seção contém uma série de comandos que determinam como ocorre a operação de execução automática.</span><span class="sxs-lookup"><span data-stu-id="9153e-137">Each section contains a series of commands that determine how the Autorun operation takes place.</span></span> <span data-ttu-id="9153e-138">Há cinco comandos disponíveis.</span><span class="sxs-lookup"><span data-stu-id="9153e-138">There are five commands available.</span></span>



| <span data-ttu-id="9153e-139">Comando</span><span class="sxs-lookup"><span data-stu-id="9153e-139">Command</span></span>                         | <span data-ttu-id="9153e-140">Descrição</span><span class="sxs-lookup"><span data-stu-id="9153e-140">Description</span></span>                                                                            |
|---------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="9153e-141">DefaultIcon</span><span class="sxs-lookup"><span data-stu-id="9153e-141">defaulticon</span></span>](autorun-cmds.md) | <span data-ttu-id="9153e-142">Especifica o ícone padrão para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9153e-142">Specifies the default icon for the application.</span></span>                                        |
| [<span data-ttu-id="9153e-143">cone</span><span class="sxs-lookup"><span data-stu-id="9153e-143">icon</span></span>](autorun-cmds.md)        | <span data-ttu-id="9153e-144">Especifica o caminho e o nome do arquivo de um ícone específico do aplicativo para a unidade de CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="9153e-144">Specifies the path and file name of an application-specific icon for the CD-ROM drive.</span></span> |
| [<span data-ttu-id="9153e-145">open</span><span class="sxs-lookup"><span data-stu-id="9153e-145">open</span></span>](autorun-cmds.md)        | <span data-ttu-id="9153e-146">Especifica o caminho e o nome de arquivo do aplicativo de inicialização.</span><span class="sxs-lookup"><span data-stu-id="9153e-146">Specifies the path and file name of the startup application.</span></span>                           |
| [<span data-ttu-id="9153e-147">useautorun</span><span class="sxs-lookup"><span data-stu-id="9153e-147">useautorun</span></span>](autorun-cmds.md)  | <span data-ttu-id="9153e-148">Especifica que os recursos de reprodução automática v2 devem ser usados se houver suporte.</span><span class="sxs-lookup"><span data-stu-id="9153e-148">Specifies that Autoplay V2 features should be used if supported.</span></span>                       |
| [<span data-ttu-id="9153e-149">Shell</span><span class="sxs-lookup"><span data-stu-id="9153e-149">shell</span></span>](autorun-cmds.md)       | <span data-ttu-id="9153e-150">Define o comando padrão no menu de atalho do CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="9153e-150">Defines the default command in the CD-ROM's shortcut menu.</span></span>                             |
| [<span data-ttu-id="9153e-151">verbo do Shell \_</span><span class="sxs-lookup"><span data-stu-id="9153e-151">shell\_verb</span></span>](autorun-cmds.md) | <span data-ttu-id="9153e-152">Adiciona comandos ao menu de atalho do CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="9153e-152">Adds commands to the CD-ROM's shortcut menu.</span></span>                                           |



 

<span data-ttu-id="9153e-153">Veja a seguir um exemplo de um arquivo autorun. inf simples.</span><span class="sxs-lookup"><span data-stu-id="9153e-153">The following is an example of a simple Autorun.inf file.</span></span> <span data-ttu-id="9153e-154">Ele especifica Filename.exe como o aplicativo de inicialização.</span><span class="sxs-lookup"><span data-stu-id="9153e-154">It specifies Filename.exe as the startup application.</span></span> <span data-ttu-id="9153e-155">O segundo ícone no Filename.exe representará a unidade de CD-ROM em vez do ícone de unidade padrão.</span><span class="sxs-lookup"><span data-stu-id="9153e-155">The second icon in Filename.exe will represent the CD-ROM drive instead of the standard drive icon.</span></span>


```
[autorun] 
open=Filename.exe 
icon=Filename.exe,1
```



<span data-ttu-id="9153e-156">Este exemplo de Autorun. inf executa aplicativos de inicialização diferentes, dependendo do tipo de computador.</span><span class="sxs-lookup"><span data-stu-id="9153e-156">This Autorun.inf sample runs different startup applications depending on the type of computer.</span></span>


```
[autorun] 
open=Filename_x86.exe 
icon=IconFile.ico 

[autorun.alpha] 
open=Filename_RISC.exe 
icon=IconFile.ico
```



## <a name="the-deviceinstall-section"></a><span data-ttu-id="9153e-157">A \[ \] seção DeviceInstall</span><span class="sxs-lookup"><span data-stu-id="9153e-157">The \[DeviceInstall\] Section</span></span>

<span data-ttu-id="9153e-158">Você pode usar a seção **\[ DeviceInstall \]** em qualquer mídia removível.</span><span class="sxs-lookup"><span data-stu-id="9153e-158">You can use the **\[DeviceInstall\]** section on any removable media.</span></span> <span data-ttu-id="9153e-159">Há suporte apenas no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9153e-159">It is supported only under Windows XP.</span></span> <span data-ttu-id="9153e-160">Você usa **DriverPath** para especificar um caminho de diretório no qual o Windows XP procura por arquivos de driver, o que impede uma pesquisa demorada por todo o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="9153e-160">You use **DriverPath** to specify a directory path where Windows XP searches for driver files, which prevents a lengthy search through the entire contents.</span></span>

<span data-ttu-id="9153e-161">Use a seção **\[ DeviceInstall \]** com uma instalação de driver para especificar diretórios em que o Windows XP deve pesquisar arquivos de driver na mídia.</span><span class="sxs-lookup"><span data-stu-id="9153e-161">You use the **\[DeviceInstall\]** section with a driver installation to specify directories where Windows XP should search the media for driver files.</span></span> <span data-ttu-id="9153e-162">No Windows XP, toda a mídia não é mais pesquisada por padrão, portanto, exigir **\[ DeviceInstall \]** para especificar locais de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="9153e-162">Under Windows XP, entire media are no longer searched by default, therefore requiring **\[DeviceInstall\]** to specify search locations.</span></span> <span data-ttu-id="9153e-163">A seguir estão as únicas mídias removíveis que o Windows XP pesquisa totalmente sem uma seção **\[ DeviceInstall \]** em um arquivo autorun. inf.</span><span class="sxs-lookup"><span data-stu-id="9153e-163">The following are the only removable media that Windows XP fully searches without a **\[DeviceInstall\]** section in an Autorun.inf file.</span></span>

-   <span data-ttu-id="9153e-164">Disquetes encontrados nas unidades A ou B.</span><span class="sxs-lookup"><span data-stu-id="9153e-164">Floppy disks found in drives A or B.</span></span>
-   <span data-ttu-id="9153e-165">Mídia de CD/DVD com menos de 1 gigabyte (GB) de tamanho.</span><span class="sxs-lookup"><span data-stu-id="9153e-165">CD/DVD media less that 1 gigabyte (GB) in size.</span></span>

<span data-ttu-id="9153e-166">Todas as outras mídias devem incluir uma seção **\[ DeviceInstall \]** para o Windows XP detectar quaisquer drivers armazenados nessa mídia.</span><span class="sxs-lookup"><span data-stu-id="9153e-166">All other media must include a **\[DeviceInstall\]** section for Windows XP to detect any drivers stored on that media.</span></span>

> [!Note]  
> <span data-ttu-id="9153e-167">Assim como acontece com a seção **\[ autorun \]** , a seção **\[ DeviceInstall \]** pode ser específica da arquitetura.</span><span class="sxs-lookup"><span data-stu-id="9153e-167">As with the **\[AutoRun\]** section, the **\[DeviceInstall\]** section can be architecture-specific.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="9153e-168">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9153e-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9153e-169">Como implementar aplicativos de inicialização autorun</span><span class="sxs-lookup"><span data-stu-id="9153e-169">How to Implement Autorun Startup Applications</span></span>](how-to-implement-autorun-startup-applications.md)
</dt> <dt>

[<span data-ttu-id="9153e-170">Gravando um aplicativo de instalação de dispositivo</span><span class="sxs-lookup"><span data-stu-id="9153e-170">Writing a Device Installation Application</span></span>](/windows-hardware/drivers/install/writing-a-device-installation-application)
</dt> </dl>

 

 
