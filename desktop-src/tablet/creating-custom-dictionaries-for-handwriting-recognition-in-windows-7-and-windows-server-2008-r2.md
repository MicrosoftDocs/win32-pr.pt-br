---
description: Esta seção explica como criar um dicionário personalizado para o reconhecimento de manuscrito.
ms.assetid: 83abf534-740c-44a3-bbd4-babb54f2930e
title: Criando dicionários personalizados para reconhecimento de manuscrito no Windows 7 e no Windows Server 2008 R2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80b9b7b5a1d9dfadddd83825aea7d6f676439999
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105807262"
---
# <a name="creating-custom-dictionaries-for-handwriting-recognition-in-windows-7-and-windows-server-2008-r2"></a><span data-ttu-id="f9c77-103">Criando dicionários personalizados para reconhecimento de manuscrito no Windows 7 e no Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f9c77-103">Creating Custom Dictionaries for Handwriting Recognition in Windows 7 and Windows Server 2008 R2</span></span>

<span data-ttu-id="f9c77-104">Esta seção explica como criar um dicionário personalizado para o reconhecimento de manuscrito.</span><span class="sxs-lookup"><span data-stu-id="f9c77-104">This section explains how to create a custom dictionary for handwriting recognition.</span></span>

<span data-ttu-id="f9c77-105">No sistema operacional Windows 7 e no sistema operacional Windows Server 2008 R2, a precisão do reconhecimento de manuscrito pode ser significativamente melhorada com o uso de dicionários personalizados.</span><span class="sxs-lookup"><span data-stu-id="f9c77-105">In the Windows 7 operating system and the Windows Server 2008 R2 operating system, the accuracy of handwriting recognition can be significantly improved through the use of custom dictionaries.</span></span> <span data-ttu-id="f9c77-106">Esses dicionários complementam ou substituem os dicionários do sistema usados para manuscrito.</span><span class="sxs-lookup"><span data-stu-id="f9c77-106">These dictionaries supplement or replace system dictionaries used for handwriting.</span></span> <span data-ttu-id="f9c77-107">O suporte ao reconhecimento de manuscrito é fornecido por meio do recurso Serviços de Reconhecimento de Manuscrito que precisa ser habilitado por meio de Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="f9c77-107">Support for handwriting recognition is provided through the Ink and Handwriting Services feature that needs to be enabled through Server Manager.</span></span>

> [!Note]  
> <span data-ttu-id="f9c77-108">Os dicionários personalizados podem ser instalados para um idioma somente se o reconhecedor de manuscrito para esse idioma estiver instalado.</span><span class="sxs-lookup"><span data-stu-id="f9c77-108">Custom dictionaries can be installed for a language only if the handwriting recognizer for that language is installed.</span></span>

 

<span data-ttu-id="f9c77-109">Há duas etapas básicas para configurar um dicionário personalizado para manuscrito:</span><span class="sxs-lookup"><span data-stu-id="f9c77-109">There are two basic steps to setting up a custom dictionary for handwriting:</span></span>

-   <span data-ttu-id="f9c77-110">Compilar uma lista de palavras.</span><span class="sxs-lookup"><span data-stu-id="f9c77-110">Compile a word list.</span></span> <span data-ttu-id="f9c77-111">A compilação cria um arquivo de dicionário personalizado compilado (. hwrdict).</span><span class="sxs-lookup"><span data-stu-id="f9c77-111">The compilation creates a compiled custom dictionary (.hwrdict) file.</span></span>
-   <span data-ttu-id="f9c77-112">Instale o dicionário personalizado compilado.</span><span class="sxs-lookup"><span data-stu-id="f9c77-112">Install the compiled custom dictionary.</span></span>

## <a name="compiling-a-word-list"></a><span data-ttu-id="f9c77-113">Compilando uma lista de palavras</span><span class="sxs-lookup"><span data-stu-id="f9c77-113">Compiling a Word List</span></span>

