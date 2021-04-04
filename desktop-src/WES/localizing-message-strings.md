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
# <a name="localizing-message-strings"></a>Localizando cadeias de caracteres de mensagem

Cada cadeia de caracteres de mensagem especificada no manifesto deve fazer referência a uma cadeia de caracteres na seção **localização** do manifesto. A seção de localização contém uma seção de tabela de cadeia de caracteres para cada localidade que você dá suporte.

O exemplo a seguir mostra como definir uma tabela de cadeia de caracteres. Você deve especificar os atributos de **ID** e **valor** da cadeia de caracteres. Use o valor do atributo **ID** para fazer referência à cadeia de caracteres no seu manifesto. O atributo **Value** contém a cadeia de caracteres localizada.


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


Em vez de adicionar cadeias de caracteres localizadas ao manifesto, você deve criar um arquivo MUI (Multilingual User interface) para cada idioma ao qual dá suporte. Use um arquivo de texto de mensagem para especificar suas cadeias de caracteres localizadas.

O procedimento a seguir descreve como criar um arquivo MUI para inglês e francês.

**Para criar um arquivo MUI para inglês e francês**

1.  Crie um arquivo de texto de mensagem que cria as cadeias de caracteres de mensagem francesa. Para obter detalhes sobre como criar um arquivo de texto de mensagem, consulte [arquivos de texto da mensagem](/windows/desktop/EventLog/message-text-files). Os identificadores de mensagem que você especificar no arquivo de texto de mensagem devem corresponder aos identificadores de recurso que o compilador de mensagem gerou para as mesmas cadeias de caracteres no manifesto. Para determinar os identificadores de recurso usados para as cadeias de caracteres no manifesto, consulte o arquivo. h que o compilador de mensagem gerou quando você compilou o manifesto.
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


2.  Execute os comandos a seguir para criar a DLL de recursos que contém suas cadeias de caracteres localizadas. O arquivo messages.mc é o arquivo de texto de mensagem que você criou na etapa 1.
    ```cmd
    mc -u -U messages.mc

    rc -r messages.rc

    link -dll -noentry -out:messages.dll messages.res
    ```

    

3.  Na pasta que contém seu provedor, crie uma subpasta para cada localidade com suporte. O nome da subpasta deve ser o nome do idioma para essa localidade. Por exemplo, para 0x0409, use en-US como o nome da pasta.
4.  Crie um arquivo. rcconfig que informe à ferramenta de Muirct.exe que você deseja dividir os recursos de cadeia de caracteres de mensagem do executável e das DLLs de recurso. Veja a seguir um exemplo de arquivo. rcconfig.
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
  

5.  Execute os comandos de Muirct.exe a seguir para dividir as cadeias de caracteres em inglês do arquivo executável do provedor.
    ```cmd
    muirct -q split.rcconfig -v 2 -x 0x0409 -g 0x0409 provider.exe provider.exe.ln en-US\provider.exe.mui

    muirct -c provider.exe.ln -e en-US\provider.exe.mui
    ```
 

6.  Execute os seguintes comandos de Muirct.exe para dividir as cadeias de caracteres francesas da DLL de recursos. Remova o arquivo de idioma neutro (fr-FR \\messages.dll) depois que o arquivo MUI for criado.
    ```cmd
    muirct -q split.rcconfig -v 2 -x 0x040C -g 0x0409 messages.dll fr-FR\messages.dll fr-FR\provider.exe.mui

    muirct -c provider.exe.ln -e fr-FR\provider.exe.mui
    ```
  

7.  Renomeie provider.exe. ln para provider.exe.