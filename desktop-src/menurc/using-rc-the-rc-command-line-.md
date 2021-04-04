---
title: Usando o RC (a linha de comando do RC)
description: Para iniciar o RC, use o comando a seguir.
ms.assetid: da087e15-ecb5-4d03-b534-be872cf7d8b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c34e24fdf7b9b648a9baf9c6db8981f05d5434ef
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917231"
---
# <a name="using-rc-the-rc-command-line"></a><span data-ttu-id="b6dbf-103">Usando o RC (a linha de comando do RC)</span><span class="sxs-lookup"><span data-stu-id="b6dbf-103">Using RC (The RC Command Line)</span></span>

<span data-ttu-id="b6dbf-104">Para iniciar o RC, use o comando a seguir.</span><span class="sxs-lookup"><span data-stu-id="b6dbf-104">To start RC, use the following command.</span></span>

<span data-ttu-id="b6dbf-105">**RC** \[ *Opções* \] do *arquivo de script*</span><span class="sxs-lookup"><span data-stu-id="b6dbf-105">**RC** \[*options*\] *script-file*</span></span>

<span data-ttu-id="b6dbf-106">O parâmetro *script-File* especifica o nome do arquivo de definição de recurso que contém os nomes, os tipos, os nomes de arquivo e as descrições dos recursos a serem compilados.</span><span class="sxs-lookup"><span data-stu-id="b6dbf-106">The *script-file* parameter specifies the name of the resource-definition file that contains the names, types, filenames, and descriptions of the resources to be compiled.</span></span>

<span data-ttu-id="b6dbf-107">O RC pode gerar arquivos de recursos separados para aplicativos que têm recursos diferentes de idioma e idioma.</span><span class="sxs-lookup"><span data-stu-id="b6dbf-107">RC can generate separate resource files for applications that have both language-neutral and language-specific resources.</span></span> <span data-ttu-id="b6dbf-108">Os desenvolvedores podem usar um [arquivo de configuração de recurso](/windows/desktop/Intl/preparing-resources) ou definir opções de linha de comando para selecionar quais tipos de recursos e itens são recursos não localizáveis do arquivo de [idioma neutro (ln)](/windows/desktop/Intl/mui-resource-management) e quais são recursos localizáveis de arquivos MUI específicos do idioma.</span><span class="sxs-lookup"><span data-stu-id="b6dbf-108">Developers can use a [resource configuration file](/windows/desktop/Intl/preparing-resources) or set command-line options to select which resource types and items are non-localizable resources of the [language-neutral (LN) file](/windows/desktop/Intl/mui-resource-management) and which are localizable resources of language-specific MUI files.</span></span> <span data-ttu-id="b6dbf-109">Para obter mais informações, consulte a [interface do usuário multilíngüe](/windows/desktop/Intl/multilingual-user-interface).</span><span class="sxs-lookup"><span data-stu-id="b6dbf-109">For more information, see the [Multilingual User Interface](/windows/desktop/Intl/multilingual-user-interface).</span></span>

<span data-ttu-id="b6dbf-110">O parâmetro *Options* pode ser uma ou mais das opções de linha de comando a seguir.</span><span class="sxs-lookup"><span data-stu-id="b6dbf-110">The *options* parameter can be one or more of the following command-line options.</span></span>

## <a name="options"></a><span data-ttu-id="b6dbf-111">Opções</span><span class="sxs-lookup"><span data-stu-id="b6dbf-111">Options</span></span>

<dl> <dt>

<span data-ttu-id="b6dbf-112"><span id="__"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="b6dbf-112"><span id="__"></span>**/?**</span></span>
</dt> <dd>

<span data-ttu-id="b6dbf-113">Exibe uma lista de opções de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="b6dbf-113">Displays a list of command-line options.</span></span>

</dd> <dt>

<span data-ttu-id="b6dbf-114"><span id="_c"></span><span id="_C"></span>**/c**</span><span class="sxs-lookup"><span data-stu-id="b6dbf-114"><span id="_c"></span><span id="_C"></span>**/c**</span></span>
</dt> <dd>

