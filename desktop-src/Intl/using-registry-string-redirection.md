---
description: O armazenamento de cadeias de caracteres embutidas no registro é parte de um modelo de localização anterior ao Windows Vista.
ms.assetid: 70185942-7d32-4151-a4e1-f71cf45e87af
title: Usando o redirecionamento de cadeia de caracteres do registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 287f6e1420aae0ff41c386e19852bebbd1a322c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105788076"
---
# <a name="using-registry-string-redirection"></a><span data-ttu-id="5e7b3-103">Usando o redirecionamento de cadeia de caracteres do registro</span><span class="sxs-lookup"><span data-stu-id="5e7b3-103">Using Registry String Redirection</span></span>

<span data-ttu-id="5e7b3-104">O armazenamento de cadeias de caracteres embutidas no registro é parte de um modelo de localização anterior ao Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-104">Storage of hard-coded strings in the registry is part of a pre-Windows Vista localization model.</span></span> <span data-ttu-id="5e7b3-105">Não há suporte para ele no MUI.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-105">It is not supported by MUI.</span></span> <span data-ttu-id="5e7b3-106">No modelo atual, a interface do usuário para o sistema operacional é executada em arquivos de recursos específicos de idioma sobre uma base neutra de idioma.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-106">In the current model, the user interface for the operating system runs in language-specific resource files on top of a language-neutral base.</span></span> <span data-ttu-id="5e7b3-107">Os componentes do sistema operacional usam o registro de maneira neutra de linguagem.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-107">The components of the operating system use the registry in a language-neutral manner.</span></span>

<span data-ttu-id="5e7b3-108">O MUI usa apenas as cadeias de caracteres de registro redirecionadas definidas por recursos do Win32 PE no arquivo de recurso de idioma base.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-108">MUI uses only redirected registry strings defined by Win32 PE resources in the base language resource file.</span></span> <span data-ttu-id="5e7b3-109">O redirecionamento é definido separadamente, por exemplo, em um arquivo. inf.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-109">Redirection is defined separately, for example, in an .inf file.</span></span> <span data-ttu-id="5e7b3-110">Esse tipo de armazenamento permite que o carregador de recursos selecione os recursos de idioma corretos automaticamente durante o carregamento do módulo de recurso.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-110">This type of storage allows the resource loader to select the correct language resources automatically during resource module loading.</span></span>

> [!Note]  
> <span data-ttu-id="5e7b3-111">Este tópico pertence apenas aos recursos do Win32 PE.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-111">This topic pertains only to Win32 PE resources.</span></span> <span data-ttu-id="5e7b3-112">Se você estiver usando recursos do PE não Win32, deverá fornecer redirecionamento de cadeia de caracteres de registro personalizado, se necessário.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-112">If using non-Win32 PE resources, you must provide customized registry string redirection, if required.</span></span>

 

## <a name="create-a-language-neutral-resource"></a><span data-ttu-id="5e7b3-113">Criar um recurso de Language-Neutral</span><span class="sxs-lookup"><span data-stu-id="5e7b3-113">Create a Language-Neutral Resource</span></span>

<span data-ttu-id="5e7b3-114">Um aplicativo MUI em execução no Windows Vista e posterior usa um recurso de cadeia de caracteres com neutralidade de idioma para permitir o acesso a cadeias de caracteres específicas de idioma armazenadas em uma tabela de recursos de cadeia.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-114">A MUI application running on Windows Vista and later uses a language-neutral string resource to allow access to language-specific strings stored in a string resource table.</span></span> <span data-ttu-id="5e7b3-115">O código do aplicativo que lê esses valores do registro é descrito na seção carregar um Language-Neutral valor do registro de [localizando cadeias de caracteres redirecionadas](locating-redirected-strings.md).</span><span class="sxs-lookup"><span data-stu-id="5e7b3-115">Application code that reads these values from the registry is described in the Load a Language-Neutral Registry Value section of [Locating Redirected Strings](locating-redirected-strings.md).</span></span>

<span data-ttu-id="5e7b3-116">Os dados de um valor de registro com neutralidade de idioma têm o formato " `@<PE-path>,-<stringID>[;<comment>]` ", em que:</span><span class="sxs-lookup"><span data-stu-id="5e7b3-116">The data for a language-neutral registry value has the format "`@<PE-path>,-<stringID>[;<comment>]`", where:</span></span>

-   <span data-ttu-id="5e7b3-117">*PE-path* especifica o caminho do executável.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-117">*PE-path* specifies the path of the executable.</span></span> <span data-ttu-id="5e7b3-118">Você pode especificar o caminho usando uma variável de ambiente, como% ProgramFiles%, para dar suporte à implantação.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-118">You can specify the path using an environment variable, such as %ProgramFiles%, to support deployment.</span></span> <span data-ttu-id="5e7b3-119">Uma alternativa para fazer sua referência de cadeia de caracteres é deixar as informações de caminho do arquivo.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-119">An alternative for making your string reference is to leave out the file path information.</span></span> <span data-ttu-id="5e7b3-120">Nesse caso, seu aplicativo deve ter alguns meios, por exemplo, outro valor de registro, para comunicar seu próprio diretório de instalação.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-120">In this case, your application must have some means, for example, another registry value, to communicate its own install directory.</span></span>
-   <span data-ttu-id="5e7b3-121">*stringid* especifica o identificador de recurso numérico do recurso de cadeia de caracteres relevante, que é implementado assim como qualquer outro recurso de cadeia de caracteres localizável.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-121">*stringID* specifies the numeric resource identifier of the relevant string resource, which is implemented just like any other localizable string resource.</span></span>
-   <span data-ttu-id="5e7b3-122">*Comentário* especifica informações opcionais para depuração ou legibilidade do valor do registro.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-122">*comment* specifies optional information for debugging or readability of the registry value.</span></span> <span data-ttu-id="5e7b3-123">As funções da API do registro ignoram o comentário ao carregar a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-123">The registry API functions ignore the comment when loading the string.</span></span>