<span data-ttu-id="f9c77-114">A lista de palavras a ser compilada deve estar no formato de texto sem formatação e deve ser salva usando uma codificação Unicode.</span><span class="sxs-lookup"><span data-stu-id="f9c77-114">The word list to be compiled must be in plain-text format and should be saved using a Unicode encoding.</span></span> <span data-ttu-id="f9c77-115">Outras codificações não funcionarão.</span><span class="sxs-lookup"><span data-stu-id="f9c77-115">Other encodings will not work.</span></span> <span data-ttu-id="f9c77-116">Cada linha do arquivo de texto é usada como uma única entrada no dicionário.</span><span class="sxs-lookup"><span data-stu-id="f9c77-116">Each line of the text file is taken as a single entry in the dictionary.</span></span> <span data-ttu-id="f9c77-117">São permitidas entradas de unidades de multipalavra contendo um ou mais espaços.</span><span class="sxs-lookup"><span data-stu-id="f9c77-117">Multiword units entries containing one or more spaces are allowed.</span></span> <span data-ttu-id="f9c77-118">Os espaços no início ou no final de uma linha são ignorados.</span><span class="sxs-lookup"><span data-stu-id="f9c77-118">Spaces at the beginning or end of a line are ignored.</span></span>

<span data-ttu-id="f9c77-119">Um dicionário personalizado é compilado a partir de uma linha de comando.</span><span class="sxs-lookup"><span data-stu-id="f9c77-119">A custom dictionary is compiled from a command line.</span></span> <span data-ttu-id="f9c77-120">Para compilar um dicionário, abra uma janela de comando, navegue até a pasta que contém a lista de palavras e execute HwrComp.exe com as opções de linha de comando que você deseja usar.</span><span class="sxs-lookup"><span data-stu-id="f9c77-120">To compile a dictionary, open a command window, navigate to the folder containing the word list, and then run HwrComp.exe with the command-line options you want to use.</span></span>

<span data-ttu-id="f9c77-121">O exemplo a seguir mostra a sintaxe de uso para as opções de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="f9c77-121">The following example shows the usage syntax for the command-line options.</span></span>

``` syntax
Usage: hwrcomp       [-lang <localename>] [-type <type>]
    [-comment <comment>]
    [-o <dictfile.hwrdict>]
    <inputfile>
     
```

