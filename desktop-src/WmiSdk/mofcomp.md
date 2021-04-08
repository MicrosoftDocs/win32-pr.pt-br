---
description: O compilador formato MOF (MOF) analisa um arquivo que contém instruções MOF e adiciona as classes e instâncias de classe definidas no arquivo ao repositório do WMI.
ms.assetid: 9858da09-fb91-43a4-9817-83b10e2ee08f
ms.tgt_platform: multiple
title: Mofcomp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da63525e4bb8a32f3628b68295e5cc8ade0b08de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827492"
---
# <a name="mofcomp"></a><span data-ttu-id="31fce-103">Mofcomp</span><span class="sxs-lookup"><span data-stu-id="31fce-103">mofcomp</span></span>

<span data-ttu-id="31fce-104">O compilador [*formato MOF (MOF)*](gloss-m.md) analisa um arquivo que contém instruções MOF e adiciona as classes e instâncias de classe definidas no arquivo ao repositório do WMI.</span><span class="sxs-lookup"><span data-stu-id="31fce-104">The [*Managed Object Format (MOF)*](gloss-m.md) compiler parses a file containing MOF statements and adds the classes and class instances defined in the file to the WMI repository.</span></span> <span data-ttu-id="31fce-105">Os arquivos MOF geralmente são compilados automaticamente durante a instalação dos sistemas com os quais eles são fornecidos, mas você também pode compilar arquivos MOF usando essa ferramenta.</span><span class="sxs-lookup"><span data-stu-id="31fce-105">MOF files are usually automatically compiled during the installation of the systems with which they are provided, but you can also compile MOF files by using this tool.</span></span>

