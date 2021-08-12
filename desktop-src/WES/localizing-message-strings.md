---
title: Localizando cadeias de caracteres de mensagem
description: Cada cadeia de caracteres de mensagem especificada no manifesto deve referenciar uma cadeia de caracteres na seção de localização do manifesto.
ms.assetid: aeae9ef6-6ef7-46f5-a9ab-fabe418549b2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b55b94ea8e8a40de1401cf3aba97488d5531a77b441361e38f1ff98219940afc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118587894"
---
# <a name="localizing-message-strings"></a>Localizando cadeias de caracteres de mensagem

Cada cadeia de caracteres de mensagem especificada no manifesto deve referenciar uma cadeia de caracteres na **seção de localização** do manifesto. A seção localização contém uma seção de tabela de cadeia de caracteres para cada localidade que você suporta.

O exemplo a seguir mostra como definir uma tabela de cadeia de caracteres. Você deve especificar a **ID** da cadeia de caracteres e os **atributos de** valor. Use o valor do atributo **id** para referenciar a cadeia de caracteres em seu manifesto. O **atributo value** contém a cadeia de caracteres localizada.


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="http://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="http://www.w3.org/2001/XMLSchema"
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


Em vez de adicionar cadeias de caracteres localizadas ao manifesto, você deve criar um arquivo MUI (interface do usuário multilíngue) para cada idioma que você suporta. Use um arquivo de texto de mensagem para especificar suas cadeias de caracteres localizadas.

O procedimento a seguir descreve como criar um arquivo MUI para inglês e francês.

**Para criar um arquivo MUI para inglês e francês**

1.  Crie um arquivo de texto de mensagem que cria as cadeias de caracteres de mensagem em francês. Para obter detalhes sobre como criar um arquivo de texto de mensagem, consulte [Arquivos de Texto da Mensagem](/windows/desktop/EventLog/message-text-files). Os identificadores de mensagem especificados no arquivo de texto da mensagem devem corresponder aos identificadores de recurso que o compilador de mensagem gerou para as mesmas cadeias de caracteres no manifesto. Para determinar os identificadores de recurso usados para as cadeias de caracteres no manifesto, consulte o arquivo .h que o compilador de mensagem gerou quando você compilou o manifesto.
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


2.  Execute os comandos a seguir para criar a DLL de recurso que contém suas cadeias de caracteres localizadas. O messages.mc arquivo é o arquivo de texto da mensagem que você criou na etapa 1.
    ```cmd
    mc -u -U messages.mc

    rc -r messages.rc

    link -dll -noentry -out:messages.dll messages.res
    ```

    

3.  Na pasta que contém seu provedor, crie uma subpasta para cada localidade à sua suporte. O nome da subpasta deve ser o nome do idioma dessa localidade. Por exemplo, por 0x0409, use en-US como o nome da pasta.
4.  Crie um arquivo .rcconfig que informa à Muirct.exe que você deseja dividir os recursos da cadeia de caracteres de mensagem do executável e das DLLs de recurso. A seguir está um arquivo .rcconfig de exemplo.
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
  

5.  Execute os seguintes Muirct.exe para dividir as cadeias de caracteres em inglês do arquivo executável do provedor.
    ```cmd
    muirct -q split.rcconfig -v 2 -x 0x0409 -g 0x0409 provider.exe provider.exe.ln en-US\provider.exe.mui

    muirct -c provider.exe.ln -e en-US\provider.exe.mui
    ```
 

6.  Execute os comandos Muirct.exe a seguir para dividir as cadeias de caracteres em francês da DLL do recurso. Remova o arquivo neutro de idioma (fr-FR \\messages.dll) depois que o arquivo MUI for criado.
    ```cmd
    muirct -q split.rcconfig -v 2 -x 0x040C -g 0x0409 messages.dll fr-FR\messages.dll fr-FR\provider.exe.mui

    muirct -c provider.exe.ln -e fr-FR\provider.exe.mui
    ```
  

7.  Renomeie provider.exe.ln para provider.exe.