### <a name="explanation-of-options"></a><span data-ttu-id="f9c77-122">Explicação das opções</span><span class="sxs-lookup"><span data-stu-id="f9c77-122">Explanation of Options</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f9c77-123">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="f9c77-123">Parameter</span></span></th>
<th><span data-ttu-id="f9c77-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="f9c77-124">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9c77-125">-lang <localename></span><span class="sxs-lookup"><span data-stu-id="f9c77-125">-lang <localename></span></span></td>
<td><span data-ttu-id="f9c77-126">O nome de localidade especificado atribuído ao arquivo de dicionário personalizado compilado.</span><span class="sxs-lookup"><span data-stu-id="f9c77-126">The specified locale name assigned to the compiled custom dictionary file.</span></span> <span data-ttu-id="f9c77-127">O argumento <localename> tem o formato idioma-região.</span><span class="sxs-lookup"><span data-stu-id="f9c77-127">The argument <localename> has the form language-REGION.</span></span> <span data-ttu-id="f9c77-128">Um exemplo disso é en-US, que significa o idioma inglês na região de Estados Unidos.</span><span class="sxs-lookup"><span data-stu-id="f9c77-128">An example of this is en-US, which signifies the English language in the United States region.</span></span> <span data-ttu-id="f9c77-129">Para obter exemplos desse formulário, consulte [constantes e cadeias de caracteres de identificador de linguagem](/windows/desktop/Intl/language-identifier-constants-and-strings).</span><span class="sxs-lookup"><span data-stu-id="f9c77-129">For examples of this form, see [Language Identifier Constants and Strings](/windows/desktop/Intl/language-identifier-constants-and-strings).</span></span> <span data-ttu-id="f9c77-130">Os seguintes idiomas têm suporte para o Windows 7 e o Windows Server 2008 R2 por esse recurso: en-US, en-GB, en-CA, en-AU, de-DE, de-CH, fr-FR, es-ES, es-MX, es-AR, it-IT, NL-NL, NL-is, pt-BR, pt-PT, da-DK, SV-SE, NB-NO, NN-não, fi-FI, pl-PL, CS-CZ, ru-RU, RO-RO, Sr-LATN-CS, Sr-Cyrl-CS, CA-ES e HR-HR.</span><span class="sxs-lookup"><span data-stu-id="f9c77-130">The following languages are supported for Windows 7 and Windows Server 2008 R2 by this feature: en-US, en-GB, en-CA, en-AU, de-DE, de-CH, fr-FR, es-ES, es-MX, es-AR, it-IT, nl-NL, nl-BE, pt-BR, pt-PT, da-DK, sv-SE, nb-NO, nn-NO, fi-FI, pl-PL, cs-CZ, ru-RU, ro-RO, sr-Latn-CS, sr-Cyrl-CS, ca-ES and hr-HR.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9c77-131">-tipo <type></span><span class="sxs-lookup"><span data-stu-id="f9c77-131">-type <type></span></span></td>
<td><span data-ttu-id="f9c77-132">O argumento de opção <type> é uma concatenação de cadeia de caracteres única do uso do recurso como a lista de palavras principal (primária) ou como um suplemento para a lista de palavras principal (secundária) seguida pelo nome da lista de palavras real ao qual o recurso é aplicado (como Dictionary ou sobrenome).</span><span class="sxs-lookup"><span data-stu-id="f9c77-132">The option argument <type> is a single-string concatenation of the resource's use as either the main word list (PRIMARY) or as a supplement to the main word list (SECONDARY) followed by the actual word list name to which the resource is applied (such as DICTIONARY or SURNAME).</span></span> <span data-ttu-id="f9c77-133">O valores possíveis são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="f9c77-133">The following are possible values:</span></span>
<ul>
<li><span data-ttu-id="f9c77-134">PRIMÁRIO-CITYNAME-LISTA</span><span class="sxs-lookup"><span data-stu-id="f9c77-134">PRIMARY-CITYNAME-LIST</span></span></li>
<li><span data-ttu-id="f9c77-135">PRIMÁRIO-PAÍSNAME-LISTA</span><span class="sxs-lookup"><span data-stu-id="f9c77-135">PRIMARY-COUNTRYNAME-LIST</span></span></li>
<li><span data-ttu-id="f9c77-136">COUNTRYSHORTNAME PRIMÁRIO-LISTA</span><span class="sxs-lookup"><span data-stu-id="f9c77-136">PRIMARY-COUNTRYSHORTNAME-LIST</span></span></li>
<li><span data-ttu-id="f9c77-137">DICIONÁRIO PRIMÁRIO</span><span class="sxs-lookup"><span data-stu-id="f9c77-137">PRIMARY-DICTIONARY</span></span></li>
<li><span data-ttu-id="f9c77-138">PRIMÁRIA-LISTA ESPECIFICADA</span><span class="sxs-lookup"><span data-stu-id="f9c77-138">PRIMARY-GIVENNAME-LIST</span></span></li>
<li><span data-ttu-id="f9c77-139">ESTADOOUPROVÍNCIA PRIMÁRIO-LISTA</span><span class="sxs-lookup"><span data-stu-id="f9c77-139">PRIMARY-STATEORPROVINCE-LIST</span></span></li>
<li><span data-ttu-id="f9c77-140">PRIMÁRIO-RUA-DA-LISTA</span><span class="sxs-lookup"><span data-stu-id="f9c77-140">PRIMARY-STREETNAME-LIST</span></span></li>
<li><span data-ttu-id="f9c77-141">PRIMARY-SOBRENOME-LISTA</span><span class="sxs-lookup"><span data-stu-id="f9c77-141">PRIMARY-SURNAME-LIST</span></span></li>
<li><span data-ttu-id="f9c77-142">SECUNDÁRIA-CITYNAME-LISTA</span><span class="sxs-lookup"><span data-stu-id="f9c77-142">SECONDARY-CITYNAME-LIST</span></span></li>
<li><span data-ttu-id="f9c77-143">LISTA DE PAÍSNAME SECUNDÁRIA</span><span class="sxs-lookup"><span data-stu-id="f9c77-143">SECONDARY-COUNTRYNAME-LIST</span></span></li>
<li><span data-ttu-id="f9c77-144">COUNTRYSHORTNAME SECUNDÁRIO-LISTA</span><span class="sxs-lookup"><span data-stu-id="f9c77-144">SECONDARY-COUNTRYSHORTNAME-LIST</span></span></li>
<li><span data-ttu-id="f9c77-145">DICIONÁRIO SECUNDÁRIO</span><span class="sxs-lookup"><span data-stu-id="f9c77-145">SECONDARY-DICTIONARY</span></span></li>
<li><span data-ttu-id="f9c77-146">EMAILSMTP SECUNDÁRIO-LISTA</span><span class="sxs-lookup"><span data-stu-id="f9c77-146">SECONDARY-EMAILSMTP-LIST</span></span></li>
<li><span data-ttu-id="f9c77-147">EMAILUSERNAME SECUNDÁRIO-LISTA</span><span class="sxs-lookup"><span data-stu-id="f9c77-147">SECONDARY-EMAILUSERNAME-LIST</span></span></li>
<li><span data-ttu-id="f9c77-148">SECUNDÁRIA-LISTA ESPECIFICADA</span><span class="sxs-lookup"><span data-stu-id="f9c77-148">SECONDARY-GIVENNAME-LIST</span></span></li>
<li><span data-ttu-id="f9c77-149">ESTADOOUPROVÍNCIA SECUNDÁRIO-LISTA</span><span class="sxs-lookup"><span data-stu-id="f9c77-149">SECONDARY-STATEORPROVINCE-LIST</span></span></li>
<li><span data-ttu-id="f9c77-150">LISTA DE ENDEREÇOS SECUNDÁRIOS</span><span class="sxs-lookup"><span data-stu-id="f9c77-150">SECONDARY-STREETNAME-LIST</span></span></li>
<li><span data-ttu-id="f9c77-151">SECUNDÁRIA-SOBRENOME-LISTA</span><span class="sxs-lookup"><span data-stu-id="f9c77-151">SECONDARY-SURNAME-LIST</span></span></li>
<li><span data-ttu-id="f9c77-152">URL SECUNDÁRIA-LISTA</span><span class="sxs-lookup"><span data-stu-id="f9c77-152">SECONDARY-URL-LIST</span></span></li>
</ul>
<span data-ttu-id="f9c77-153">Se um valor de tipo começar com o prefixo primário, o dicionário compilado, depois de instalado, substituirá o dicionário do sistema para esse idioma.</span><span class="sxs-lookup"><span data-stu-id="f9c77-153">If a type value starts with the prefix PRIMARY, the compiled dictionary, after it is installed, will replace the system dictionary for that language.</span></span> <span data-ttu-id="f9c77-154">O valor principal-DICTIONARY representa o dicionário principal do sistema para um idioma.</span><span class="sxs-lookup"><span data-stu-id="f9c77-154">The value PRIMARY-DICTIONARY represents the main system dictionary for a language.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="f9c77-155">Substituir um dicionário do sistema não faz nada para o conteúdo original do dicionário do sistema, pois a substituição estará em vigor somente até que o dicionário personalizado tenha sido removido.</span><span class="sxs-lookup"><span data-stu-id="f9c77-155">Replacing a system dictionary does nothing to the original system dictionary content, as the replacement is in effect only until the custom dictionary has been removed.</span></span>
</blockquote>
<br/> <span data-ttu-id="f9c77-156">Se um valor de tipo começar com o prefixo secundário, o dicionário compilado irá complementar o dicionário do sistema sem substituí-lo.</span><span class="sxs-lookup"><span data-stu-id="f9c77-156">If a type value starts with the prefix SECONDARY, the compiled dictionary will supplement the system dictionary without replacing it.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9c77-157">-Comentário</span><span class="sxs-lookup"><span data-stu-id="f9c77-157">-comment</span></span> <comment></td>
<td><span data-ttu-id="f9c77-158">O comentário especificado é compilado no arquivo de dicionário.</span><span class="sxs-lookup"><span data-stu-id="f9c77-158">The specified comment is compiled into the dictionary file.</span></span> <span data-ttu-id="f9c77-159">O comentário deve ser uma única cadeia de caracteres e não mais de 64 caracteres.</span><span class="sxs-lookup"><span data-stu-id="f9c77-159">The comment must be a single string and no longer than 64 characters.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9c77-160">-o <dictfile.hwrdict></span><span class="sxs-lookup"><span data-stu-id="f9c77-160">-o <dictfile.hwrdict></span></span></td>
<td><span data-ttu-id="f9c77-161">A saída é gravada no nome de arquivo especificado por <dictfile.hwrdict> .</span><span class="sxs-lookup"><span data-stu-id="f9c77-161">Output is written to the file name specified by <dictfile.hwrdict>.</span></span><br/> <span data-ttu-id="f9c77-162">Se essa opção estiver ausente, o nome do arquivo de saída será derivado do nome do arquivo de entrada original, com a extensão de arquivo de entrada substituída por. hwrdict.</span><span class="sxs-lookup"><span data-stu-id="f9c77-162">If this option is missing, the output file name is derived from the original input file name, with the input file extension replaced by .hwrdict.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="defaults"></a><span data-ttu-id="f9c77-163">Padrões</span><span class="sxs-lookup"><span data-stu-id="f9c77-163">Defaults</span></span>

