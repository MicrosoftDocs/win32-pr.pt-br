---
description: Você pode criar um objeto para WMI em Visual Basic Scripting Edition (VBScript) conectando-se ao WMI e chamando CreateObject. A tabela a seguir lista os métodos na API de script para WMI que dão suporte à criação de objetos.
ms.assetid: 3acbce31-6d56-4a7a-af03-fa37b2b868be
ms.tgt_platform: multiple
title: Criando um objeto usando o VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6bfbb4753f19f8ed6f7a61d94ab1d9f03b57e091
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461218"
---
# <a name="creating-an-object-using-vbscript"></a>Criando um objeto usando o VBScript

Você pode criar um objeto para WMI em Visual Basic Scripting Edition (VBScript) conectando-se ao WMI e chamando [CreateObject](/previous-versions//xzysf6hc(v=vs.85)). A tabela a seguir lista os métodos na API de script para WMI que dão suporte à criação de objetos.



| Interface                                        | ProgID                             |
|--------------------------------------------------|------------------------------------|
| [**SWbemDateTime**](swbemdatetime.md)           | "WbemScripting. SwbemDateTime"      |
| [**SWbemLocator**](swbemlocator.md)             | "WbemScripting. SWbemLocator"       |
| [**SWbemLastError**](swbemlasterror.md)         | "WbemScripting. SWbem. LastError"    |
| [**SWbemObjectPath**](swbemobjectpath.md)       | "WbemScripting.SWbemObjectPath"    |
| [**SWbemNamedValueSet**](swbemnamedvalueset.md) | "WbemScripting.SWbemNamedValueSet" |
| [**SWbemRefresher**](swbemrefresher.md)         | "WbemScripting.SWbemRefresher"     |
| [**SWbemSink**](swbemsink.md)                   | "WbemScripting. SWbemSink"          |



 

O procedimento a seguir descreve como criar um objeto WMI usando o VBScript.

**Para criar um objeto WMI usando o VBScript**

1.  Conecte-se ao WMI usando um moniker ou um objeto [**SWbemLocator**](swbemlocator.md) .

    Para obter mais informações, consulte [criando um script WMI](creating-a-wmi-script.md).

2.  Faça uma chamada para o método [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) do VBScript.

    O exemplo de código a seguir mostra como criar um objeto.

    ```VB
    Set locator = CreateObject("WbemScripting.SWbemLocator")
    ```

    

    Se você usar um moniker na etapa 1, não precisará chamar [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) novamente.

 

 