<span data-ttu-id="b6dbf-115">Define uma página de código usada pela conversão NLS.</span><span class="sxs-lookup"><span data-stu-id="b6dbf-115">Defines a code page used by NLS conversion.</span></span>

</dd> <dt>

<span data-ttu-id="b6dbf-116"><span id="_d"></span><span id="_D"></span>**/d**</span><span class="sxs-lookup"><span data-stu-id="b6dbf-116"><span id="_d"></span><span id="_D"></span>**/d**</span></span>
</dt> <dd>

<span data-ttu-id="b6dbf-117">Define um símbolo para o pré-processador que você pode testar com a diretiva [**\# ifdef**](-ifdef.md) .</span><span class="sxs-lookup"><span data-stu-id="b6dbf-117">Defines a symbol for the preprocessor that you can test with the [**\#ifdef**](-ifdef.md) directive.</span></span>

</dd> <dt>

<span data-ttu-id="b6dbf-118"><span id="_fm_mresname"></span><span id="_FM_MRESNAME"></span>**/FM** *mresname*</span><span class="sxs-lookup"><span data-stu-id="b6dbf-118"><span id="_fm_mresname"></span><span id="_FM_MRESNAME"></span>**/fm** *mresname*</span></span>
</dt> <dd>

<span data-ttu-id="b6dbf-119">RC cria um idioma neutro. Arquivo RES e um MUI (dependente de idioma). Arquivo RES usando *script-File*.</span><span class="sxs-lookup"><span data-stu-id="b6dbf-119">RC creates one language-neutral .RES file and one language-dependent (MUI) .RES file using *script-file*.</span></span> <span data-ttu-id="b6dbf-120">Essa opção deve ser usada junto com a opção **/fo** *resname* .</span><span class="sxs-lookup"><span data-stu-id="b6dbf-120">This option must be used together with the **/fo** *resname* option.</span></span> <span data-ttu-id="b6dbf-121">O RC nomeia o idioma-neutro. Arquivo RES *resname. res* e nomeia o MUI (dependente do idioma). Arquivo RES *mresname. res*.</span><span class="sxs-lookup"><span data-stu-id="b6dbf-121">RC names the language-neutral .RES file *resname.res* and names the language-dependent (MUI) .RES file *mresname.res*.</span></span>

<span data-ttu-id="b6dbf-122">**Windows Server 2003 e Windows XP/2000:** Essa opção não está disponível sem usar também as funções [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) e [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) em um sistema atualizado.</span><span class="sxs-lookup"><span data-stu-id="b6dbf-122">**Windows Server 2003 and Windows XP/2000:** This option is not available without also using the [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) and [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) functions on an updated system.</span></span>

</dd> <dt>

<span data-ttu-id="b6dbf-123"><span id="_fo_resname"></span><span id="_FO_RESNAME"></span>**/fo** *resname*</span><span class="sxs-lookup"><span data-stu-id="b6dbf-123"><span id="_fo_resname"></span><span id="_FO_RESNAME"></span>**/fo** *resname*</span></span>
</dt> <dd>

<span data-ttu-id="b6dbf-124">RC cria um. Arquivo RES chamado *resname* usando *script-File*.</span><span class="sxs-lookup"><span data-stu-id="b6dbf-124">RC creates a .RES file named *resname* using *script-file*.</span></span>

<span data-ttu-id="b6dbf-125">Se a opção **/FM** *mresname* também for definida, RC criará um idioma neutro. Arquivo RES e um MUI (dependente de idioma). Arquivo RES.</span><span class="sxs-lookup"><span data-stu-id="b6dbf-125">If the **/fm** *mresname* option is also set, RC creates one language-neutral .RES file and one language-dependent (MUI) .RES file.</span></span>

<span data-ttu-id="b6dbf-126">**Windows Server 2003 e Windows XP/2000:** Essa opção não está disponível sem usar também as funções [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) e [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) em um sistema atualizado.</span><span class="sxs-lookup"><span data-stu-id="b6dbf-126">**Windows Server 2003 and Windows XP/2000:** This option is not available without also using the [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) and [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) functions on an updated system.</span></span>

</dd> <dt>

<span data-ttu-id="b6dbf-127"><span id="_g1"></span><span id="_G1"></span>**/G1**</span><span class="sxs-lookup"><span data-stu-id="b6dbf-127"><span id="_g1"></span><span id="_G1"></span>**/g1**</span></span>
</dt> <dd>

<span data-ttu-id="b6dbf-128">Se/G1, for definido, RC gerará um arquivo MUI se o único recurso localizável que está sendo incluído no arquivo MUI for um recurso de versão.</span><span class="sxs-lookup"><span data-stu-id="b6dbf-128">If /g1, is set, RC generates a MUI file if the only localizable resource being included in the MUI file is a version resource.</span></span> <span data-ttu-id="b6dbf-129">Se/G1 não for definido, o RC não gerará um arquivo MUI se o único recurso localizável que está sendo incluído no arquivo MUI for um recurso de versão.</span><span class="sxs-lookup"><span data-stu-id="b6dbf-129">If /g1 is not set, RC will not generate a MUI file if the only localizable resource being included in the MUI file is a version resource.</span></span>

</dd> <dt>

<span data-ttu-id="b6dbf-130"><span id="_h"></span><span id="_H"></span>**/h**</span><span class="sxs-lookup"><span data-stu-id="b6dbf-130"><span id="_h"></span><span id="_H"></span>**/h**</span></span>
</dt> <dd>

<span data-ttu-id="b6dbf-131">Exibe a lista de opções de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="b6dbf-131">Displays the list of command-line options.</span></span>

</dd> <dt>

<span data-ttu-id="b6dbf-132"><span id="_I"></span><span id="_i"></span>**/I**</span><span class="sxs-lookup"><span data-stu-id="b6dbf-132"><span id="_I"></span><span id="_i"></span>**/I**</span></span>
</dt> <dd>

<span data-ttu-id="b6dbf-133">Pesquisa o diretório especificado antes de Pesquisar os diretórios especificados pela variável de ambiente INCLUDE.</span><span class="sxs-lookup"><span data-stu-id="b6dbf-133">Searches the specified directory before searching the directories specified by the INCLUDE environment variable.</span></span>

</dd> <dt>

<span data-ttu-id="b6dbf-134"><span id="_j__loctype"></span><span id="_J__LOCTYPE"></span>**/j** *loctype*</span><span class="sxs-lookup"><span data-stu-id="b6dbf-134"><span id="_j__loctype"></span><span id="_J__LOCTYPE"></span>**/j** *loctype*</span></span>
</dt> <dd>

<span data-ttu-id="b6dbf-135">Os tipos de recursos localizáveis RC colocam no MUI (dependente do idioma). Arquivo RES.</span><span class="sxs-lookup"><span data-stu-id="b6dbf-135">Localizable resource types RC places into the language-dependent (MUI) .RES file.</span></span> <span data-ttu-id="b6dbf-136">Se a opção **/q** também for definida, essa opção será ignorada e as informações no arquivo de configuração RC prevalecerão.</span><span class="sxs-lookup"><span data-stu-id="b6dbf-136">If the **/q** option is also set, this option is ignored, and the information in the RC Configuration file takes precedence.</span></span>

<span data-ttu-id="b6dbf-137">**Windows Server 2003 e Windows XP/2000:** Essa opção não está disponível sem usar também as funções [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) e [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) em um sistema atualizado.</span><span class="sxs-lookup"><span data-stu-id="b6dbf-137">**Windows Server 2003 and Windows XP/2000:** This option is not available without also using the [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) and [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) functions on an updated system.</span></span>

</dd> <dt>

<span data-ttu-id="b6dbf-138"><span id="_k_overtype"></span><span id="_K_OVERTYPE"></span>**/k** *sobrescrever*</span><span class="sxs-lookup"><span data-stu-id="b6dbf-138"><span id="_k_overtype"></span><span id="_K_OVERTYPE"></span>**/k** *overtype*</span></span>
</dt> <dd>

<span data-ttu-id="b6dbf-139">Sobreposição de tipos de recursos que o RC coloca em ambos os idiomas neutros. RES e o MUI (dependente de idioma). Arquivos RES.</span><span class="sxs-lookup"><span data-stu-id="b6dbf-139">Overlapping resource types that RC places into both the language-neutral .RES and the language-dependent (MUI).RES files.</span></span> <span data-ttu-id="b6dbf-140">Os tipos de recurso que são especificados pela opção **/k** devem ser um subconjunto daqueles especificados pela opção **/j** .</span><span class="sxs-lookup"><span data-stu-id="b6dbf-140">The resource types that are specified by the **/k** option must be a subset of those that are specified by the **/j** option.</span></span> <span data-ttu-id="b6dbf-141">Por exemplo,? J2 ? J3 ? K3 especifica que o RC coloca o tipo de recurso 3 nos arquivos de idioma neutro e dependente de idioma (MUI).</span><span class="sxs-lookup"><span data-stu-id="b6dbf-141">For example, ?J2 ?J3 ?K3 specifies that RC places resource type 3 in both the language-neutral and language-dependent (MUI) files.</span></span> <span data-ttu-id="b6dbf-142">Se a opção **/q** também for definida, essa opção será ignorada e as informações no arquivo de configuração RC prevalecerão.</span><span class="sxs-lookup"><span data-stu-id="b6dbf-142">If the **/q** option is also set, this option is ignored, and the information in the RC Configuration file takes precedence.</span></span>

<span data-ttu-id="b6dbf-143">**Windows Server 2003 e Windows XP/2000:** Essa opção não está disponível sem usar também as funções [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) e [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) em um sistema atualizado.</span><span class="sxs-lookup"><span data-stu-id="b6dbf-143">**Windows Server 2003 and Windows XP/2000:** This option is not available without also using the [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) and [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) functions on an updated system.</span></span>

</dd> <dt>

<span data-ttu-id="b6dbf-144"><span id="_l_langid"></span><span id="_L_LANGID"></span>**/l** *LangID*</span><span class="sxs-lookup"><span data-stu-id="b6dbf-144"><span id="_l_langid"></span><span id="_L_LANGID"></span>**/l** *langid*</span></span>
</dt> <dd>

<span data-ttu-id="b6dbf-145">Especifica o idioma padrão para compilação.</span><span class="sxs-lookup"><span data-stu-id="b6dbf-145">Specifies the default language for compilation.</span></span> <span data-ttu-id="b6dbf-146">Por exemplo,-l409 é equivalente a incluir a seguinte instrução na parte superior do arquivo de script de recurso: `LANGUAGE LANG_ENGLISH,SUBLANG_ENGLISH_US`</span><span class="sxs-lookup"><span data-stu-id="b6dbf-146">For example, -l409 is equivalent to including the following statement at the top of the resource script file: `LANGUAGE LANG_ENGLISH,SUBLANG_ENGLISH_US`</span></span>

<span data-ttu-id="b6dbf-147">Para obter mais informações, consulte [identificadores de idioma](/windows/desktop/Intl/language-identifiers).</span><span class="sxs-lookup"><span data-stu-id="b6dbf-147">For more information, see [Language Identifiers](/windows/desktop/Intl/language-identifiers).</span></span>

</dd> <dt>

<span data-ttu-id="b6dbf-148"><span id="_n"></span><span id="_N"></span>**opção**</span><span class="sxs-lookup"><span data-stu-id="b6dbf-148"><span id="_n"></span><span id="_N"></span>**/n**</span></span>
</dt> <dd>

<span data-ttu-id="b6dbf-149">NULL encerra todas as cadeias de caracteres na tabela de cadeias.</span><span class="sxs-lookup"><span data-stu-id="b6dbf-149">Null terminates all strings in the string table.</span></span>

</dd> <dt>

<span data-ttu-id="b6dbf-150"><span id="_q_Mui.RCConfig"></span><span id="_q_mui.rcconfig"></span><span id="_Q_MUI.RCCONFIG"></span>**/Q** *mui. RCConfig*</span><span class="sxs-lookup"><span data-stu-id="b6dbf-150"><span id="_q_Mui.RCConfig"></span><span id="_q_mui.rcconfig"></span><span id="_Q_MUI.RCCONFIG"></span>**/q** *Mui.RCConfig*</span></span>
</dt> <dd>

<span data-ttu-id="b6dbf-151">Um arquivo de configuração RC que segue o formato de arquivo de configuração RC.</span><span class="sxs-lookup"><span data-stu-id="b6dbf-151">An RC configuration file that follows the RC Configuration File format.</span></span> <span data-ttu-id="b6dbf-152">O formato de arquivo de configuração RC permite que os componentes descrevam automaticamente as informações de recursos, como controle de versão de recursos, caminho do arquivo MUI, tipos de recursos e itens.</span><span class="sxs-lookup"><span data-stu-id="b6dbf-152">The RC Configuration File format enables components to self-describe resource information such as resource versioning, MUI file path, resource types and items.</span></span> <span data-ttu-id="b6dbf-153">Esse arquivo especifica quais recursos vão para o idioma neutro. Arquivo RES e quais recursos vão para o MUI (dependente de idioma). Arquivo RES.</span><span class="sxs-lookup"><span data-stu-id="b6dbf-153">This file specifies which resources go into the language-neutral .RES file and which resources go into the language-dependent (MUI) .RES file.</span></span> <span data-ttu-id="b6dbf-154">Essa opção e as informações fornecidas no arquivo de configuração RC substituem as opções de linha de comando **/j** e **/k**.</span><span class="sxs-lookup"><span data-stu-id="b6dbf-154">This option, and the information provided in the RC Configuration file, override the command line options **/j** and **/k**.</span></span>

<span data-ttu-id="b6dbf-155">**Windows Server 2003 e Windows XP/2000:** Essa opção não está disponível sem usar também as funções [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) e [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) em um sistema atualizado.</span><span class="sxs-lookup"><span data-stu-id="b6dbf-155">**Windows Server 2003 and Windows XP/2000:** This option is not available without also using the [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) and [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) functions on an updated system.</span></span>

</dd> <dt>

<span data-ttu-id="b6dbf-156"><span id="_r"></span><span id="_R"></span>**/r**</span><span class="sxs-lookup"><span data-stu-id="b6dbf-156"><span id="_r"></span><span id="_R"></span>**/r**</span></span>
</dt> <dd>

<span data-ttu-id="b6dbf-157">Ignorado.</span><span class="sxs-lookup"><span data-stu-id="b6dbf-157">Ignored.</span></span> <span data-ttu-id="b6dbf-158">Fornecido para compatibilidade com os makefiles existentes.</span><span class="sxs-lookup"><span data-stu-id="b6dbf-158">Provided for compatibility with existing makefiles.</span></span>

</dd> <dt>

<span data-ttu-id="b6dbf-159"><span id="_u"></span><span id="_U"></span>**/u**</span><span class="sxs-lookup"><span data-stu-id="b6dbf-159"><span id="_u"></span><span id="_U"></span>**/u**</span></span>
</dt> <dd>

<span data-ttu-id="b6dbf-160">Desdefine um símbolo para o pré-processador.</span><span class="sxs-lookup"><span data-stu-id="b6dbf-160">Undefines a symbol for the preprocessor.</span></span>

</dd> <dt>

<span data-ttu-id="b6dbf-161"><span id="_v"></span><span id="_V"></span>**/v**</span><span class="sxs-lookup"><span data-stu-id="b6dbf-161"><span id="_v"></span><span id="_V"></span>**/v**</span></span>
</dt> <dd>

<span data-ttu-id="b6dbf-162">Exibe mensagens que relatam o progresso do compilador.</span><span class="sxs-lookup"><span data-stu-id="b6dbf-162">Displays messages that report on the progress of the compiler.</span></span>

</dd> <dt>

<span data-ttu-id="b6dbf-163"><span id="_x"></span><span id="_X"></span>**/x**</span><span class="sxs-lookup"><span data-stu-id="b6dbf-163"><span id="_x"></span><span id="_X"></span>**/x**</span></span>
</dt> <dd>

<span data-ttu-id="b6dbf-164">Impede que o RC Verifique a variável de ambiente INCLUDE ao procurar arquivos de cabeçalho ou arquivos de recursos.</span><span class="sxs-lookup"><span data-stu-id="b6dbf-164">Prevents RC from checking the INCLUDE environment variable when searching for header files or resource files.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b6dbf-165">Comentários</span><span class="sxs-lookup"><span data-stu-id="b6dbf-165">Remarks</span></span>

<span data-ttu-id="b6dbf-166">As opções não diferenciam maiúsculas de minúsculas e um hífen (-) pode ser usado no lugar de uma barra (/).</span><span class="sxs-lookup"><span data-stu-id="b6dbf-166">Options are not case sensitive, and a hyphen (-) can be used in place of a slash mark (/).</span></span> <span data-ttu-id="b6dbf-167">Você pode combinar opções de letra única se elas não exigirem parâmetros adicionais.</span><span class="sxs-lookup"><span data-stu-id="b6dbf-167">You can combine single-letter options if they do not require any additional parameters.</span></span>

<span data-ttu-id="b6dbf-168">O RC não gerará um arquivo MUI nos casos a seguir.</span><span class="sxs-lookup"><span data-stu-id="b6dbf-168">RC will not generate a MUI file in the following cases.</span></span>

-   <span data-ttu-id="b6dbf-169">Não existem recursos localizáveis no arquivo. rc.</span><span class="sxs-lookup"><span data-stu-id="b6dbf-169">No localizable resources exist in the .rc file.</span></span>
-   <span data-ttu-id="b6dbf-170">A única ID de idioma do recurso especificada no arquivo. rc é neutra (0x0).</span><span class="sxs-lookup"><span data-stu-id="b6dbf-170">The only resource language id specified in the .rc file is neutral (0x0).</span></span>
-   <span data-ttu-id="b6dbf-171">O arquivo. RC tem recursos que são especificados em mais de um idioma.</span><span class="sxs-lookup"><span data-stu-id="b6dbf-171">The .rc file has resources that are specified in more than one language.</span></span> <span data-ttu-id="b6dbf-172">A exceção é que se o arquivo. rc contiver dois idiomas, e um idioma for neutro (0x0), o RC gerará um arquivo MUI.</span><span class="sxs-lookup"><span data-stu-id="b6dbf-172">The exception is if the .rc file contains two languages, and one language is neutral (0x0), RC generates a MUI file.</span></span>

<span data-ttu-id="b6dbf-173">Para mais informações, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="b6dbf-173">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="b6dbf-174">Definindo nomes para o pré-processador</span><span class="sxs-lookup"><span data-stu-id="b6dbf-174">Defining Names for the Preprocessor</span></span>](defining-names-for-the-preprocessor.md)
-   [<span data-ttu-id="b6dbf-175">Renomeando o arquivo de recurso compilado</span><span class="sxs-lookup"><span data-stu-id="b6dbf-175">Renaming the Compiled Resource File</span></span>](renaming-the-compiled-resource-file.md)
-   [<span data-ttu-id="b6dbf-176">Procurando arquivos</span><span class="sxs-lookup"><span data-stu-id="b6dbf-176">Searching for Files</span></span>](searching-for-files.md)
-   [<span data-ttu-id="b6dbf-177">Exibindo mensagens de progresso</span><span class="sxs-lookup"><span data-stu-id="b6dbf-177">Displaying Progress Messages</span></span>](displaying-progress-messages.md)
-   [<span data-ttu-id="b6dbf-178">Mensagens de diagnóstico RC</span><span class="sxs-lookup"><span data-stu-id="b6dbf-178">RC Diagnostic Messages</span></span>](rc-diagnostic-messages.md)

## <a name="related-topics"></a><span data-ttu-id="b6dbf-179">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b6dbf-179">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6dbf-180">Interface do Usuário Multilíngue</span><span class="sxs-lookup"><span data-stu-id="b6dbf-180">Multilingual User Interface</span></span>](/windows/desktop/Intl/multilingual-user-interface)
</dt> </dl>

 

 