<span data-ttu-id="f9c77-164">Se nenhum parâmetro for especificado, os valores de opção padrão serão</span><span class="sxs-lookup"><span data-stu-id="f9c77-164">If no parameters are specified, the default option values are</span></span>

<span data-ttu-id="f9c77-165">-lang <current input language> -tipo de dicionário secundário</span><span class="sxs-lookup"><span data-stu-id="f9c77-165">-lang <current input language> -type SECONDARY-DICTIONARY</span></span>

### <a name="examples"></a><span data-ttu-id="f9c77-166">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f9c77-166">Examples</span></span>

<span data-ttu-id="f9c77-167">O seguinte compila o arquivo de entrada mylist1.txt, aplica os valores de opção padrão e cria o arquivo de saída mylist1. hwrdict.</span><span class="sxs-lookup"><span data-stu-id="f9c77-167">The following compiles the input file mylist1.txt, applies the default option values, and creates the output file mylist1.hwrdict.</span></span>

``` syntax
hwrcomp mylist1.txt
```

<span data-ttu-id="f9c77-168">Por outro lado, o seguinte compila mylist1.txt em myrsrc1. hwrdict, mas atribui "Inglês (EUA)" (en-US) como o idioma e o dicionário secundário como o tipo.</span><span class="sxs-lookup"><span data-stu-id="f9c77-168">In contrast, the following compiles mylist1.txt into myrsrc1.hwrdict, but assigns "English (US)" (en-US) as the language and SECONDARY-DICTIONARY as the type.</span></span>