> [!Note]  
> <span data-ttu-id="5e7b3-124">Os dados para o valor do registro não fazem nenhuma referência explícita ao arquivo de recurso específico do idioma.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-124">The data for the registry value makes no explicit reference to the language-specific resource file.</span></span> <span data-ttu-id="5e7b3-125">O arquivo correto é determinado em tempo de execução, com base nas preferências de idioma da interface do usuário atual.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-125">The correct file is determined at runtime, based on the current user interface language preferences.</span></span>

 

<span data-ttu-id="5e7b3-126">Um valor de registro é inserido sem um espaço entre "," e "-".</span><span class="sxs-lookup"><span data-stu-id="5e7b3-126">A registry value is entered without a space between the "," and "-".</span></span> <span data-ttu-id="5e7b3-127">Um valor correto do registro é:</span><span class="sxs-lookup"><span data-stu-id="5e7b3-127">A correct registry value is:</span></span>

`shell32.dll,-22912`

<span data-ttu-id="5e7b3-128">Um valor de registro incorreto é:</span><span class="sxs-lookup"><span data-stu-id="5e7b3-128">An incorrect registry value is:</span></span>

`shell32.dll, -22912`

<span data-ttu-id="5e7b3-129">Um exemplo do Windows Vista é o valor do registro com os seguintes dados:</span><span class="sxs-lookup"><span data-stu-id="5e7b3-129">An example from Windows Vista is the registry value with the following data:</span></span>

`@%SystemRoot%\system32\input.dll,-5020`

## <a name="create-resources-for-shortcut-strings"></a><span data-ttu-id="5e7b3-130">Criar recursos para cadeias de caracteres de atalho</span><span class="sxs-lookup"><span data-stu-id="5e7b3-130">Create Resources for Shortcut Strings</span></span>

<span data-ttu-id="5e7b3-131">Quando o aplicativo MUI exibe seu nome na interface do usuário do Shell, uma cadeia de caracteres InfoTip é exibida para o ícone do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-131">When the MUI application displays its name in the shell user interface, an InfoTip string is displayed for the application icon.</span></span> <span data-ttu-id="5e7b3-132">Você deve criar recursos de cadeia de caracteres para o nome de exibição do aplicativo e a cadeia de caracteres InfoTip associada para cada idioma com suporte.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-132">You should create string resources for your application display name and associated InfoTip string for each supported language.</span></span> <span data-ttu-id="5e7b3-133">Quando os recursos estiverem prontos, seu aplicativo poderá usar as cadeias de caracteres conforme descrito na seção usar API do Shell para carregar cadeias de caracteres de atalho da sessão de registro de [localizando cadeias de caracteres redirecionadas](locating-redirected-strings.md).</span><span class="sxs-lookup"><span data-stu-id="5e7b3-133">When the resources are ready, your application can use the strings as described in the Use Shell API to Load Shortcut Strings from the Registry section of [Locating Redirected Strings](locating-redirected-strings.md).</span></span>

### <a name="prepare-resources-for-a-shortcut-created-with-windows-installer"></a><span data-ttu-id="5e7b3-134">Preparar recursos para um atalho criado com Windows Installer</span><span class="sxs-lookup"><span data-stu-id="5e7b3-134">Prepare Resources for a Shortcut Created with Windows Installer</span></span>

<span data-ttu-id="5e7b3-135">Se você usar Windows Installer (MSI) para criar um atalho, os recursos de cadeia de caracteres incluirão o nome de exibição e a descrição do atalho.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-135">If you use Windows Installer (MSI) to create a shortcut, string resources include shortcut display name and description.</span></span> <span data-ttu-id="5e7b3-136">Na [tabela de atalho MSI](../msi/shortcut-table.md), a DLL de recurso é referenciada nas colunas apropriadas e os identificadores de recurso para seu nome de exibição de atalho e descrição são usados nas colunas do identificador de recurso correspondente.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-136">In the [MSI shortcut table](../msi/shortcut-table.md), the resource DLL is referenced in the appropriate columns and the resource identifiers for your shortcut display name and description are used in the corresponding resource identifier columns.</span></span>

<span data-ttu-id="5e7b3-137">Para que o atalho do aplicativo funcione corretamente com a tecnologia de recursos do MUI, tenha em mente os seguintes pontos ao preparar as cadeias de caracteres de atalho:</span><span class="sxs-lookup"><span data-stu-id="5e7b3-137">So that the application shortcut works properly with MUI resource technology, keep the following points in mind when preparing the shortcut strings:</span></span>

-   <span data-ttu-id="5e7b3-138">Use variáveis de ambiente ou um caminho relativo para registrar a DLL.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-138">Use either environment variables or a relative path to register the DLL.</span></span> <span data-ttu-id="5e7b3-139">Você pode especificar @% SystemRoot% \\ system32shell32.dll contanto que \\ o tipo de cadeia de caracteres do registro seja reg \_ Expand \_ sz.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-139">You can specify @%systemroot%\\system32\\shell32.dll as long as the registry string type is REG\_EXPAND\_SZ.</span></span> <span data-ttu-id="5e7b3-140">O identificador de recurso de cadeia de caracteres para "documento de texto" em Shell32.dll é 12345.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-140">The string resource identifier for "Text Document" in Shell32.dll is 12345.</span></span>
-   <span data-ttu-id="5e7b3-141">Não use espaços em volta dos símbolos "," e "-".</span><span class="sxs-lookup"><span data-stu-id="5e7b3-141">Do not use spaces around the "," and "-" symbols.</span></span> <span data-ttu-id="5e7b3-142">Um exemplo correto é "shell32.dll,-22912".</span><span class="sxs-lookup"><span data-stu-id="5e7b3-142">A correct example is "shell32.dll,-22912".</span></span>
-   <span data-ttu-id="5e7b3-143">Não use um nome de arquivo curto.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-143">Do not use a short file name.</span></span> <span data-ttu-id="5e7b3-144">Esse tipo de nome não funciona com o carregador de recursos.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-144">This type of name does not work with the resource loader.</span></span>

