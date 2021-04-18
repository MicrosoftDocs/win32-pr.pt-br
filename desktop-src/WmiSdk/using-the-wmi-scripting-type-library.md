---
description: Você pode usar a biblioteca de tipos de script do WMI para chamar métodos de API de script do WMI de Microsoft Visual Studio e em arquivos WSF do host de script do Windows.
ms.assetid: 6ef4e210-0733-4f2a-89c1-1a7aca5a19d9
ms.tgt_platform: multiple
title: Usando a biblioteca de tipos de script WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8ba419d9a9b676d798b97e3b1a57f4e038d97814
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105807803"
---
# <a name="using-the-wmi-scripting-type-library"></a>Usando a biblioteca de tipos de script WMI

Você pode usar a biblioteca de tipos de script do WMI para chamar métodos de API de script do WMI de Microsoft Visual Studio e em arquivos WSF do host de script do Windows.

## <a name="using-the-wmi-scripting-type-library-with-microsoft-visual-studio"></a>Usando a biblioteca de tipos de script WMI com Microsoft Visual Studio

> [!Note]  
> Os recursos do Visual InterDev 6,0 foram integrados ao [Microsoft Visual Studio .net](https://msdn.microsoft.com/vstudio/default.aspx).

 

O procedimento a seguir descreve como habilitar o IDE (ambiente de desenvolvimento integrado) para estar ciente da biblioteca de tipos WbemScripting.

**Para adicionar a biblioteca de tipos de script WMI às referências do projeto**

1.  Selecione **Adicionar referências** no menu **projeto** .
2.  Na guia COM da caixa **Adicionar referência** , selecione biblioteca de script do Microsoft WMI v 1.2.
3.  Se nenhuma opção adequada aparecer na lista de referências, adicione-a usando **procurar** na caixa **referências** . A **procura** abre uma caixa **Adicionar referência** que permite que você localize a biblioteca de tipos WbemScripting.

    A biblioteca de tipos WbemScripting reside no arquivo Wbemdisp. tlb no diretório% windir% \\ System32 \\ WBEM.

4.  Selecione o arquivo e clique em **Abrir**. A biblioteca de scripts do Microsoft WMI V 1.2 aparece na lista de referências. Certifique-se de selecionar a caixa ao lado desse item na lista.

## <a name="using-the-wmi-scripting-type-library-with-windows-script-host-20"></a>Usando a biblioteca de tipos de script do WMI com o Windows Script Host 2,0

Você pode incluir a referência ao **WbemScripting. SWbemLocator** em um arquivo wsf do host de script do Windows, ao contrário de um script escrito em Visual Basic, Scripting Edition ou outras linguagens de script. Isso permite que você use nomes constantes em vez de valores. Por exemplo, use **WbemAuthenticationLevelPktPrivacy** em vez do valor 6 ao definir a autenticação.

Os scripts podem se conectar à API de script para a biblioteca de tipos do WMI usando os seguintes métodos:

-   Especificar o GUID WbemScripting nos métodos do VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) e [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx).

    Isso alerta o host de scripts do Windows para se conectar ao conjunto de objetos WMI.

    O exemplo de código VBScript a seguir cria um novo objeto [**SWbemDateTime**](swbemdatetime.md) .

    ```VB
    Set dateTime = CreateObject("WbemScripting.SWbemDateTime")
    ```

    

-   Usando a [cadeia de caracteres do moniker](constructing-a-moniker-string.md) "winmgmts:" ao obter um objeto novo ou existente.

    O exemplo de código VBScript a seguir usa o moniker "winmgmts:" para obter a instância do [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process) com uma propriedade **Handle** de 0 (zero). **Handle** é a propriedade de chave para essa classe.

    ```VB
    Set Process = GetObject("winmgmts:Win32_Process.Handle=0")
    ```

    

-   Referenciando a biblioteca de tipos WMI usando a <reference> marca do formato de arquivo XML do WSH 2,0. Se você usar a <reference> marca, a marca deverá ter um atributo **UUID** cujo valor é o **GUID** da biblioteca de tipos WMI ou (recomendado) um atributo Object cujo valor é o **ProgID** de qualquer um dos objetos de script WMI que você pode criar.

    O exemplo de código VBScript a seguir usa o PROGID de "WbemScripting". Para executar o script, salve o texto em um arquivo com uma extensão. wsf.

    ```VB
    <?xml version="1.0" encoding="US-ASCII"?>
    <job>
    <reference object="WbemScripting.SWbemLocator"/>
    <script language="VBScript">
        set service = GetObject("winmgmts:")
        ' Following line uses a symbolic 
        ' constant from the WMI type library
        service.Security_.impersonationLevel = _
            wbemImpersonationLevelDelegate
    </script>
    </job>
    ```

    

-   Usando um **objeto** <> marca para criar um objeto de script WMI. Você pode especificar o atributo **ID** com o valor de um nome que faz referência ao objeto de script WMI que você deseja criar e o atributo **ProgID** igual ao PROID do objeto de script WMI.

    O script do WSH a seguir exibe o nome do host e o número de processadores no computador local. Para executar o script, salve o texto em um arquivo com uma extensão. wsf.

    ```XML
    <?xml version="1.0" encoding="US-ASCII"?>
    <job>
     <object id="objSWbemLocator" progid="WbemScripting.SWbemLocator"/>
     <script language="VBScript">

      strComputer = "."
      Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, "root\cimv2")
      Set colSettings = objSWbemServices.ExecQuery("Select * From Win32_ComputerSystem")
      For Each objComputer in colSettings
       Wscript.Echo "System Name: " & objComputer.Name
       Wscript.Echo "Number of Processors: " & objComputer.NumberOfProcessors
      Next

     </script>
    </job>
    ```

    

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script)
</dt> <dt>

[API de script para WMI](scripting-api-for-wmi.md)
</dt> </dl>

 

 