``` syntax
hwrcomp -lang en-US -type SECONDARY-DICTIONARY -o myrsrc1 mylist1.txt 
```

## <a name="installing-a-compiled-custom-dictionary"></a><span data-ttu-id="f9c77-169">Instalando um dicionário personalizado compilado</span><span class="sxs-lookup"><span data-stu-id="f9c77-169">Installing a Compiled Custom Dictionary</span></span>

<span data-ttu-id="f9c77-170">HwrComp.exe cria um arquivo. hwrdict, que está em um formato binário utilizável por um reconhecedor de manuscrito.</span><span class="sxs-lookup"><span data-stu-id="f9c77-170">HwrComp.exe creates a .hwrdict file, which is in a binary format usable by a handwriting recognizer.</span></span> <span data-ttu-id="f9c77-171">Esse arquivo pode ser instalado em qualquer computador que esteja executando o Windows 7 ou o Windows Server 2008 R2 que dê suporte ao reconhecimento de manuscrito.</span><span class="sxs-lookup"><span data-stu-id="f9c77-171">This file can be installed on any computer running Windows 7 or Windows Server 2008 R2 that supports handwriting recognition.</span></span> <span data-ttu-id="f9c77-172">Um dicionário é instalado apenas para o usuário atual ou para todos os usuários em um computador.</span><span class="sxs-lookup"><span data-stu-id="f9c77-172">A dictionary is installed either for just the current user or for all users on a machine.</span></span>

<span data-ttu-id="f9c77-173">Um arquivo de dicionário personalizado compilado pode ser instalado a partir da linha de comando usando a ferramenta HwrReg.exe.</span><span class="sxs-lookup"><span data-stu-id="f9c77-173">A compiled custom dictionary file can be installed from the command line using the tool HwrReg.exe.</span></span> <span data-ttu-id="f9c77-174">Essa ferramenta é útil se você deseja substituir alguns dos valores de configuração que são compilados no arquivo ou são os valores padrão.</span><span class="sxs-lookup"><span data-stu-id="f9c77-174">This tool is useful if you wish to override some of the configuration values that either are compiled into the file or are the default values.</span></span> <span data-ttu-id="f9c77-175">Há duas maneiras de executar HwrReg.exe: no modo de verificação/instalação e no modo de lista/remoção.</span><span class="sxs-lookup"><span data-stu-id="f9c77-175">There are two ways to run HwrReg.exe: in check/install mode and in list/remove mode.</span></span>

### <a name="running-hwrregexe-in-checkinstall-mode"></a><span data-ttu-id="f9c77-176">Executando HwrReg.exe no modo de verificação/instalação</span><span class="sxs-lookup"><span data-stu-id="f9c77-176">Running HwrReg.exe in Check/Install Mode</span></span>

<span data-ttu-id="f9c77-177">Esse modo é para arquivos de dicionário personalizados que ainda não foram instalados.</span><span class="sxs-lookup"><span data-stu-id="f9c77-177">This mode is for custom dictionary files that have not yet been installed.</span></span> <span data-ttu-id="f9c77-178">O seguinte mostra a sintaxe de uso para as opções de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="f9c77-178">The following shows the usage syntax for the command-line options.</span></span>

``` syntax
Usage: hwrreg        [-check]
    [-lang <localename>] 
    [-scope {all|me}]
    [-noprompt] 
    <dictfile.hwrdict>
```