### <a name="prepare-resources-for-a-shortcut-using-inf-format"></a><span data-ttu-id="5e7b3-145">Preparar recursos para um atalho usando o formato INF</span><span class="sxs-lookup"><span data-stu-id="5e7b3-145">Prepare Resources for a Shortcut Using INF Format</span></span>

<span data-ttu-id="5e7b3-146">Se você usar o formato de arquivo INF para criar cadeias de caracteres de atalho, o arquivo de recursos deverá fazer as seguintes configurações do registro.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-146">If you use the INF file format to create shortcut strings, the resource file should make the following registry settings.</span></span> <span data-ttu-id="5e7b3-147">Essas instruções pressupõem o uso da sintaxe ProfileItems da API de instalação.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-147">These instructions assume the use of the ProfileItems syntax of Setup API.</span></span>

1.  <span data-ttu-id="5e7b3-148">Altere o valor de InfoTip para apontar para a referência de redirecionamento de cadeia de caracteres usando o caminho e o identificador de recurso.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-148">Change the InfoTip value to point to the string redirection reference, using the path and resource identifier.</span></span>
2.  <span data-ttu-id="5e7b3-149">Adicione o novo valor DisplayResource nas seções de instalação do ProfileItems.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-149">Add the new value DisplayResource under the ProfileItems installation sections.</span></span>

<span data-ttu-id="5e7b3-150">Veja a seguir um exemplo que mostra a adição do aplicativo Calculadora ao menu **Iniciar** :</span><span class="sxs-lookup"><span data-stu-id="5e7b3-150">The following is an example showing the addition of the Calculator application to the **Start** menu:</span></span>


```C++
[CalcInstallItems]
"Name" = %Calc_DESC%
"CmdLine" = 11, calc.exe
"SubDir" = %Access_GROUP%
"WorkingDir" = 11

"InfoTip" = "@%systemroot%\system32\shell32.dll,-22531"

"DisplayResource" = "%systemroot%\system32\shell32.dll",22019
```



<span data-ttu-id="5e7b3-151">Use a sintaxe mostrada abaixo ao usar o INF para adicionar itens, por exemplo, uma pasta de grupo de acesso, ao menu **Iniciar** .</span><span class="sxs-lookup"><span data-stu-id="5e7b3-151">Use the syntax shown below when using INF to add items, for example, an Access Group folder, to the **Start** menu.</span></span> <span data-ttu-id="5e7b3-152">Essa sintaxe pressupõe o uso do \[ \] suporte StartMenuItems da instalação, semelhante à sintaxe usada em Syssetup. inf.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-152">This syntax assumes the use of \[StartMenuItems\] support from Setup, similar to the syntax used in Syssetup.inf.</span></span>


```C++
[StartMenuItems]
<description> = <binary>,<commandline>,<iconfile>,<iconnum>,<infotip>,<resDLL,resID>
```



<span data-ttu-id="5e7b3-153">Defina o valor *InfoTip* para a referência de cadeia de caracteres " `@<path>,-resID` ".</span><span class="sxs-lookup"><span data-stu-id="5e7b3-153">Set the value *infotip* to the string reference "`@<path>,-resID`".</span></span>

<span data-ttu-id="5e7b3-154">O nome de exibição é determinado pelos valores *resDLL* e *resID* .</span><span class="sxs-lookup"><span data-stu-id="5e7b3-154">The display name is determined by the *resDLL* and *resID* values.</span></span> <span data-ttu-id="5e7b3-155">O valor *resID* especifica o identificador de recurso para um recurso de cadeia de caracteres associado ao arquivo de idioma neutro.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-155">The *resID* value specifies the resource identifier for a string resource associated with the language-neutral file.</span></span> <span data-ttu-id="5e7b3-156">O valor *resDLL* especifica o caminho para o arquivo de idioma neutro.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-156">The *resDLL* value specifies the path to the language-neutral file.</span></span>

## <a name="create-resources-for-friendly-document-type-names"></a><span data-ttu-id="5e7b3-157">Criar recursos para nomes de tipo de documento amigáveis</span><span class="sxs-lookup"><span data-stu-id="5e7b3-157">Create Resources for Friendly Document Type Names</span></span>

<span data-ttu-id="5e7b3-158">Você deve implementar o nome amigável e as cadeias de caracteres InfoTip para seu aplicativo como recursos de cadeia.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-158">You must implement friendly name and InfoTip strings for your application as string resources.</span></span> <span data-ttu-id="5e7b3-159">Para permitir que nomes de tipo de documento amigáveis reajam ao idioma da interface do usuário, o aplicativo deve registrar os nomes usando o valor FriendlyTypeName na chave do identificador de programa para o tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-159">To allow friendly document type names to react to the user interface language, the application must register the names using the FriendlyTypeName value under the program identifier key for the file type.</span></span> <span data-ttu-id="5e7b3-160">O valor padrão para a chave do identificador do programa deve ser mantido para manter a compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-160">The default value for the program identifier key should be retained to keep backward compatibility.</span></span> <span data-ttu-id="5e7b3-161">Para obter informações sobre como acessar os nomes do seu aplicativo, consulte os nomes de tipo de documento amigável da consulta na seção registro de [localizando cadeias de caracteres redirecionadas](locating-redirected-strings.md).</span><span class="sxs-lookup"><span data-stu-id="5e7b3-161">For information about accessing the names from your application, see the Query Friendly Document Type Names in the Registry section of [Locating Redirected Strings](locating-redirected-strings.md).</span></span>

