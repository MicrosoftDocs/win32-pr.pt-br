---
description: você pode criar um objeto para o wmi no Visual Basic scripting Edition (VBScript) conectando-se ao wmi e chamando CreateObject. A tabela a seguir lista os métodos na API de script para WMI que dão suporte à criação de objetos.
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
ms.openlocfilehash: e86dbc649d5feab471485dbdf536cde911c139aeab3b6eb3323b24199438d1d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119244566"
---
# <a name="creating-an-object-using-vbscript"></a>Criando um objeto usando o VBScript

você pode criar um objeto para o wmi no Visual Basic scripting Edition (VBScript) conectando-se ao wmi e chamando [CreateObject](/previous-versions//xzysf6hc(v=vs.85)). A tabela a seguir lista os métodos na API de script para WMI que dão suporte à criação de objetos.



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

1.  Conexão o WMI usando um moniker ou um objeto [**SWbemLocator**](swbemlocator.md) .

    Para obter mais informações, consulte [criando um script WMI](creating-a-wmi-script.md).

2.  Faça uma chamada para o método [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) do VBScript.

    O exemplo de código a seguir mostra como criar um objeto.

    ```VB
    Set locator = CreateObject("WbemScripting.SWbemLocator")
    ```

    

    Se você usar um moniker na etapa 1, não precisará chamar [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) novamente.

 

 
