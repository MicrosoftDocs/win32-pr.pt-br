---
title: Localizando cadeias de caracteres de mensagem
description: Cada cadeia de caracteres de mensagem especificada no manifesto deve fazer referência a uma cadeia de caracteres na seção localização do manifesto.
ms.assetid: aeae9ef6-6ef7-46f5-a9ab-fabe418549b2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7812aed8bf376994a2cbecfa5997737d9740ec1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007849"
---
# <a name="localizing-message-strings"></a><span data-ttu-id="6cbfe-103">Localizando cadeias de caracteres de mensagem</span><span class="sxs-lookup"><span data-stu-id="6cbfe-103">Localizing Message Strings</span></span>

<span data-ttu-id="6cbfe-104">Cada cadeia de caracteres de mensagem especificada no manifesto deve fazer referência a uma cadeia de caracteres na seção **localização** do manifesto.</span><span class="sxs-lookup"><span data-stu-id="6cbfe-104">Each message string that you specify in the manifest must reference a string in the **localization** section of the manifest.</span></span> <span data-ttu-id="6cbfe-105">A seção de localização contém uma seção de tabela de cadeia de caracteres para cada localidade que você dá suporte.</span><span class="sxs-lookup"><span data-stu-id="6cbfe-105">The localization section contains a string table section for each locale that you support.</span></span>