<span data-ttu-id="5e7b3-162">O trabalho específico envolve as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="5e7b3-162">The specific work involves the following steps:</span></span>

1.  <span data-ttu-id="5e7b3-163">Implemente o nome amigável e as cadeias de caracteres InfoTip como recursos de cadeia específicos do idioma.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-163">Implement the friendly name and InfoTip strings as language-specific string resources.</span></span>
2.  <span data-ttu-id="5e7b3-164">Adicione o valor FriendlyTypeName na chave do registro do tipo de documento.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-164">Add the FriendlyTypeName value under the document type registry key.</span></span> <span data-ttu-id="5e7b3-165">Os dados para o valor seguem o padrão " `@<path>,-<resID>` ", em que *Path* indica o executável e *resID* é o identificador de recurso de um recurso de cadeia de caracteres localizável associado a esse executável.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-165">The data for the value follows the pattern "`@<path>,-<resID>`", where *path* indicates the executable and *resID* is the resource identifier of a localizable string resource associated with that executable.</span></span>
3.  <span data-ttu-id="5e7b3-166">Especifique o valor do registro InfoTip de acordo com o formato " `@<path>,-<resID>` ".</span><span class="sxs-lookup"><span data-stu-id="5e7b3-166">Specify the InfoTip registry value according to the format "`@<path>,-<resID>`".</span></span>

<span data-ttu-id="5e7b3-167">O exemplo a seguir mostra as configurações do registro para um arquivo. txt:</span><span class="sxs-lookup"><span data-stu-id="5e7b3-167">The following example shows the registry settings for a .txt file:</span></span>


```C++
HKCR\.txt
@="txtfile"
"Content Type"="text/plain"

HKCR\txtfile
@="Text Document"

"FriendlyTypeName" = "@%systemroot%\system32\shell32.dll,-12345"

"InfoTip" = "@%systemroot%\system32\shell32.dll,-12346"
```



## <a name="provide-resources-for-shell-verb-action-strings"></a><span data-ttu-id="5e7b3-168">Fornecer recursos para cadeias de caracteres de ação de verbo do Shell</span><span class="sxs-lookup"><span data-stu-id="5e7b3-168">Provide Resources for Shell Verb Action Strings</span></span>

<span data-ttu-id="5e7b3-169">Cadeias de caracteres de ação para determinados verbos, por exemplo, "abrir" e "Editar", são mostradas no menu pop-up exibido quando o usuário clica com o botão direito do mouse em um arquivo no Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-169">Action strings for certain verbs, for example, "open" and "edit", are shown in the pop-up menu displayed when the user right-clicks a file in Windows Explorer.</span></span> <span data-ttu-id="5e7b3-170">Seu aplicativo não precisa especificar cadeias de caracteres para verbos de shell comuns, pois o Shell tem seus próprios padrões habilitados para MUI para esses verbos.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-170">Your application does not have to specify strings for common shell verbs, as the shell has its own MUI-enabled defaults for these verbs.</span></span> <span data-ttu-id="5e7b3-171">No entanto, você deve fornecer recursos de cadeia de caracteres localizáveis para cadeias que representam verbos não comuns.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-171">However, you should provide localizable string resources for strings representing uncommon verbs.</span></span>

<span data-ttu-id="5e7b3-172">Em sistemas operacionais anteriores ao Windows XP, cadeias de caracteres para verbos de Shell no registro são renderizadas usando a sintaxe a seguir, em que *Verb* especifica o nome real do verbo:</span><span class="sxs-lookup"><span data-stu-id="5e7b3-172">On pre-Windows XP operating systems, strings for shell verbs in the registry are rendered using the following syntax, where *verb* specifies the actual verb name:</span></span>


```C++
HKCR\<progid>\shell\<verb>
@ = <friendly-name>
```



<span data-ttu-id="5e7b3-173">Veja um exemplo:</span><span class="sxs-lookup"><span data-stu-id="5e7b3-173">Here's an example:</span></span>


```C++
HKCR\Sample.app\shell\Disc
@ = "Disconnect"
```



<span data-ttu-id="5e7b3-174">No Windows XP e posterior, você pode usar um nível de indireção para fazer uma cadeia de caracteres de ação depender do idioma da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-174">On Windows XP and later, you can use a level of indirection to make an action string depend on user interface language.</span></span> <span data-ttu-id="5e7b3-175">Esses sistemas operacionais dão suporte a um valor de MUIVerb para definição de uma cadeia de caracteres compatível com MUI.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-175">These operating systems support a MUIVerb value for definition of a MUI-compatible string.</span></span> <span data-ttu-id="5e7b3-176">Aqui está um exemplo de uma entrada de registro para um verbo incomum:</span><span class="sxs-lookup"><span data-stu-id="5e7b3-176">Here's an example of a registry entry for an uncommon verb:</span></span>


```C++
HKCR\Sample.app\shell\Disc
@ = "Disconnect"
"MUIVerb" = "@%systemroot%\system32\sample.exe,-9875"
```



<span data-ttu-id="5e7b3-177">Seu aplicativo MUI também deve ser capaz de registrar o valor padrão antigo como uma cadeia de caracteres localizável, conforme mostrado abaixo:</span><span class="sxs-lookup"><span data-stu-id="5e7b3-177">Your MUI application should also be able to register the old default value as a localizable string, as shown below:</span></span>


```C++
HKCR\Sample.app\shell\Disc
@ = "@%systemroot%\system32\sample.exe,-9875"
```



> [!Note]  
> <span data-ttu-id="5e7b3-178">O registro do valor padrão antigo não é recomendado porque requer uma instalação diferente no Windows XP e posterior da instalação usada em sistemas operacionais anteriores.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-178">Registration of the old default value is not recommended because it requires a different setup on Windows XP and later from the setup used on earlier operating systems.</span></span>

 