### <a name="explanation-of-options"></a><span data-ttu-id="f9c77-179">Explicação das opções</span><span class="sxs-lookup"><span data-stu-id="f9c77-179">Explanation of Options</span></span>



| <span data-ttu-id="f9c77-180">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="f9c77-180">Parameter</span></span>                | <span data-ttu-id="f9c77-181">Descrição</span><span class="sxs-lookup"><span data-stu-id="f9c77-181">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                        |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9c77-182">-verificar</span><span class="sxs-lookup"><span data-stu-id="f9c77-182">-check</span></span>                   | <span data-ttu-id="f9c77-183">O arquivo de dicionário é verificado sem ser instalado.</span><span class="sxs-lookup"><span data-stu-id="f9c77-183">The dictionary file is verified without being installed.</span></span> <span data-ttu-id="f9c77-184">A opção verificar exibe o comentário do arquivo, além das informações de registro que seriam usadas para instalar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="f9c77-184">The  check option displays the file's comment, plus the registration information that would be used to install the file.</span></span> <span data-ttu-id="f9c77-185">Essa opção é útil para verificar as informações de registro antes da execução da instalação.</span><span class="sxs-lookup"><span data-stu-id="f9c77-185">This option is useful for verifying registration information before the installation is performed.</span></span> <br/> <span data-ttu-id="f9c77-186">Se essa opção estiver ausente, HwrReg.exe instalará o dicionário personalizado.</span><span class="sxs-lookup"><span data-stu-id="f9c77-186">If this option is missing, HwrReg.exe installs the custom dictionary.</span></span><br/>  |
|  <span data-ttu-id="f9c77-187">lang <localename></span><span class="sxs-lookup"><span data-stu-id="f9c77-187">lang <localename></span></span> | <span data-ttu-id="f9c77-188">O arquivo de dicionário é verificado sem ser instalado.</span><span class="sxs-lookup"><span data-stu-id="f9c77-188">The dictionary file is verified without being installed.</span></span> <span data-ttu-id="f9c77-189">A opção verificar exibe o comentário do arquivo, além das informações de registro que seriam usadas para instalar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="f9c77-189">The  check option displays the file's comment, plus the registration information that would be used to install the file.</span></span> <span data-ttu-id="f9c77-190">Essa opção é útil para verificar as informações de registro antes da execução da instalação.</span><span class="sxs-lookup"><span data-stu-id="f9c77-190">This option is useful for verifying registration information before the installation is performed.</span></span> <br/> <span data-ttu-id="f9c77-191">Se essa opção estiver ausente, HwrReg.exe instalará o dicionário personalizado.</span><span class="sxs-lookup"><span data-stu-id="f9c77-191">If this option is missing, HwrReg.exe installs the custom dictionary.</span></span> <br/> |
|  <span data-ttu-id="f9c77-192">escopo {todos \| me}</span><span class="sxs-lookup"><span data-stu-id="f9c77-192">scope {all\|me}</span></span>         | <span data-ttu-id="f9c77-193">O dicionário personalizado é instalado para todos os usuários (escopo todos) ou apenas para o usuário atual (escopo me).</span><span class="sxs-lookup"><span data-stu-id="f9c77-193">The custom dictionary is installed either for all users ( scope all) or for just the current user ( scope me).</span></span> <span data-ttu-id="f9c77-194">A instalação com escopo todos requer que o comando seja executado em um prompt de comando com privilégios elevados; caso contrário, um código de erro será retornado.</span><span class="sxs-lookup"><span data-stu-id="f9c77-194">Installing with  scope all requires the command to be run in an elevated command prompt; otherwise, an error code will be returned.</span></span> <br/> <span data-ttu-id="f9c77-195">Se essa opção estiver ausente, a instalação será delimitada apenas ao usuário atual.</span><span class="sxs-lookup"><span data-stu-id="f9c77-195">If this option is missing, the installation is scoped to just the current user.</span></span><br/>                          |
|  <span data-ttu-id="f9c77-196">noprompt</span><span class="sxs-lookup"><span data-stu-id="f9c77-196">noprompt</span></span>                | <span data-ttu-id="f9c77-197">HwrReg.exe não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="f9c77-197">HwrReg.exe does not prompt for confirmation.</span></span> <span data-ttu-id="f9c77-198">Isso pode ser útil ao executar hwrReg.exe de um script.</span><span class="sxs-lookup"><span data-stu-id="f9c77-198">This can be useful when running hwrReg.exe from a script.</span></span> <br/>                                                                                                                                                                                                                                                                 |



 