<span data-ttu-id="6cbfe-106">O exemplo a seguir mostra como definir uma tabela de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="6cbfe-106">The following example shows how to define a string table.</span></span> <span data-ttu-id="6cbfe-107">Você deve especificar os atributos de **ID** e **valor** da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="6cbfe-107">You must specify the string's **id** and **value** attributes.</span></span> <span data-ttu-id="6cbfe-108">Use o valor do atributo **ID** para fazer referência à cadeia de caracteres no seu manifesto.</span><span class="sxs-lookup"><span data-stu-id="6cbfe-108">You use the value of the **id** attribute to reference the string in your manifest.</span></span> <span data-ttu-id="6cbfe-109">O atributo **Value** contém a cadeia de caracteres localizada.</span><span class="sxs-lookup"><span data-stu-id="6cbfe-109">The **value** attribute contains the localized string.</span></span>


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="https://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="https://www.w3.org/2001/XMLSchema"    
    >

    <instrumentation>
        <events>
            <provider name="Microsoft-Windows-SampleProvider" 
                guid="{1db28f2e-8f80-4027-8c5a-a11f7f10f62d}" 
                symbol="PROVIDER_GUID" 
                resourceFileName="<path to the exe or dll that contains the metadata resources>" 
                messageFileName="<path to the exe or dll that contains the string resources>"
                message="$(string.ProviderName)">

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="ProviderName" value="Sample Provider"/>
                <string id="PathNotFound" value="The path %1 was not found."/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```


<span data-ttu-id="6cbfe-110">Em vez de adicionar cadeias de caracteres localizadas ao manifesto, você deve criar um arquivo MUI (Multilingual User interface) para cada idioma ao qual dá suporte.</span><span class="sxs-lookup"><span data-stu-id="6cbfe-110">Instead of adding localized strings to the manifest, you should create a multilingual user interface (MUI) file for each language that you support.</span></span> <span data-ttu-id="6cbfe-111">Use um arquivo de texto de mensagem para especificar suas cadeias de caracteres localizadas.</span><span class="sxs-lookup"><span data-stu-id="6cbfe-111">Use a message text file to specify your localized strings.</span></span>

<span data-ttu-id="6cbfe-112">O procedimento a seguir descreve como criar um arquivo MUI para inglês e francês.</span><span class="sxs-lookup"><span data-stu-id="6cbfe-112">The following procedure describes how to create a MUI file for English and French.</span></span>

<span data-ttu-id="6cbfe-113">**Para criar um arquivo MUI para inglês e francês**</span><span class="sxs-lookup"><span data-stu-id="6cbfe-113">**To create a MUI file for English and French**</span></span>

1.  <span data-ttu-id="6cbfe-114">Crie um arquivo de texto de mensagem que cria as cadeias de caracteres de mensagem francesa.</span><span class="sxs-lookup"><span data-stu-id="6cbfe-114">Create a message text file that creates the French message strings.</span></span> <span data-ttu-id="6cbfe-115">Para obter detalhes sobre como criar um arquivo de texto de mensagem, consulte [arquivos de texto da mensagem](/windows/desktop/EventLog/message-text-files).</span><span class="sxs-lookup"><span data-stu-id="6cbfe-115">For details on creating a message text file, see [Message Text Files](/windows/desktop/EventLog/message-text-files).</span></span> <span data-ttu-id="6cbfe-116">Os identificadores de mensagem que você especificar no arquivo de texto de mensagem devem corresponder aos identificadores de recurso que o compilador de mensagem gerou para as mesmas cadeias de caracteres no manifesto.</span><span class="sxs-lookup"><span data-stu-id="6cbfe-116">The message identifiers that you specify in the message text file must match the resource identifiers that the message compiler generated for the same strings in the manifest.</span></span> <span data-ttu-id="6cbfe-117">Para determinar os identificadores de recurso usados para as cadeias de caracteres no manifesto, consulte o arquivo. h que o compilador de mensagem gerou quando você compilou o manifesto.</span><span class="sxs-lookup"><span data-stu-id="6cbfe-117">To determine the resource identifiers used for the strings in the manifest, see the .h file that the message compiler generated when you compiled the manifest.</span></span>
    ```Text
    LanguageNames=(French=0x40C:MSG0040C)

    ; // The following are message definitions.

    MessageId=0x00000065
    SymbolicName=MSG_ProviderName
    Language=French
    <FRENCH STRING GOES HERE>
    .


    MessageId=0x00000066
    SymbolicName=MSG_PathNotFound
    Language=French
    <FRENCH STRING GOES HERE>
    .
    
    ```


2.  <span data-ttu-id="6cbfe-118">Execute os comandos a seguir para criar a DLL de recursos que contém suas cadeias de caracteres localizadas.</span><span class="sxs-lookup"><span data-stu-id="6cbfe-118">Run the following commands to create the resource DLL that contains your localized strings.</span></span> <span data-ttu-id="6cbfe-119">O arquivo messages.mc é o arquivo de texto de mensagem que você criou na etapa 1.</span><span class="sxs-lookup"><span data-stu-id="6cbfe-119">The messages.mc file is the message text file that you created in step 1.</span></span>
    ```cmd
    mc -u -U messages.mc

    rc -r messages.rc

    link -dll -noentry -out:messages.dll messages.res
    ```

    

3.  <span data-ttu-id="6cbfe-120">Na pasta que contém seu provedor, crie uma subpasta para cada localidade com suporte.</span><span class="sxs-lookup"><span data-stu-id="6cbfe-120">In the folder that contains your provider, create a subfolder for each locale that you support.</span></span> <span data-ttu-id="6cbfe-121">O nome da subpasta deve ser o nome do idioma para essa localidade.</span><span class="sxs-lookup"><span data-stu-id="6cbfe-121">The name of the subfolder must be the language name for that locale.</span></span> <span data-ttu-id="6cbfe-122">Por exemplo, para 0x0409, use en-US como o nome da pasta.</span><span class="sxs-lookup"><span data-stu-id="6cbfe-122">For example, for 0x0409, use en-US as the folder name.</span></span>
4.  <span data-ttu-id="6cbfe-123">Crie um arquivo. rcconfig que informe à ferramenta de Muirct.exe que você deseja dividir os recursos de cadeia de caracteres de mensagem do executável e das DLLs de recurso.</span><span class="sxs-lookup"><span data-stu-id="6cbfe-123">Create a .rcconfig file that tells the Muirct.exe tool that you want to split the message string resources from the executable and the resource DLLs.</span></span> <span data-ttu-id="6cbfe-124">Veja a seguir um exemplo de arquivo. rcconfig.</span><span class="sxs-lookup"><span data-stu-id="6cbfe-124">The following is an example .rcconfig file.</span></span>
    ```XML
    <localization>
          <resources>
                <win32Resources fileType="Application">
                      <neutralResources>
                      </neutralResources>
                      <localizedResources>
                            <resourceType typeNameId="#11"/>
                      </localizedResources>
                </win32Resources>
          </resources>
    </localization>
    ```
  

5.  <span data-ttu-id="6cbfe-125">Execute os comandos de Muirct.exe a seguir para dividir as cadeias de caracteres em inglês do arquivo executável do provedor.</span><span class="sxs-lookup"><span data-stu-id="6cbfe-125">Run the following Muirct.exe commands to split the English strings from the provider executable file.</span></span>
    ```cmd
    muirct -q split.rcconfig -v 2 -x 0x0409 -g 0x0409 provider.exe provider.exe.ln en-US\provider.exe.mui

    muirct -c provider.exe.ln -e en-US\provider.exe.mui
    ```
 

6.  <span data-ttu-id="6cbfe-126">Execute os seguintes comandos de Muirct.exe para dividir as cadeias de caracteres francesas da DLL de recursos.</span><span class="sxs-lookup"><span data-stu-id="6cbfe-126">Run the following Muirct.exe commands to split the French strings from the resource DLL.</span></span> <span data-ttu-id="6cbfe-127">Remova o arquivo de idioma neutro (fr-FR \\messages.dll) depois que o arquivo MUI for criado.</span><span class="sxs-lookup"><span data-stu-id="6cbfe-127">Remove the language neutral file (fr-FR\\messages.dll) after the MUI file is created.</span></span>
    ```cmd
    muirct -q split.rcconfig -v 2 -x 0x040C -g 0x0409 messages.dll fr-FR\messages.dll fr-FR\provider.exe.mui

    muirct -c provider.exe.ln -e fr-FR\provider.exe.mui
    ```
  

7.  <span data-ttu-id="6cbfe-128">Renomeie provider.exe. ln para provider.exe.</span><span class="sxs-lookup"><span data-stu-id="6cbfe-128">Rename provider.exe.ln to provider.exe.</span></span>