## <a name="create-resources-for-verb-protocol-and-auxusertype-strings"></a><span data-ttu-id="5e7b3-179">Criar recursos para cadeias de caracteres verbo, protocolo e AuxUserType</span><span class="sxs-lookup"><span data-stu-id="5e7b3-179">Create Resources for Verb, Protocol, and AuxUserType Strings</span></span>

<span data-ttu-id="5e7b3-180">Você deve criar recursos de cadeia de caracteres localizáveis para sequências de verbo, protocolo e AuxUserType.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-180">You should create localizable string resources for Verb, Protocol, and AuxUserType strings.</span></span> <span data-ttu-id="5e7b3-181">Use as seguintes configurações do registro:</span><span class="sxs-lookup"><span data-stu-id="5e7b3-181">Use the following registry settings:</span></span>


```C++
HKCR\CLSID\{<Your_CLSID>}\Verb\<number> @="<Your Verb>, <menu_flag>, <verb_flag>"
"LocalizedString"="@<resDLLpath\resDLL.DLL>,-resStrID"
...

HKCR\CLSID\{<Your_CLSID>}\AuxUserType\<number>
@="<Your Short Name>"
"LocalizedString"="@<resDLLpath\resDLL.DLL>,-resStrID1"
...

HKCR\<Your_Name>\protocol\StdFileEditing\verb\<number>
@="<Your Verb>"
"LocalizedString"="@<resDLLpath\resDLL.DLL>,-resStrID"
...
```



<span data-ttu-id="5e7b3-182">O valor especificado para a Localizadastring contém apenas ou substitui o valor para *o verbo*, não os dois valores de sinalizador.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-182">The value specified for LocalizedString only contains or replaces the value for *Your Verb*, not the two flag values.</span></span>

<span data-ttu-id="5e7b3-183">Aqui está um resumo para ajudá-lo a garantir as configurações corretas do registro:</span><span class="sxs-lookup"><span data-stu-id="5e7b3-183">Here is a summary to help you ensure correct registry settings:</span></span>

-   <span data-ttu-id="5e7b3-184">Se CLSID tiver uma \\ chave de inserção de CLSID \\ {CLSID} de HKCR \\ , defina o valor padrão de CLSID usando CLSID de HKCR \\ \\ {CLSID} \\ localizadastring.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-184">If CLSID has a HKCR\\CLSID\\{clsid}\\Insertable key, define the default CLSID value using HKCR\\CLSID\\{clsid}\\LocalizedString.</span></span>
-   <span data-ttu-id="5e7b3-185">Se CLSID tiver uma ou mais subchaves no \\ \\ verbo {CLSID} do CLSID \\ de HKCR, defina cada cadeia de caracteres de verbo individual usando o verbo do% \\ CLSID} de HKCR \\ \\ \\ XXX \\ .</span><span class="sxs-lookup"><span data-stu-id="5e7b3-185">If CLSID has one or more subkeys under HKCR\\CLSID\\{clsid}\\Verb, define each individual Verb string using HKCR\\CLSID\\{clsid}\\Verb\\xxx\\LocalizedString.</span></span>
-   <span data-ttu-id="5e7b3-186">Se CLSID tiver uma ou mais subchaves no \\ verbo de StdFileEditing do protocolo HKCR {ProgID} \\ \\ \\ , defina cada cadeia de caracteres de verbo individual usando o \\ protocolo HKCR {ProgID} \\ \\ StdFileEditing \\ verbo \\ XXX \\ localizadastring.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-186">If CLSID has one or more subkeys under HKCR\\{progid}\\Protocol\\Stdfileediting\\Verb, define each individual Verb string using HKCR\\{progid}\\Protocol\\Stdfileediting\\Verb\\xxx\\LocalizedString.</span></span>
-   <span data-ttu-id="5e7b3-187">Se CLSID tiver uma ou mais subchaves AuxUserType listadas em \\ CLSID \\ de HKCR {CLSID} \\ AuxUserType, defina cada entrada AuxUserType usando o CLSID do HKCR \\ \\ {CLSID} \\ AuxUserType \\ XXX \\ .</span><span class="sxs-lookup"><span data-stu-id="5e7b3-187">If CLSID has one or more listed AuxUserType subkeys under HKCR\\CLSID\\{clsid}\\AuxUserType, define each AuxUserType entry using HKCR\\CLSID\\{clsid}\\AuxUserType\\xxx\\LocalizedString.</span></span>

## <a name="create-a-resource-for-the-uninstall-program"></a><span data-ttu-id="5e7b3-188">Criar um recurso para o programa de desinstalação</span><span class="sxs-lookup"><span data-stu-id="5e7b3-188">Create a Resource for the Uninstall Program</span></span>

<span data-ttu-id="5e7b3-189">Para registrar o programa de desinstalação do aplicativo, você pode criar valores de registro na subchave do identificador exclusivo para o aplicativo na chave do registro HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Uninstall.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-189">To register the uninstall program for the application, you can create registry values in the unique identifier subkey for the application under the registry key HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows\\CurrentVersion\\Uninstall.</span></span> <span data-ttu-id="5e7b3-190">Os valores a serem definidos incluem: DisplayName, DisplayVersion, Publisher, ProductID, RegOwner, RegCompany, UrlInfoAbout, HelpTelephone, HelpLink, InstallLocation, Installname, InstallDate, Contact, Comments, DisplayIcon, README, UrlUpdateInfo.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-190">Values to set include: DisplayName, DisplayVersion, Publisher, ProductID, RegOwner, RegCompany, UrlInfoAbout, HelpTelephone, HelpLink, InstallLocation, InstallSource, InstallDate, Contact, Comments, DisplayIcon, Readme, UrlUpdateInfo.</span></span>