<span data-ttu-id="f9c77-199">O exemplo a seguir instala o dicionário personalizado myrsrc1. hwrdict para a linguagem "dinamarquês (Dinamarca)" (da DK), com o escopo padrão apenas do usuário atual.</span><span class="sxs-lookup"><span data-stu-id="f9c77-199">The following example installs the custom dictionary myrsrc1.hwrdict for language "Danish (Denmark)" (da DK), with the default scope of just the current user.</span></span>

``` syntax
hwrreg -lang da-DK myrsrc1.hwrdict 
```

### <a name="running-hwrregexe-in-listremove-mode"></a><span data-ttu-id="f9c77-200">Executando HwrReg.exe no modo de lista/remoção</span><span class="sxs-lookup"><span data-stu-id="f9c77-200">Running HwrReg.exe in List/Remove Mode</span></span>

<span data-ttu-id="f9c77-201">Esse modo lista ou remove os dicionários personalizados instalados.</span><span class="sxs-lookup"><span data-stu-id="f9c77-201">This mode either lists or removes installed custom dictionaries.</span></span> <span data-ttu-id="f9c77-202">O seguinte mostra a sintaxe de uso para as opções de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="f9c77-202">The following shows the usage syntax for the command-line options.</span></span>

``` syntax
Usage: hwrreg        [-lang <localename>] 
    [-scope {all|me}] 
    [-type <type>]
    -list | -remove
```

### <a name="explanation-of-options"></a><span data-ttu-id="f9c77-203">Explicação das opções</span><span class="sxs-lookup"><span data-stu-id="f9c77-203">Explanation of Options</span></span>



| <span data-ttu-id="f9c77-204">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="f9c77-204">Parameter</span></span>                | <span data-ttu-id="f9c77-205">Descrição</span><span class="sxs-lookup"><span data-stu-id="f9c77-205">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  <span data-ttu-id="f9c77-206">lang <localename></span><span class="sxs-lookup"><span data-stu-id="f9c77-206">lang <localename></span></span> | <span data-ttu-id="f9c77-207">Os dicionários registrados somente para esse nome de localidade são listados ou removidos.</span><span class="sxs-lookup"><span data-stu-id="f9c77-207">The dictionaries registered for only this locale name are listed or removed.</span></span> <span data-ttu-id="f9c77-208">O argumento <localename> tem a região de idioma do formulário.</span><span class="sxs-lookup"><span data-stu-id="f9c77-208">The argument <localename> has the form language REGION.</span></span> <span data-ttu-id="f9c77-209">Para obter exemplos desse formulário, consulte [constantes e cadeias de caracteres de identificador de linguagem](/windows/desktop/Intl/language-identifier-constants-and-strings).</span><span class="sxs-lookup"><span data-stu-id="f9c77-209">For examples of this form, see [Language Identifier Constants and Strings](/windows/desktop/Intl/language-identifier-constants-and-strings).</span></span> <br/> <span data-ttu-id="f9c77-210">Se essa opção estiver ausente, os dicionários para todos os idiomas serão listados ou removidos.</span><span class="sxs-lookup"><span data-stu-id="f9c77-210">If this option is missing, dictionaries for all languages are listed or removed.</span></span><br/> |
|  <span data-ttu-id="f9c77-211">escopo {todos \| me}</span><span class="sxs-lookup"><span data-stu-id="f9c77-211">scope {all\|me}</span></span>         | <span data-ttu-id="f9c77-212">O dicionário personalizado é instalado para todos os usuários (escopo todos) ou apenas para o usuário atual (escopo me).</span><span class="sxs-lookup"><span data-stu-id="f9c77-212">The custom dictionary is installed either for all users ( scope all) or for just the current user ( scope me).</span></span> <span data-ttu-id="f9c77-213">A instalação com escopo todos requer que o comando seja executado em um prompt de comando com privilégios elevados; caso contrário, um código de erro será retornado.</span><span class="sxs-lookup"><span data-stu-id="f9c77-213">Installing with  scope all requires the command to be run in an elevated command prompt; otherwise, an error code will be returned.</span></span> <br/> <span data-ttu-id="f9c77-214">Se essa opção estiver ausente, a instalação será delimitada apenas ao usuário atual.</span><span class="sxs-lookup"><span data-stu-id="f9c77-214">If this option is missing, the installation is scoped to just the current user.</span></span><br/>                      |
|  <span data-ttu-id="f9c77-215">Escreva <type></span><span class="sxs-lookup"><span data-stu-id="f9c77-215">type <type></span></span>       | <span data-ttu-id="f9c77-216">Lista ou remove somente os dicionários que são registrados com o tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="f9c77-216">Lists or removes only dictionaries that are registered with the specified type.</span></span><br/> <span data-ttu-id="f9c77-217">Se essa opção estiver ausente, todos os tipos de dicionário serão listados ou removidos.</span><span class="sxs-lookup"><span data-stu-id="f9c77-217">If this option is missing, all dictionary types are listed or removed.</span></span> <span data-ttu-id="f9c77-218">Instalar ou remover um dicionário personalizado de outro tipo (como a lista de PAÍSname primário) pode afetar o reconhecimento de manuscrito em outros contextos.</span><span class="sxs-lookup"><span data-stu-id="f9c77-218">Installing or removing a custom dictionary of another type (such as PRIMARY-COUNTRYNAME-LIST) may affect handwriting recognition in other contexts.</span></span> <br/>                                              |
|  <span data-ttu-id="f9c77-219">list</span><span class="sxs-lookup"><span data-stu-id="f9c77-219">list</span></span>                    | <span data-ttu-id="f9c77-220">Lista todos os dicionários instalados que correspondem às outras opções.</span><span class="sxs-lookup"><span data-stu-id="f9c77-220">Lists all installed dictionaries that match the other options.</span></span><br/> <span data-ttu-id="f9c77-221">Se essa opção estiver ausente, a opção remover deverá ser especificada.</span><span class="sxs-lookup"><span data-stu-id="f9c77-221">If this option is missing, the option  remove must be specified.</span></span><br/>                                                                                                                                                                                                                          |
|  <span data-ttu-id="f9c77-222">remove</span><span class="sxs-lookup"><span data-stu-id="f9c77-222">remove</span></span>                  | <span data-ttu-id="f9c77-223">Solicita a remoção de qualquer dicionário que corresponda às outras opções.</span><span class="sxs-lookup"><span data-stu-id="f9c77-223">Prompts for removal of any dictionary that matches the other options.</span></span><br/> <span data-ttu-id="f9c77-224">Se essa opção estiver ausente, a lista de opções deverá ser especificada.</span><span class="sxs-lookup"><span data-stu-id="f9c77-224">If this option is missing, the option  list must be specified.</span></span><br/>                                                                                                                                                                                                                     |



 