<span data-ttu-id="31fce-106">Para obter mais informações sobre como localizar e usar mofcomp.exe, consulte [usando as ferramentas de gerenciamento do WMI](/previous-versions/system-center/configuration-manager-2003/cc180468(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="31fce-106">For more information about locating and using mofcomp.exe, see [Using WMI Management Tools](/previous-versions/system-center/configuration-manager-2003/cc180468(v=technet.10)).</span></span> <span data-ttu-id="31fce-107">Para obter informações sobre como remover classes e instâncias do repositório do WMI, consulte o comando de pré-processador do [**pragma DeleteClass**](pragma-deleteclass.md) .</span><span class="sxs-lookup"><span data-stu-id="31fce-107">For information about removing classes and instances from the WMI repository, see the [**pragma deleteclass**](pragma-deleteclass.md) preprocessor command.</span></span>

<span data-ttu-id="31fce-108">O exemplo de código a seguir mostra como executar o compilador MOF em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="31fce-108">The following code example shows how to run the MOF compiler on a file.</span></span>

``` syntax
mofcomp
  [-autorecover]
  [-check]
  [-N:<namespacepath>]
  [-class:createonly | -class:forceupdate | 
   -class:safeupdate | -class:updateonly ] 
  [-instance:updateonly | -instance:createonly]
  [-B:<filename>]
  [-WMI]
  [-P:<Password>]
  [-U:<UserName>]
  [-A:<Authority>]
  [-MOF:<path>] 
  [-MFL:<path>] 
  [-AMENDMENT:<Locale>]
  [-ER:<ResourceName>]
  [-L:<ResourceLocale>] 
  <MOFfile>
```

## <a name="switches"></a><span data-ttu-id="31fce-109">Comutadores</span><span class="sxs-lookup"><span data-stu-id="31fce-109">Switches</span></span>

<dl> <dt>

<span data-ttu-id="31fce-110"><span id="-autorecover"></span><span id="-AUTORECOVER"></span>**-recuperação automática**</span><span class="sxs-lookup"><span data-stu-id="31fce-110"><span id="-autorecover"></span><span id="-AUTORECOVER"></span>**-autorecover**</span></span>
</dt> <dd>

<span data-ttu-id="31fce-111">Adiciona o arquivo MOF nomeado à lista de arquivos compilados durante a recuperação do repositório.</span><span class="sxs-lookup"><span data-stu-id="31fce-111">Adds the named MOF file to the list of files compiled during repository recovery.</span></span> <span data-ttu-id="31fce-112">A lista de arquivos MOF de recuperação automática é armazenada na chave do registro:</span><span class="sxs-lookup"><span data-stu-id="31fce-112">The list of autorecover MOF files is stored in the registry key:</span></span>

<span data-ttu-id="31fce-113">**HKEY \_ SOFTWARE do \_ computador local** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM \\**</span><span class="sxs-lookup"><span data-stu-id="31fce-113">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM\\**</span></span>

<span data-ttu-id="31fce-114">Os arquivos MOF listados nesta entrada de registro devem residir no computador local porque os arquivos MOF que usam o comando de **recuperação automática** não podem recuperar arquivos MOF localizados em um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="31fce-114">The MOF files listed in this registry entry must reside on the local computer because MOF files that use the **autorecover** command cannot recover MOF files located on a remote computer.</span></span>

> [!Note]  
> <span data-ttu-id="31fce-115">Para garantir que todas as definições de classe WMI para objetos gerenciados sejam restauradas no [*repositório WMI*](gloss-w.md) se o WMI tiver uma falha e reiniciar, use a instrução de pré-processador de [**\# AutoRecuperação pragma**](pragma-autorecover.md) em seu arquivo [*formato MOF*](gloss-m.md) (MOF).</span><span class="sxs-lookup"><span data-stu-id="31fce-115">To ensure that all your WMI class definitions for managed objects are restored to the [*WMI repository*](gloss-w.md) if WMI has a failure and restarts, use the [**\#pragma autorecover**](pragma-autorecover.md) preprocessor instruction in your [*Managed Object Format*](gloss-m.md) (MOF) file.</span></span>

 

</dd> <dt>

<span data-ttu-id="31fce-116"><span id="-check"></span><span id="-CHECK"></span>**-verificar**</span><span class="sxs-lookup"><span data-stu-id="31fce-116"><span id="-check"></span><span id="-CHECK"></span>**-check**</span></span>
</dt> <dd>

<span data-ttu-id="31fce-117">Solicita que o compilador execute apenas uma verificação de sintaxe e imprima as mensagens de erro apropriadas.</span><span class="sxs-lookup"><span data-stu-id="31fce-117">Requests that the compiler perform a syntax check only and print appropriate error messages.</span></span> <span data-ttu-id="31fce-118">Nenhuma outra opção pode ser usada com essa opção.</span><span class="sxs-lookup"><span data-stu-id="31fce-118">No other switch can be used with this switch.</span></span> <span data-ttu-id="31fce-119">Quando essa opção é usada, nenhuma conexão com Instrumentação de Gerenciamento do Windows (WMI) é estabelecida e nenhuma modificação no repositório do WMI é feita.</span><span class="sxs-lookup"><span data-stu-id="31fce-119">When this switch is used, no connection to Windows Management Instrumentation (WMI) is established and no modifications to the WMI repository are made.</span></span>

</dd> <dt>

<span data-ttu-id="31fce-120"><span id="-N__namespacepath_"></span><span id="-n__namespacepath_"></span><span id="-N__NAMESPACEPATH_"></span>**-N: <** _NamespacePath_*_>_*</span><span class="sxs-lookup"><span data-stu-id="31fce-120"><span id="-N__namespacepath_"></span><span id="-n__namespacepath_"></span><span id="-N__NAMESPACEPATH_"></span>**-N:<**_namespacepath_*_>_*</span></span>
</dt> <dd><span data-ttu-id="31fce-121">Solicita que o compilador carregue o arquivo MOF no namespace especificado como *NamespacePath*.</span><span class="sxs-lookup"><span data-stu-id="31fce-121">Requests that the compiler load the MOF file into the namespace specified as *namespacepath*.</span></span> <span data-ttu-id="31fce-122">O MOF compilado é carregado no namespace Mofcomp padrão, o \\ padrão raiz, a menos que essa opção seja usada.</span><span class="sxs-lookup"><span data-stu-id="31fce-122">The compiled MOF is loaded into the default Mofcomp namespace, root\\default, unless this switch is used.</span></span> <span data-ttu-id="31fce-123">Você também pode inserir o namespace pragma do comando de pré-processador **\# ("**_caminho do namespace_*_")_* no arquivo MOF para obter o mesmo efeito.</span><span class="sxs-lookup"><span data-stu-id="31fce-123">You can also insert the preprocessor command **\#pragma namespace ("**_namespace path_*_")_* in the MOF file to achieve the same effect.</span></span> <span data-ttu-id="31fce-124">Se os comandos **-N:** switch e o \# <a href="pragma-namespace.md">namespace pragma</a> forem usados, o \# **namespace de pragma** **Recover** terá prioridade.</span><span class="sxs-lookup"><span data-stu-id="31fce-124">If both the **-N:** switch and the \#<a href="pragma-namespace.md">pragma namespace</a> command are used, \#**pragma namespace** **autorecover** takes priority.</span></span> <span data-ttu-id="31fce-125">Nesse caso, a única maneira de compilar o MOF em outro namespace é editar o arquivo MOF e alterar o comando de \# **namespace de pragma** .</span><span class="sxs-lookup"><span data-stu-id="31fce-125">In this case, the only way to compile the MOF into another namespace is to edit the MOF file and change the \#**pragma namespace** command.</span></span> <span data-ttu-id="31fce-126">Um computador remoto pode ser especificado usando o \\ \\ \\ padrão raiz MachineName \\ .</span><span class="sxs-lookup"><span data-stu-id="31fce-126">A remote computer can be specified using \\\\machinename\\root\\default.</span></span></dd> <dt>

<span data-ttu-id="31fce-127"><span id="-class_createonly"></span><span id="-CLASS_CREATEONLY"></span>**-Class: somente**</span><span class="sxs-lookup"><span data-stu-id="31fce-127"><span id="-class_createonly"></span><span id="-CLASS_CREATEONLY"></span>**-class:createonly**</span></span>
</dt> <dd>

<span data-ttu-id="31fce-128">Solicita que o compilador não faça nenhuma alteração nas classes existentes.</span><span class="sxs-lookup"><span data-stu-id="31fce-128">Requests that the compiler not make any changes to existing classes.</span></span> <span data-ttu-id="31fce-129">Quando essa opção for usada, a operação de compilação será encerrada se uma classe especificada no arquivo MOF já existir.</span><span class="sxs-lookup"><span data-stu-id="31fce-129">When this switch is used, the compile operation terminates if a class specified in the MOF file already exists.</span></span>

</dd> <dt>

<span data-ttu-id="31fce-130"><span id="-class_forceupdate"></span><span id="-CLASS_FORCEUPDATE"></span>**-classe: forceupdate**</span><span class="sxs-lookup"><span data-stu-id="31fce-130"><span id="-class_forceupdate"></span><span id="-CLASS_FORCEUPDATE"></span>**-class:forceupdate**</span></span>
</dt> <dd>

<span data-ttu-id="31fce-131">Força atualizações de classes quando existem classes filhas conflitantes.</span><span class="sxs-lookup"><span data-stu-id="31fce-131">Forces updates of classes when conflicting child classes exist.</span></span> <span data-ttu-id="31fce-132">Por exemplo, suponha que um qualificador de classe seja definido em uma classe filho e a classe base tente adicionar o mesmo qualificador.</span><span class="sxs-lookup"><span data-stu-id="31fce-132">For example, suppose a class qualifier is defined in a child class and the base class tries to add the same qualifier.</span></span> <span data-ttu-id="31fce-133">Na **classe: modo forceupdate** , o compilador MOF resolve esse conflito excluindo o qualificador conflitante na classe filho.</span><span class="sxs-lookup"><span data-stu-id="31fce-133">In **-class:forceupdate** mode, the MOF compiler resolves this conflict by deleting the conflicting qualifier in the child class.</span></span> <span data-ttu-id="31fce-134">Se a classe filho tiver instâncias, a atualização forçada falhará.</span><span class="sxs-lookup"><span data-stu-id="31fce-134">If the child class has instances, the forced update fails.</span></span>

</dd> <dt>

<span data-ttu-id="31fce-135"><span id="-class_safeupdate"></span><span id="-CLASS_SAFEUPDATE"></span>**-classe: safeupdate**</span><span class="sxs-lookup"><span data-stu-id="31fce-135"><span id="-class_safeupdate"></span><span id="-CLASS_SAFEUPDATE"></span>**-class:safeupdate**</span></span>
</dt> <dd>

<span data-ttu-id="31fce-136">Permite atualizações de classes, mesmo se houver classes filhas, desde que a alteração não cause conflitos com classes filhas.</span><span class="sxs-lookup"><span data-stu-id="31fce-136">Allows updates of classes even if there are child classes, as long as the change does not cause conflicts with child classes.</span></span> <span data-ttu-id="31fce-137">Por exemplo, esse sinalizador permite adicionar uma nova propriedade à classe base que não foi mencionada anteriormente em classes filhas.</span><span class="sxs-lookup"><span data-stu-id="31fce-137">For example, this flag allows adding a new property to the base class that was not previously mentioned in child classes.</span></span> <span data-ttu-id="31fce-138">Se as classes filhas tiverem instâncias, a atualização falhará.</span><span class="sxs-lookup"><span data-stu-id="31fce-138">If the child classes have instances, the update fails.</span></span>

</dd> <dt>

<span data-ttu-id="31fce-139"><span id="-class_updateonly"></span><span id="-CLASS_UPDATEONLY"></span>**-classe: UpdateOnly**</span><span class="sxs-lookup"><span data-stu-id="31fce-139"><span id="-class_updateonly"></span><span id="-CLASS_UPDATEONLY"></span>**-class:updateonly**</span></span>
</dt> <dd>

<span data-ttu-id="31fce-140">Solicita que o compilador não crie nenhuma classe nova.</span><span class="sxs-lookup"><span data-stu-id="31fce-140">Requests that the compiler not create any new classes.</span></span> <span data-ttu-id="31fce-141">Quando essa opção for usada, a operação de compilação será encerrada se uma classe especificada no arquivo MOF não existir.</span><span class="sxs-lookup"><span data-stu-id="31fce-141">When this switch is used, the compile operation terminates if a class specified in the MOF file does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="31fce-142"><span id="-instance_updateonly"></span><span id="-INSTANCE_UPDATEONLY"></span>**-instância: UpdateOnly**</span><span class="sxs-lookup"><span data-stu-id="31fce-142"><span id="-instance_updateonly"></span><span id="-INSTANCE_UPDATEONLY"></span>**-instance:updateonly**</span></span>
</dt> <dd>

<span data-ttu-id="31fce-143">Solicita que o compilador não crie nenhuma nova instância.</span><span class="sxs-lookup"><span data-stu-id="31fce-143">Requests that the compiler not create any new instances.</span></span> <span data-ttu-id="31fce-144">Quando essa opção for usada, a operação de compilação será encerrada se uma instância especificada no arquivo MOF não existir.</span><span class="sxs-lookup"><span data-stu-id="31fce-144">When this switch is used, the compile operation terminates if an instance specified in the MOF file does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="31fce-145"><span id="-instance_createonly"></span><span id="-INSTANCE_CREATEONLY"></span>**-instância: somente**</span><span class="sxs-lookup"><span data-stu-id="31fce-145"><span id="-instance_createonly"></span><span id="-INSTANCE_CREATEONLY"></span>**-instance:createonly**</span></span>
</dt> <dd>

<span data-ttu-id="31fce-146">Solicita que o compilador não faça nenhuma alteração nas instâncias existentes.</span><span class="sxs-lookup"><span data-stu-id="31fce-146">Requests that the compiler not make any changes to existing instances.</span></span> <span data-ttu-id="31fce-147">Quando essa opção for usada, a operação de compilação será encerrada se uma instância especificada no arquivo MOF já existir.</span><span class="sxs-lookup"><span data-stu-id="31fce-147">When this switch is used, the compile operation terminates if an instance specified in the MOF file already exists.</span></span>

</dd> <dt>

<span data-ttu-id="31fce-148"><span id="-B__filename_"></span><span id="-b__filename_"></span><span id="-B__FILENAME_"></span>**-B: <** _nome do arquivo_*_>_*</span><span class="sxs-lookup"><span data-stu-id="31fce-148"><span id="-B__filename_"></span><span id="-b__filename_"></span><span id="-B__FILENAME_"></span>**-B:<**_filename_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="31fce-149">Solicita que o compilador crie uma versão binária do arquivo MOF com o nome *nome* de arquivo sem fazer nenhuma modificação no repositório WMI.</span><span class="sxs-lookup"><span data-stu-id="31fce-149">Requests that the compiler create a binary version of the MOF file with the name *filename* without making any modifications to the WMI repository.</span></span>

<span data-ttu-id="31fce-150">Se você usar a opção **-B: <** _filename_ *_>_* para criar um arquivo MOF binário, somente os tipos de qualificador padrão serão armazenados no repositório WMI.</span><span class="sxs-lookup"><span data-stu-id="31fce-150">If you use the **-B:<**_filename_*_>_* option to create a binary MOF file, only default qualifier flavors are stored in the WMI repository.</span></span>

<span data-ttu-id="31fce-151">O formato binário MOF é o formato intermediário para combinar um driver WDM com o MOF como um recurso.</span><span class="sxs-lookup"><span data-stu-id="31fce-151">Binary MOF format is the intermediate format for combining a WDM-driver with the MOF as a resource.</span></span> <span data-ttu-id="31fce-152">O MOF binário representa classes e instâncias da mesma forma que um arquivo MOF de texto e é compactado antes de ser armazenado em disco.</span><span class="sxs-lookup"><span data-stu-id="31fce-152">The binary MOF represents classes and instances just as a text MOF file does and is compressed before it is stored on disk.</span></span>

</dd> <dt>

<span data-ttu-id="31fce-153"><span id="-WMI"></span><span id="-wmi"></span>**-WMI**</span><span class="sxs-lookup"><span data-stu-id="31fce-153"><span id="-WMI"></span><span id="-wmi"></span>**-WMI**</span></span>
</dt> <dd>

<span data-ttu-id="31fce-154">Solicita que o compilador execute uma verificação de sintaxe do WMI.</span><span class="sxs-lookup"><span data-stu-id="31fce-154">Requests that the compiler perform a WMI syntax check.</span></span> <span data-ttu-id="31fce-155">A opção **-B:** deve ser usada com essa opção.</span><span class="sxs-lookup"><span data-stu-id="31fce-155">The **-B:** switch must be used with this switch.</span></span> <span data-ttu-id="31fce-156">A opção **-WMI** é usada somente para criar arquivos MOF binários para uso por drivers de dispositivo WDM.</span><span class="sxs-lookup"><span data-stu-id="31fce-156">The **-WMI** switch is only used for building binary MOF files for use by WDM device drivers.</span></span> <span data-ttu-id="31fce-157">Essa opção invoca um verificador de arquivo MOF binário separado, que é executado depois que o arquivo MOF binário é criado.</span><span class="sxs-lookup"><span data-stu-id="31fce-157">This switch invokes a separate binary MOF file checker, which runs after the binary MOF file is created.</span></span>

</dd> <dt>

<span data-ttu-id="31fce-158"><span id="-P__Password_"></span><span id="-p__password_"></span><span id="-P__PASSWORD_"></span>**-P: <** _senha_*_>_*</span><span class="sxs-lookup"><span data-stu-id="31fce-158"><span id="-P__Password_"></span><span id="-p__password_"></span><span id="-P__PASSWORD_"></span>**-P:<**_Password_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="31fce-159">Especifica a *senha* como a senha do usuário do computador a ser inserida ao fazer logon.</span><span class="sxs-lookup"><span data-stu-id="31fce-159">Specifies *Password* as the password for the computer user to enter when logging on.</span></span>

</dd> <dt>

<span data-ttu-id="31fce-160"><span id="-U__UserName_"></span><span id="-u__username_"></span><span id="-U__USERNAME_"></span>**-U: <** _nome de usuário_*_>_*</span><span class="sxs-lookup"><span data-stu-id="31fce-160"><span id="-U__UserName_"></span><span id="-u__username_"></span><span id="-U__USERNAME_"></span>**-U:<**_UserName_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="31fce-161">Especifica *username* como o nome do usuário que está fazendo logon.</span><span class="sxs-lookup"><span data-stu-id="31fce-161">Specifies *UserName* as the name of the user logging on.</span></span>

</dd> <dt>

<span data-ttu-id="31fce-162"><span id="-A__Authority_"></span><span id="-a__authority_"></span><span id="-A__AUTHORITY_"></span>**-A: autoridade de <** *_>_*</span><span class="sxs-lookup"><span data-stu-id="31fce-162"><span id="-A__Authority_"></span><span id="-a__authority_"></span><span id="-A__AUTHORITY_"></span>**-A:<**_Authority_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="31fce-163">Especifica a *autoridade* como a autoridade (nome de domínio) a ser usada ao fazer logon no WMI.</span><span class="sxs-lookup"><span data-stu-id="31fce-163">Specifies *Authority* as the authority (domain name) to use when logging on to WMI.</span></span>

</dd> <dt>

<span data-ttu-id="31fce-164"><span id="-MOF__path_"></span><span id="-mof__path_"></span><span id="-MOF__PATH_"></span>**-MOF: caminho de <** *_>_*</span><span class="sxs-lookup"><span data-stu-id="31fce-164"><span id="-MOF__path_"></span><span id="-mof__path_"></span><span id="-MOF__PATH_"></span>**-MOF:<**_path_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="31fce-165">Nome da saída de idioma neutro.</span><span class="sxs-lookup"><span data-stu-id="31fce-165">Name of the language neutral output.</span></span> <span data-ttu-id="31fce-166">Usado com a opção **-aditamento** para especificar o nome do arquivo MOF com neutralidade de idioma que será gerado.</span><span class="sxs-lookup"><span data-stu-id="31fce-166">Used with the **-AMENDMENT** switch to specify the name of the language-neutral MOF file that will be generated.</span></span>

</dd> <dt>

<span data-ttu-id="31fce-167"><span id="-MFL__path_"></span><span id="-mfl__path_"></span><span id="-MFL__PATH_"></span>**-MFL: caminho de <** *_>_*</span><span class="sxs-lookup"><span data-stu-id="31fce-167"><span id="-MFL__path_"></span><span id="-mfl__path_"></span><span id="-MFL__PATH_"></span>**-MFL:<**_path_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="31fce-168">Nome da saída específica do idioma.</span><span class="sxs-lookup"><span data-stu-id="31fce-168">Name of the language specific output.</span></span> <span data-ttu-id="31fce-169">Usado com a opção **-aditamento** para especificar o nome do arquivo MOF específico do idioma que será gerado.</span><span class="sxs-lookup"><span data-stu-id="31fce-169">Used with the **-AMENDMENT** switch to specify the name of the language-specific MOF file that will be generated.</span></span>

</dd> <dt>

<span data-ttu-id="31fce-170"><span id="-AMENDMENT__Locale_"></span><span id="-amendment__locale_"></span><span id="-AMENDMENT__LOCALE_"></span>**-Emenda: <** _localidade_*_>_*</span><span class="sxs-lookup"><span data-stu-id="31fce-170"><span id="-AMENDMENT__Locale_"></span><span id="-amendment__locale_"></span><span id="-AMENDMENT__LOCALE_"></span>**-AMENDMENT:<**_Locale_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="31fce-171">Divide o arquivo MOF em versões específicas de idioma e neutras.</span><span class="sxs-lookup"><span data-stu-id="31fce-171">Splits the MOF file into language-neutral and -specific versions.</span></span> <span data-ttu-id="31fce-172">O compilador MOF cria uma forma neutra de idioma do arquivo MOF que tem todos os qualificadores corrigidos removidos.</span><span class="sxs-lookup"><span data-stu-id="31fce-172">The MOF compiler creates a language-neutral form of the MOF file that has all amended qualifiers removed.</span></span> <span data-ttu-id="31fce-173">Uma versão localizada do arquivo MOF também é criada com uma extensão de nome de arquivo MFL.</span><span class="sxs-lookup"><span data-stu-id="31fce-173">A localized version of the MOF file is also created with an MFL file name extension.</span></span> <span data-ttu-id="31fce-174">O parâmetro *locale* especifica o nome do namespace filho que contém as definições de classe localizadas.</span><span class="sxs-lookup"><span data-stu-id="31fce-174">The *Locale* parameter specifies the name of the child namespace that contains the localized class definitions.</span></span> <span data-ttu-id="31fce-175">O formato do parâmetro *locale* é MS \_ xxx, em que xxx é o valor hexadecimal do LCID do Windows.</span><span class="sxs-lookup"><span data-stu-id="31fce-175">The format of the *Locale* parameter is MS\_xxx where xxx is the hexadecimal value of the Windows LCID.</span></span> <span data-ttu-id="31fce-176">Por exemplo, a localidade para inglês americano é MS \_ 409.</span><span class="sxs-lookup"><span data-stu-id="31fce-176">For example, the locale for American English is MS\_409.</span></span>

</dd> <dt>

<span data-ttu-id="31fce-177"><span id="-ER__ResourceName_"></span><span id="-er__resourcename_"></span><span id="-ER__RESOURCENAME_"></span>**-ER <** _resourceName_*_>_*</span><span class="sxs-lookup"><span data-stu-id="31fce-177"><span id="-ER__ResourceName_"></span><span id="-er__resourcename_"></span><span id="-ER__RESOURCENAME_"></span>**-ER <**_ResourceName_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="31fce-178">Extrai o MOF binário de um recurso nomeado.</span><span class="sxs-lookup"><span data-stu-id="31fce-178">Extracts binary MOF from a named resource.</span></span> <span data-ttu-id="31fce-179">Essa opção Obtém o MOF binário da classe no repositório WMI, enquanto a opção-B cria o formato binário MOF a partir de um arquivo MOF.</span><span class="sxs-lookup"><span data-stu-id="31fce-179">This switch gets the binary MOF from the class in the WMI repository while the -B switch creates the binary MOF format from a MOF file.</span></span>

</dd> <dt>

<span data-ttu-id="31fce-180"><span id="-L__ResourceLocale_"></span><span id="-l__resourcelocale_"></span><span id="-L__RESOURCELOCALE_"></span>**-L: <** _ResourceLocale_*_>_*</span><span class="sxs-lookup"><span data-stu-id="31fce-180"><span id="-L__ResourceLocale_"></span><span id="-l__resourcelocale_"></span><span id="-L__RESOURCELOCALE_"></span>**-L:<**_ResourceLocale_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="31fce-181">Opcional.</span><span class="sxs-lookup"><span data-stu-id="31fce-181">Optional.</span></span> <span data-ttu-id="31fce-182">Extrai as descrições do MOF localizadas do MOF binário quando usadas com a opção-ER.</span><span class="sxs-lookup"><span data-stu-id="31fce-182">Extracts the localized MOF descriptions from the binary MOF when used with -ER switch.</span></span>

</dd> <dt>

<span data-ttu-id="31fce-183"><span id="_MOFfile_"></span><span id="_moffile_"></span><span id="_MOFFILE_"></span>**<**_MOFfile_*_>_*</span><span class="sxs-lookup"><span data-stu-id="31fce-183"><span id="_MOFfile_"></span><span id="_moffile_"></span><span id="_MOFFILE_"></span>**<**_MOFfile_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="31fce-184">Nome do arquivo a ser analisado.</span><span class="sxs-lookup"><span data-stu-id="31fce-184">Name of the file to parse.</span></span>

</dd> </dl>

## <a name="return-values"></a><span data-ttu-id="31fce-185">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="31fce-185">Return Values</span></span>

<span data-ttu-id="31fce-186">Como sua primeira operação, o compilador MOF executa uma verificação de sintaxe no arquivo MOF.</span><span class="sxs-lookup"><span data-stu-id="31fce-186">As its first operation, the MOF compiler performs a syntax check on the MOF file.</span></span> <span data-ttu-id="31fce-187">Se o compilador encontrar erros, ele imprime uma mensagem de erro e o processo é encerrado.</span><span class="sxs-lookup"><span data-stu-id="31fce-187">If the compiler finds any errors, it prints an error message and the process terminates.</span></span>

<span data-ttu-id="31fce-188">O compilador MOF pode retornar os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="31fce-188">The MOF compiler can return the following values:</span></span>

<dl> <dt>

<span data-ttu-id="31fce-189"><span id="0"></span>0</span><span class="sxs-lookup"><span data-stu-id="31fce-189"><span id="0"></span>0</span></span>
</dt> <dd>

<span data-ttu-id="31fce-190">A operação de compilação do MOF foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="31fce-190">MOF compile operation was successful.</span></span>

</dd> <dt>

<span data-ttu-id="31fce-191"><span id="1"></span>1</span><span class="sxs-lookup"><span data-stu-id="31fce-191"><span id="1"></span>1</span></span>
</dt> <dd>

<span data-ttu-id="31fce-192">O compilador MOF não pôde se conectar ao servidor WMI.</span><span class="sxs-lookup"><span data-stu-id="31fce-192">The MOF compiler could not connect with the WMI server.</span></span> <span data-ttu-id="31fce-193">Isso ocorre devido a um erro semântico, como uma incompatibilidade com o repositório WMI existente ou um erro real, como a falha do servidor WMI para iniciar.</span><span class="sxs-lookup"><span data-stu-id="31fce-193">This is either because of a semantic error such as an incompatibility with the existing WMI repository or an actual error such as the failure of the WMI server to start.</span></span>

</dd> <dt>

<span data-ttu-id="31fce-194"><span id="2"></span>2</span><span class="sxs-lookup"><span data-stu-id="31fce-194"><span id="2"></span>2</span></span>
</dt> <dd>

<span data-ttu-id="31fce-195">Uma ou mais opções de linha de comando não eram válidas.</span><span class="sxs-lookup"><span data-stu-id="31fce-195">One or more command-line switches were not valid.</span></span>

</dd> <dt>

<span data-ttu-id="31fce-196"><span id="3"></span>Beta</span><span class="sxs-lookup"><span data-stu-id="31fce-196"><span id="3"></span>3</span></span>
</dt> <dd>

<span data-ttu-id="31fce-197">Ocorreu um erro de sintaxe do MOF.</span><span class="sxs-lookup"><span data-stu-id="31fce-197">A MOF syntax error occurred.</span></span>

</dd> </dl>

<span data-ttu-id="31fce-198">Se o arquivo MOF for analisado corretamente, mas for feita uma tentativa de executar uma operação proibida por uma opção de linha de comando, o compilador retornará um código de erro gerado pelo WMI em vez de qualquer um dos códigos de retorno listados na lista anterior.</span><span class="sxs-lookup"><span data-stu-id="31fce-198">If the MOF file is parsed correctly, but an attempt is made to perform an operation that is forbidden by a command-line switch, the compiler returns an error code generated by WMI instead of any of the return codes listed in the list preceding.</span></span> <span data-ttu-id="31fce-199">Por exemplo, um código de erro WMI é retornado quando a opção **-Instance: UpdateOnly** é especificada e o arquivo MOF tenta criar uma instância.</span><span class="sxs-lookup"><span data-stu-id="31fce-199">For example, a WMI error code is returned when the **-instance:updateonly** switch is specified and the MOF file attempts to create an instance.</span></span>

<span data-ttu-id="31fce-200">Se a instrução de pré-processador de [**\# AutoRecuperação pragma**](pragma-autorecover.md) não estiver no arquivo, o seguinte aviso será retornado:</span><span class="sxs-lookup"><span data-stu-id="31fce-200">If the [**\#pragma autorecover**](pragma-autorecover.md) preprocessor statement is not in the file, then the following warning is returned:</span></span>

``` syntax
WARNING: FileYourMof.Mof does not contain #PRAGMA AUTORECOVER.
If the WMI repository is rebuilt in the future, the contents of this 
MOF file   will not be included in the new WMI repository.
To include this MOF file when the WMI Repository is automatically 
reconstructed, place the #PRAGMA AUTORECOVER statement on the first 
line of the MOF file.
```

## <a name="remarks"></a><span data-ttu-id="31fce-201">Comentários</span><span class="sxs-lookup"><span data-stu-id="31fce-201">Remarks</span></span>

<span data-ttu-id="31fce-202">O compilador MOF está disponível no diretório% windir% \\ System32 \\ WBEM.</span><span class="sxs-lookup"><span data-stu-id="31fce-202">The MOF Compiler is available in the %Windir%\\System32\\wbem directory.</span></span> <span data-ttu-id="31fce-203">Você deve especificar o arquivo MOF como o parâmetro do compilador MOF.</span><span class="sxs-lookup"><span data-stu-id="31fce-203">You must specify the MOF file as the parameter of the MOF Compiler.</span></span> <span data-ttu-id="31fce-204">Você também pode especificar uma opção de recuperação automática se quiser que o arquivo MOF seja recompilado automaticamente se o repositório CIM precisar ser recuperado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="31fce-204">You can also specify an Autorecover switch if you want the MOF file to be automatically recompiled if the CIM Repository ever has to be automatically recovered.</span></span> <span data-ttu-id="31fce-205">Para obter mais informações, digite **Mofcomp/?**</span><span class="sxs-lookup"><span data-stu-id="31fce-205">For more information, type **Mofcomp /?**</span></span> <span data-ttu-id="31fce-206">no prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="31fce-206">at the command prompt.</span></span>

<span data-ttu-id="31fce-207">Um arquivo MOF que usa o conjunto de caracteres Unicode contém uma assinatura como os dois primeiros bytes do arquivo.</span><span class="sxs-lookup"><span data-stu-id="31fce-207">A MOF file that uses the Unicode character set contains a signature as the first two bytes of the file.</span></span> <span data-ttu-id="31fce-208">Essa assinatura é U + FFFE ou U + FEFF, dependendo da ordenação de bytes do arquivo.</span><span class="sxs-lookup"><span data-stu-id="31fce-208">This signature is either U+FFFE or U+FEFF, depending on the byte ordering of the file.</span></span>

<span data-ttu-id="31fce-209">Quando nenhum erro ocorre no processo de análise, o compilador MOF se conecta ao servidor WMI em execução no computador local, a menos que a opção **-check** seja especificada.</span><span class="sxs-lookup"><span data-stu-id="31fce-209">When no errors occur in the parsing process, the MOF compiler connects to the WMI server running on the local computer unless the **-check** switch is specified.</span></span> <span data-ttu-id="31fce-210">As classes e instâncias definidas no arquivo MOF são adicionadas ao repositório do WMI.</span><span class="sxs-lookup"><span data-stu-id="31fce-210">Classes and instances defined in the MOF file are added to the WMI repository.</span></span>

<span data-ttu-id="31fce-211">Quando ocorre um erro na atualização do repositório WMI, o compilador não faz nenhuma tentativa de retornar o repositório para seu estado antes do início do compilador.</span><span class="sxs-lookup"><span data-stu-id="31fce-211">When an error occurs in updating the WMI repository, the compiler makes no attempt to return the repository to its state before the compiler began processing.</span></span>

<span data-ttu-id="31fce-212">**Windows 8:** Ao instalar um provedor, Mofcomp trata os \[ \] qualificadores de chave e \[ estático \] como true se estiverem presentes, independentemente de seus valores reais.</span><span class="sxs-lookup"><span data-stu-id="31fce-212">**Windows 8:** When installing a provider, mofcomp treats the \[Key\] and \[Static\] qualifiers as true if they are present, regardless of their actual values.</span></span> <span data-ttu-id="31fce-213">Outros qualificadores são tratados como false se estiverem presentes, mas não definidos explicitamente como true.</span><span class="sxs-lookup"><span data-stu-id="31fce-213">Other qualifiers are treated as false if they are present but not explicitly set to true.</span></span>

## <a name="requirements"></a><span data-ttu-id="31fce-214">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31fce-214">Requirements</span></span>



| <span data-ttu-id="31fce-215">Requisito</span><span class="sxs-lookup"><span data-stu-id="31fce-215">Requirement</span></span> | <span data-ttu-id="31fce-216">Valor</span><span class="sxs-lookup"><span data-stu-id="31fce-216">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="31fce-217">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31fce-217">Minimum supported client</span></span><br/> | <span data-ttu-id="31fce-218">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="31fce-218">Windows Vista</span></span><br/>       |
| <span data-ttu-id="31fce-219">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31fce-219">Minimum supported server</span></span><br/> | <span data-ttu-id="31fce-220">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="31fce-220">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="31fce-221">Confira também</span><span class="sxs-lookup"><span data-stu-id="31fce-221">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31fce-222">**namespace de pragma**</span><span class="sxs-lookup"><span data-stu-id="31fce-222">**pragma namespace**</span></span>](pragma-namespace.md)
</dt> <dt>

[<span data-ttu-id="31fce-223">Compilando arquivos MOF</span><span class="sxs-lookup"><span data-stu-id="31fce-223">Compiling MOF Files</span></span>](compiling-mof-files.md)
</dt> <dt>

[<span data-ttu-id="31fce-224">Compilando arquivos MOF localizados</span><span class="sxs-lookup"><span data-stu-id="31fce-224">Compiling Localized MOF Files</span></span>](compiling-localized-mof-files.md)
</dt> <dt>

[<span data-ttu-id="31fce-225">Registrando um provedor</span><span class="sxs-lookup"><span data-stu-id="31fce-225">Registering a Provider</span></span>](registering-a-provider.md)
</dt> <dt>

[<span data-ttu-id="31fce-226">**IMOFCompiler:: comcompilefile**</span><span class="sxs-lookup"><span data-stu-id="31fce-226">**IMOFCompiler::CompileFile**</span></span>](/windows/desktop/api/Wbemcli/nf-wbemcli-imofcompiler-compilefile)
</dt> </dl>

 