> [!Note]  
> <span data-ttu-id="5e7b3-191">Para habilitar a tecnologia MUI para cada valor, você pode acrescentar " \_ localizado" ao nome do valor.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-191">To enable MUI technology for each value, you can append "\_Localized" to the value name.</span></span>

 

<span data-ttu-id="5e7b3-192">Os componentes do sistema operacional são necessários para fornecer um valor para DisplayName \_ localizado de uma maneira específica de MUI.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-192">Operating system components are required to provide a value for DisplayName\_Localized in a MUI-specific way.</span></span> <span data-ttu-id="5e7b3-193">Você deve posicionar o nome de exibição em uma DLL, como Res.dll, como um recurso de cadeia de caracteres, supondo que o identificador seja 1245.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-193">You should place the display name in a DLL, such as Res.dll, as a string resource, assuming the identifier to be 1245.</span></span> <span data-ttu-id="5e7b3-194">Em seguida, o aplicativo pode registrar o nome de exibição como DisplayName \_ localizado com o valor "@ \\res.DLL,-1245".</span><span class="sxs-lookup"><span data-stu-id="5e7b3-194">Then the application can register the display name as DisplayName\_Localized with value "@\\res.DLL,-1245".</span></span> <span data-ttu-id="5e7b3-195">Todas as outras configurações do registro devem ser mantidas como estão, incluindo o valor original para DisplayName.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-195">All the other registry settings should be retained as they are, including the original value for DisplayName.</span></span>

## <a name="create-resources-for-sound-events"></a><span data-ttu-id="5e7b3-196">Criar recursos para eventos de som</span><span class="sxs-lookup"><span data-stu-id="5e7b3-196">Create Resources for Sound Events</span></span>

<span data-ttu-id="5e7b3-197">O Windows associa determinados eventos a arquivos de som, por exemplo, um novo evento de notificação por email ou um evento de alarme de bateria crítica.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-197">Windows associates certain events with sound files, for example, a New Mail Notification event or a Critical Battery Alarm event.</span></span> <span data-ttu-id="5e7b3-198">Os nomes de evento devem ser exibidos pela interface do usuário e devem oferecer suporte à globalização.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-198">The event names must be displayed by the user interface and must support globalization.</span></span> <span data-ttu-id="5e7b3-199">Portanto, você deve implementar um recurso de cadeia de caracteres localizável para a descrição de cada descrição de evento.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-199">Therefore, you should implement a localizable string resource for the description of each event description.</span></span> <span data-ttu-id="5e7b3-200">Adicione um novo valor de registro para cada nome de evento, além do valor padrão embutido em código.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-200">Add a new registry value for each event name, in addition to the hard-coded default value.</span></span>

<span data-ttu-id="5e7b3-201">Faça o seguinte para habilitar um evento de som:</span><span class="sxs-lookup"><span data-stu-id="5e7b3-201">Do the following to enable a sound event:</span></span>

1.  <span data-ttu-id="5e7b3-202">Implemente a descrição como um recurso de cadeia de caracteres localizável.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-202">Implement the description as a localizable string resource.</span></span>
2.  <span data-ttu-id="5e7b3-203">Adicione um novo valor de registro para o nome de exibição, além do valor padrão embutido em código.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-203">Add a new registry value for the display name, in addition to the hard-coded default value.</span></span> <span data-ttu-id="5e7b3-204">O layout do registro associado é mostrado abaixo:</span><span class="sxs-lookup"><span data-stu-id="5e7b3-204">The associated registry layout is shown below:</span></span>


```C++
HKCR\AppEvents\EventLabels
<event_name>
    (Default) REG_SZ "<description>"
    DispFileName REG_EXPAND_SZ "@<path>,-<resID>"
```



<span data-ttu-id="5e7b3-205">Se o shell não conseguir localizar ou recuperar o valor de DispFileName, ele usará a descrição padrão.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-205">If the shell cannot find or retrieve the value of DispFileName, it uses the default description.</span></span>

## <a name="create-resources-for-keyboard-layout-strings"></a><span data-ttu-id="5e7b3-206">Criar recursos para cadeias de caracteres de layout do teclado</span><span class="sxs-lookup"><span data-stu-id="5e7b3-206">Create Resources for Keyboard Layout Strings</span></span>

<span data-ttu-id="5e7b3-207">Se seu aplicativo implementa um layout de teclado, ele requer um recurso de cadeia de caracteres localizável para o nome do layout para exibição de tela, por exemplo, em listas de layouts de teclado.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-207">If your application implements a keyboard layout, it requires a localizable string resource for the name of the layout for screen display, for example, in lists of keyboard layouts.</span></span> <span data-ttu-id="5e7b3-208">Cada layout de teclado tem uma chave do registro em HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Control \\ teclado layouts.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-208">Each keyboard layout has a registry key under HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\Keyboard Layouts.</span></span>

<span data-ttu-id="5e7b3-209">Entre os valores dessa chave estão o texto do layout, um nome legível para compatibilidade com versões anteriores e o nome de exibição do layout.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-209">Among the values for that key are Layout Text, a human-readable name for backward compatibility, and Layout Display Name.</span></span> <span data-ttu-id="5e7b3-210">Os dados fornecidos para o nome de exibição de layout devem ser uma referência de cadeia de caracteres do formato " `@<path>,-resID` ", referindo-se a um recurso de cadeia de caracteres localizável associado ao layout do teclado.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-210">The data supplied for Layout Display Name should be a string reference of the form "`@<path>,-resID`", referring to a localizable string resource associated with the keyboard layout.</span></span>

<span data-ttu-id="5e7b3-211">Aqui está um exemplo de uma configuração de registro para o layout de teclado espanhol (Espanha):</span><span class="sxs-lookup"><span data-stu-id="5e7b3-211">Here is an example of a registry setting for the Spanish (Spain) keyboard layout:</span></span>