### <a name="examples"></a><span data-ttu-id="f9c77-225">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f9c77-225">Examples</span></span>

<span data-ttu-id="f9c77-226">O seguinte lista os dicionários que têm o idioma "Inglês (EUA)" (en US) e o dicionário principal do tipo e que são instalados apenas para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="f9c77-226">The following lists dictionaries that have language "English (US)" (en US) and type PRIMARY DICTIONARY and that are installed for just the current user.</span></span>

``` syntax
hwrreg -list -lang en-US -type PRIMARY-DICTIONARY
                  
```

<span data-ttu-id="f9c77-227">Da mesma forma, o seguinte remove os dicionários que correspondem aos mesmos critérios.</span><span class="sxs-lookup"><span data-stu-id="f9c77-227">Similarly, the following removes dictionaries that match the same criteria.</span></span>

``` syntax
hwrreg -remove -lang en-US -type PRIMARY-DICTIONARY
                  
```

## <a name="general-notes-on-custom-dictionaries"></a><span data-ttu-id="f9c77-228">Observações gerais sobre dicionários personalizados</span><span class="sxs-lookup"><span data-stu-id="f9c77-228">General Notes on Custom Dictionaries</span></span>

-   <span data-ttu-id="f9c77-229">Se você instalar dois dicionários personalizados que têm o mesmo tipo, idioma e escopo, a segunda instalação substituirá o primeiro.</span><span class="sxs-lookup"><span data-stu-id="f9c77-229">If you install two custom dictionaries that have the same type, language, and scope, the second installation will overwrite the first.</span></span>
-   <span data-ttu-id="f9c77-230">Se você instalar dois dicionários personalizados com o mesmo tipo e idioma, mas com escopos diferentes (um para todos os usuários e outro para o usuário atual), o dicionário instalado para o usuário atual terá precedência e o dicionário instalado para todos os usuários será ignorado.</span><span class="sxs-lookup"><span data-stu-id="f9c77-230">If you install two custom dictionaries with the same type and language, but with different scopes (one for all users, and one for the current user), the dictionary installed for the current user takes precedence, and the dictionary installed for all users is ignored.</span></span>

 

