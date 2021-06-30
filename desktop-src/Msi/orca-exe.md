---
description: Orca.exe é um editor de tabela de banco de dados para criar e editar Windows Installer pacotes e Mesclar módulos.
ms.assetid: 4dddc262-1271-4e00-a986-53380b957b17
title: Orca.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4647b137650bfba521dba3976ea7a1ae66451ce
ms.sourcegitcommit: 967ba3a2a618e6088cb607164a2a924530278645
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113102155"
---
# <a name="orcaexe"></a><span data-ttu-id="f4594-103">Orca.exe</span><span class="sxs-lookup"><span data-stu-id="f4594-103">Orca.exe</span></span>

<span data-ttu-id="f4594-104">Orca.exe é um editor de tabela de banco de dados para criar e editar Windows Installer pacotes e Mesclar módulos.</span><span class="sxs-lookup"><span data-stu-id="f4594-104">Orca.exe is a database table editor for creating and editing Windows Installer packages and merge modules.</span></span> <span data-ttu-id="f4594-105">A ferramenta fornece uma interface gráfica para validação, destacando as entradas específicas em que ocorrem erros de validação ou avisos.</span><span class="sxs-lookup"><span data-stu-id="f4594-105">The tool provides a graphical interface for validation, highlighting the particular entries where validation errors or warnings occur.</span></span>