`Layout Display Name=@%SystemRoot%\system32\input.dll,-5020`

## <a name="represent-ole-insert-object-common-dialog-strings"></a><span data-ttu-id="5e7b3-212">Representar cadeias de diálogo comuns de objeto de inserção OLE</span><span class="sxs-lookup"><span data-stu-id="5e7b3-212">Represent OLE Insert Object Common Dialog Strings</span></span>

<span data-ttu-id="5e7b3-213">Você pode implementar o nome de exibição de um objeto OLE insertável como um recurso de cadeia de caracteres localizável associado ao código que implementa esse objeto.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-213">You can implement the display name of an OLE insertable object as a localizable string resource associated with the code implementing that object.</span></span> <span data-ttu-id="5e7b3-214">A [caixa de diálogo objeto de inserção OLE](/cpp/mfc/reference/coleinsertdialog-class) Obtém um nome de exibição da chave do registro do \\ CLSID \\ { *<GUID>* }, em que *GUID* identifica o identificador de classe de um objeto OLE que poderia ser inserido.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-214">The [OLE Insert Object dialog box](/cpp/mfc/reference/coleinsertdialog-class) gets a display name from the registry key HKCR\\CLSID\\{*<GUID>*}, where *GUID* identifies the class identifier of an insertable OLE object.</span></span> <span data-ttu-id="5e7b3-215">O Windows Vista e versões posteriores implementam esse tipo de objeto de forma localizável, usando um nome de exibição compatível com MUI que permite a personalização para o idioma da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-215">Windows Vista and later implement this type of object in a localizable way, using a MUI-compliant display name that allows customization to the user interface language.</span></span> <span data-ttu-id="5e7b3-216">Por outro lado, os sistemas operacionais anteriores ao Windows Vista implementam o nome de exibição para esse tipo de objeto usando o valor padrão da chave do registro correspondente.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-216">In contrast, pre-Windows Vista operating systems implement the display name for this type of object using the default value of the corresponding registry key.</span></span> <span data-ttu-id="5e7b3-217">Normalmente, esse nome é um nome em inglês (Estados Unidos) ou um nome no idioma da interface do usuário padrão do sistema.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-217">Typically this name is either an English (United States) name or a name in the system default UI language.</span></span>

> [!Note]  
> <span data-ttu-id="5e7b3-218">Nem todos os objetos que correspondem a subchaves da chave do registro podem ser inseridos.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-218">Not all objects that correspond to subkeys of the registry key are insertable.</span></span>

 

<span data-ttu-id="5e7b3-219">O valor padrão da chave do \\ CLSID de HKCR \\ { *<GUID>* } deve reter um nome legível para compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-219">The default value of the HKCR\\CLSID\\{*<GUID>*} key should retain a human-readable name for backward compatibility.</span></span> <span data-ttu-id="5e7b3-220">No entanto, ele também deve definir o valor de localizadores, no formato " `@<path>,-ResID` ", em que Path identifica o arquivo executável que implementa o objeto.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-220">However, it should also define the LocalizedString value, in the format "`@<path>,-ResID`", where path identifies the executable file implementing the object.</span></span> <span data-ttu-id="5e7b3-221">O valor ResID especifica o identificador de recurso da cadeia de caracteres localizável para o nome de exibição.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-221">The ResID value specifies the resource identifier of the localizable string for the display name.</span></span>

<span data-ttu-id="5e7b3-222">Por exemplo, o script de registro para o objeto de clipe de mídia que poderia ser inserido inclui as seguintes linhas:</span><span class="sxs-lookup"><span data-stu-id="5e7b3-222">For example, the registration script for the insertable Media Clip object includes the following lines:</span></span>


```C++
HKCR,"CLSID\%CLSID_Media_Clip%",,,"%default description%"
HKCR,"CLSID\%CLSID_Media_Clip%","LocalizedString",,"@%systemroot%\system32\mplay32.exe,-9217"
```



<span data-ttu-id="5e7b3-223">A primeira linha fornece compatibilidade com versões anteriores, colocando uma cadeia de texto simples no registro como um nome de exibição padrão.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-223">The first line provides backward compatibility by placing a simple text string in the registry as a default display name.</span></span> <span data-ttu-id="5e7b3-224">A segunda linha fornece acesso ao nome de exibição compatível com MUI.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-224">The second line provides access to the MUI-compliant display name.</span></span> <span data-ttu-id="5e7b3-225">Indica o identificador de cadeia de caracteres armazenado em Mplay32.exe.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-225">It indicates the string identifier stored in Mplay32.exe.</span></span> <span data-ttu-id="5e7b3-226">A cadeia de caracteres com o identificador 9217 em Mplay32.exe pode ser associada a valores de recursos de cadeia de caracteres para qualquer número de idiomas.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-226">The string with identifier 9217 in Mplay32.exe can be associated with string resource values for any number of languages.</span></span> <span data-ttu-id="5e7b3-227">Seu nome em inglês (Estados Unidos) é "Media clip".</span><span class="sxs-lookup"><span data-stu-id="5e7b3-227">Its English (United States) name is "Media Clip".</span></span>

## <a name="create-string-resources-for-microsoft-management-console-snap-ins"></a><span data-ttu-id="5e7b3-228">Criar recursos de cadeia de caracteres para o console de gerenciamento Microsoft Snap-Ins</span><span class="sxs-lookup"><span data-stu-id="5e7b3-228">Create String Resources for Microsoft Management Console Snap-Ins</span></span>

<span data-ttu-id="5e7b3-229">Você deve criar um recurso de cadeia de caracteres localizável para cada snap-in do MMC (console de gerenciamento Microsoft) usado pelo seu aplicativo MUI.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-229">You should create a localizable string resource for each Microsoft Management Console (MMC) snap-in used by your MUI application.</span></span> <span data-ttu-id="5e7b3-230">Como um snap-in faz parte de um console do, ele tem uma interface do usuário e deve ser globalizado para operar em mais de um idioma.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-230">Because a snap-in is part of a console, it has a user interface and must be globalized to operate in more than one language.</span></span>

