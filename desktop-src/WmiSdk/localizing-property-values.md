---
description: O modelo de localização de esquema CIM fornece um mecanismo para localizar qualificadores. Ele não dá suporte à localização direta de valores de propriedade.
ms.assetid: a88bd873-7132-45b6-831e-64f9bb254c6e
ms.tgt_platform: multiple
title: Localizando valores de propriedade
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5ccec714557934ca32a878e21fb2a75d24a211a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296628"
---
# <a name="localizing-property-values"></a>Localizando valores de propriedade

O modelo de localização de esquema CIM fornece um mecanismo para localizar qualificadores. Ele não dá suporte à localização direta de valores de propriedade.

Em alguns casos, no entanto, os valores das propriedades de cadeia de caracteres nas instâncias estáticas podem ser substituídos por um tipo inteiro enumerado e um mapa de valor pode ser definido para a propriedade na definição de classe. Nesses casos, o qualificador de **valores** deve ser localizado. O uso de qualificadores de enumeração é o mecanismo primário para localizar valores de propriedade. Não há suporte para qualquer outra forma de localização de valor de propriedade.

O exemplo a seguir mostra como as propriedades estáticas podem ser localizadas usando mapas de valores parciais com expressões regulares. Neste exemplo, o subconjunto predefinido de valores é inicializado no esquema usando instâncias estáticas. O restante dos valores são fornecidos dinamicamente.

``` syntax
[abstract]
class DataGroup
{
   [key] string GUID;
   [Description("data group display name"): Amended,
                     ValueMap{"Logical Disk",
                     "CPU Utilization", ".+"}]
                     string GroupDisplayName;
   [ValueMap{"Monitors percentage of disk free space",
                  "Monitors percentage CPU utilization", ".+"}] 
                   string GroupDescription;
};

[static, Description ("pre-configured parameters") :amended]
class InitialGroup : DataGroup {
};

[dynamic, provider("HMProvider"),
    Description ("user-defined parameters") :amended]
class UserDefionedGroup : DataGroup {
};

instance of InitialGroup {
   GUID = "abc";
   GroupDisplayName = "Logical Disk";
   GroupDescription = "Monitors percentage of disk free space";
};

instance of InitialGroup {
   GUID = "def";
   GroupDisplayName = "CPU Utilization";
   GroupDescription = "Monitors percentage CPU utilization";
};
```

Para obter mais informações, consulte [localizando propriedades estáticas](localizing-static-properties.md).

 

 