<span data-ttu-id="f4594-106">Essa ferramenta só está disponível nos [componentes SDK do Windows para desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="f4594-106">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="f4594-107">Ele é fornecido como um arquivo de Orca.msi.</span><span class="sxs-lookup"><span data-stu-id="f4594-107">It is provided as an Orca.msi file.</span></span> <span data-ttu-id="f4594-108">Depois de instalar os componentes de SDK do Windows para os desenvolvedores de Windows Installer, clique duas vezes em Orca.msi para instalar o arquivo de Orca.exe.</span><span class="sxs-lookup"><span data-stu-id="f4594-108">After installing the Windows SDK Components for Windows Installer Developers, double click Orca.msi to install the Orca.exe file.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4594-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f4594-109">Syntax</span></span>

<span data-ttu-id="f4594-110">\**Orca\*\*\*\[\<options>\]\[\<source file>\]*</span><span class="sxs-lookup"><span data-stu-id="f4594-110">**orca** *\[\<options>\]\[\<source file>\]*</span></span>

## <a name="command-line-options"></a><span data-ttu-id="f4594-111">Opções de linha de comando</span><span class="sxs-lookup"><span data-stu-id="f4594-111">Command Line Options</span></span>

<span data-ttu-id="f4594-112">Orca.exe usa as seguintes opções de linha de comando que não diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f4594-112">Orca.exe uses the following case-insensitive command line options.</span></span> <span data-ttu-id="f4594-113">Um delimitador de barra também pode ser usado no lugar de um traço.</span><span class="sxs-lookup"><span data-stu-id="f4594-113">A slash delimiter may also be used in place of a dash.</span></span>



| <span data-ttu-id="f4594-114">Opção</span><span class="sxs-lookup"><span data-stu-id="f4594-114">Option</span></span> | <span data-ttu-id="f4594-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="f4594-115">Description</span></span>                                                 |
|--------|-------------------------------------------------------------|
| <span data-ttu-id="f4594-116">-Q</span><span class="sxs-lookup"><span data-stu-id="f4594-116">-q</span></span>     | <span data-ttu-id="f4594-117">Modo silencioso</span><span class="sxs-lookup"><span data-stu-id="f4594-117">Quiet mode</span></span>                                                  |
| <span data-ttu-id="f4594-118">-S</span><span class="sxs-lookup"><span data-stu-id="f4594-118">-s</span></span>     | <span data-ttu-id="f4594-119"><*banco de dados> esquema* \[ de dados "Orca. dat"-default\]</span><span class="sxs-lookup"><span data-stu-id="f4594-119"><*database*> Schema database \["orca.dat" - default\]</span></span> |
| <span data-ttu-id="f4594-120">-?</span><span class="sxs-lookup"><span data-stu-id="f4594-120">-?</span></span>     | <span data-ttu-id="f4594-121">Caixa de diálogo de ajuda</span><span class="sxs-lookup"><span data-stu-id="f4594-121">Help dialog</span></span>                                                 |



 

<span data-ttu-id="f4594-122">Orca.exe usa as seguintes opções de linha de comando que não diferenciam maiúsculas de minúsculas com módulos de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="f4594-122">Orca.exe uses the following case-insensitive command line options with merge modules.</span></span> <span data-ttu-id="f4594-123">Um delimitador de barra também pode ser usado no lugar de um traço.</span><span class="sxs-lookup"><span data-stu-id="f4594-123">A slash delimiter may also be used in place of a dash.</span></span> <span data-ttu-id="f4594-124">Ao executar uma mesclagem, os> de *origem* -f,-m e <são todos necessários.</span><span class="sxs-lookup"><span data-stu-id="f4594-124">When performing a merge the -f, -m and <*sourcefile*> are all required.</span></span>



| <span data-ttu-id="f4594-125">Opção</span><span class="sxs-lookup"><span data-stu-id="f4594-125">Option</span></span>     | <span data-ttu-id="f4594-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="f4594-126">Description</span></span>                                                                |
|------------|----------------------------------------------------------------------------|
| <span data-ttu-id="f4594-127">-c</span><span class="sxs-lookup"><span data-stu-id="f4594-127">-c</span></span>         | <span data-ttu-id="f4594-128">Confirmar mesclagem no banco de dados se não houver erros.</span><span class="sxs-lookup"><span data-stu-id="f4594-128">Commit merge to database if no errors.</span></span>                                     |
| <span data-ttu-id="f4594-129">-!</span><span class="sxs-lookup"><span data-stu-id="f4594-129">-!</span></span>         | <span data-ttu-id="f4594-130">Confirme a mesclagem em um banco de dados, mesmo se houver erros.</span><span class="sxs-lookup"><span data-stu-id="f4594-130">Commit merge to a database even if there are errors.</span></span>                       |
| <span data-ttu-id="f4594-131">-M</span><span class="sxs-lookup"><span data-stu-id="f4594-131">-m</span></span>         | <span data-ttu-id="f4594-132"><*módulo*> módulo de mesclagem para mesclar no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f4594-132"><*module*> Merge Module to merge into database.</span></span>                      |
| <span data-ttu-id="f4594-133">-f</span><span class="sxs-lookup"><span data-stu-id="f4594-133">-f</span></span>         | <span data-ttu-id="f4594-134">Recurso \[ : \] recurso (s) Feature2 para se conectar ao módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="f4594-134">Feature\[:Feature2\] Feature(s) to connect to Merge Module.</span></span>                |
| <span data-ttu-id="f4594-135">-r</span><span class="sxs-lookup"><span data-stu-id="f4594-135">-r</span></span>         | <span data-ttu-id="f4594-136"><*ID de diretório*> entrada de diretório para o redirecionamento de raiz do módulo.</span><span class="sxs-lookup"><span data-stu-id="f4594-136"><*directory id*> Directory entry for the module root redirection.</span></span>    |
| <span data-ttu-id="f4594-137">-X</span><span class="sxs-lookup"><span data-stu-id="f4594-137">-x</span></span>         | <span data-ttu-id="f4594-138"><o *diretório*> extrair arquivos para uma imagem sob o diretório.</span><span class="sxs-lookup"><span data-stu-id="f4594-138"><*directory*> Extract files to an image under the directory.</span></span>         |
| <span data-ttu-id="f4594-139">-g</span><span class="sxs-lookup"><span data-stu-id="f4594-139">-g</span></span>         | <span data-ttu-id="f4594-140"><linguagem de> de *idiomas* usada para abrir um módulo.</span><span class="sxs-lookup"><span data-stu-id="f4594-140"><*language*> Language used to open a module.</span></span>                         |
| <span data-ttu-id="f4594-141">-l</span><span class="sxs-lookup"><span data-stu-id="f4594-141">-l</span></span>         | <span data-ttu-id="f4594-142"><arquivo de *log*> arquivo para usar como um log, acrescentar se ele já existir.</span><span class="sxs-lookup"><span data-stu-id="f4594-142"><*log file*> File to use as a log, append if it already exists.</span></span>      |
| <span data-ttu-id="f4594-143">-i</span><span class="sxs-lookup"><span data-stu-id="f4594-143">-i</span></span>         | <span data-ttu-id="f4594-144"><o *diretório*> extrair arquivos para a imagem de origem no diretório.</span><span class="sxs-lookup"><span data-stu-id="f4594-144"><*directory*> Extract files to the source image under the directory.</span></span> |
| <span data-ttu-id="f4594-145">-CAB</span><span class="sxs-lookup"><span data-stu-id="f4594-145">-cab</span></span>       | <span data-ttu-id="f4594-146"><*nome* de arquivo> extrair o gabinete msm para o arquivo.</span><span class="sxs-lookup"><span data-stu-id="f4594-146"><*filename*> Extract the MSM cabinet to file.</span></span>                        |
| <span data-ttu-id="f4594-147">-lfn</span><span class="sxs-lookup"><span data-stu-id="f4594-147">-lfn</span></span>       | <span data-ttu-id="f4594-148">Use nomes de arquivo longos durante a extração.</span><span class="sxs-lookup"><span data-stu-id="f4594-148">Use Long File Names during the extraction.</span></span>                                 |
| <span data-ttu-id="f4594-149">-configurar</span><span class="sxs-lookup"><span data-stu-id="f4594-149">-configure</span></span> | <span data-ttu-id="f4594-150"><o *nome* de arquivo> configurar o módulo usando dados de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="f4594-150"><*filename*> Configure the module using data from a file.</span></span>            |



 

## <a name="related-topics"></a><span data-ttu-id="f4594-151">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f4594-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4594-152">Ferramentas de desenvolvimento Windows Installer</span><span class="sxs-lookup"><span data-stu-id="f4594-152">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> <dt>

[<span data-ttu-id="f4594-153">Versões, ferramentas e redistribuíveis liberados</span><span class="sxs-lookup"><span data-stu-id="f4594-153">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