<span data-ttu-id="5e7b3-231">Na maior parte, os snap-ins do MMC geram os mesmos problemas de globalização e localização que o próprio aplicativo MUI.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-231">For the most part, MMC snap-ins raise the same globalization and localization issues as the MUI application itself.</span></span> <span data-ttu-id="5e7b3-232">Um snap-in do MMC deve refletir seu nome no registro para exibição.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-232">An MMC snap-in must reflect its name in the registry for display.</span></span> <span data-ttu-id="5e7b3-233">A entrada do registro deve incluir uma referência indireta a um recurso de cadeia de caracteres localizável e uma cadeia de caracteres literal para compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-233">The registry entry should include both an indirect reference to a localizable string resource and a literal string for backward compatibility.</span></span>

<span data-ttu-id="5e7b3-234">Cada snap-in do MMC tem uma chave do registro em HKEY \_ local \_ Machine \\ software \\ Microsoft \\ MMC \\ Snaps.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-234">Each MMC snap-in has a registry key under HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\MMC\\SnapIns.</span></span> <span data-ttu-id="5e7b3-235">Entre os valores dessa chave estão namestring, especificando um nome legível por humanos para compatibilidade com versões anteriores e NameStringIndirect, especificando uma referência indireta a um recurso de cadeia de caracteres localizável.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-235">Among the values for that key are NameString, specifying a human-readable name for backward compatibility, and NameStringIndirect, specifying an indirect reference to a localizable string resource.</span></span> <span data-ttu-id="5e7b3-236">Para NameStringIndirect, você deve fornecer uma referência de cadeia de caracteres no formato " `@<path>,-resID` ", representando um recurso de cadeia de caracteres localizável.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-236">For NameStringIndirect, you should provide a string reference of the form "`@<path>,-resID`", representing a localizable string resource.</span></span>

<span data-ttu-id="5e7b3-237">Por exemplo, você pode fazer a seguinte configuração para Mymmc.dll, em que 12345 é o identificador do recurso de cadeia de caracteres correspondente que contém o nome localizável do snap-in:</span><span class="sxs-lookup"><span data-stu-id="5e7b3-237">For example, you might make the following setting for Mymmc.dll, where 12345 is the identifier of the corresponding string resource containing the localizable name of the snap-in:</span></span>


```C++
NameStringIndirect=@%systemroot%@c:\windir\system32\mymmc.dll,-12345
```



<span data-ttu-id="5e7b3-238">Alguns snap-ins registram outros valores de cadeia de caracteres do registro que o MMC não lê do registro.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-238">Some snap-ins register other registry string values that MMC does not read from the registry.</span></span> <span data-ttu-id="5e7b3-239">Para obter mais informações sobre como usar esses valores, consulte registrar o console de gerenciamento Microsoft Snap-In cadeias de caracteres não lidas do registro ao [Localizar cadeias de caracteres redirecionadas](locating-redirected-strings.md).</span><span class="sxs-lookup"><span data-stu-id="5e7b3-239">For more information about using these values, see Register Microsoft Management Console Snap-In Strings Not Read from the Registry in [Locating Redirected Strings](locating-redirected-strings.md).</span></span>

## <a name="create-string-resources-for-a-windows-service"></a><span data-ttu-id="5e7b3-240">Criar recursos de cadeia de caracteres para um serviço do Windows</span><span class="sxs-lookup"><span data-stu-id="5e7b3-240">Create String Resources for a Windows Service</span></span>

<span data-ttu-id="5e7b3-241">Embora um serviço do Windows normalmente tenha pouca ou nenhuma interface do usuário, ele deve exibir um nome em conformidade com o MUI e geralmente fornece uma descrição específica de linguagem compatível com MUI.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-241">Although a Windows service typically has little or no user interface, it must display a MUI-compliant name and usually provides a MUI-compliant language-specific description.</span></span> <span data-ttu-id="5e7b3-242">A chave do registro que descreve um serviço do Windows dá suporte apenas ao valor DisplayName para o nome do serviço e o valor de descrição para a descrição do serviço.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-242">The registry key that describes a Windows service supports only the DisplayName value for the service name and the Description value for the service description.</span></span>

<span data-ttu-id="5e7b3-243">As configurações para o serviço do Windows são feitas do aplicativo, conforme descrito em definir o nome de exibição e a descrição de um serviço do Windows do registro ao [Localizar cadeias de caracteres redirecionadas](locating-redirected-strings.md).</span><span class="sxs-lookup"><span data-stu-id="5e7b3-243">Settings for the Windows service are made from the application, as described in Set the Display Name and Description for a Windows Service from the Registry in [Locating Redirected Strings](locating-redirected-strings.md).</span></span> <span data-ttu-id="5e7b3-244">Se o seu aplicativo não definir os valores do registro para a interface do usuário do serviço, os valores no registro permanecerão definidos como Inglês, mesmo que a interface do usuário esteja em outro idioma.</span><span class="sxs-lookup"><span data-stu-id="5e7b3-244">If your application does not set the registry values for the service user interface, values in the registry remain set to English, even if the user interface is in another language.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5e7b3-245">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5e7b3-245">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e7b3-246">Preparando recursos</span><span class="sxs-lookup"><span data-stu-id="5e7b3-246">Preparing Resources</span></span>](preparing-resources.md)
</dt> <dt>

[<span data-ttu-id="5e7b3-247">Localizando cadeias de caracteres redirecionadas</span><span class="sxs-lookup"><span data-stu-id="5e7b3-247">Locating Redirected Strings</span></span>](locating-redirected-strings.md)
</dt> </dl>

 

 
