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
# <a name="localizing-property-values"></a><span data-ttu-id="235a7-104">Localizando valores de propriedade</span><span class="sxs-lookup"><span data-stu-id="235a7-104">Localizing Property Values</span></span>

<span data-ttu-id="235a7-105">O modelo de localização de esquema CIM fornece um mecanismo para localizar qualificadores.</span><span class="sxs-lookup"><span data-stu-id="235a7-105">The CIM schema localization model provides a mechanism for localizing qualifiers.</span></span> <span data-ttu-id="235a7-106">Ele não dá suporte à localização direta de valores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="235a7-106">It does not support direct localization of property values.</span></span>

<span data-ttu-id="235a7-107">Em alguns casos, no entanto, os valores das propriedades de cadeia de caracteres nas instâncias estáticas podem ser substituídos por um tipo inteiro enumerado e um mapa de valor pode ser definido para a propriedade na definição de classe.</span><span class="sxs-lookup"><span data-stu-id="235a7-107">In some cases, however, the string properties values in the static instances can be replaced by an enumerated integer type and a value map can be defined for the property in the class definition.</span></span> <span data-ttu-id="235a7-108">Nesses casos, o qualificador de **valores** deve ser localizado.</span><span class="sxs-lookup"><span data-stu-id="235a7-108">In these cases, the **Values** qualifier should be localized.</span></span> <span data-ttu-id="235a7-109">O uso de qualificadores de enumeração é o mecanismo primário para localizar valores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="235a7-109">Using enumeration qualifiers is the primary mechanism for localizing property values.</span></span> <span data-ttu-id="235a7-110">Não há suporte para qualquer outra forma de localização de valor de propriedade.</span><span class="sxs-lookup"><span data-stu-id="235a7-110">Any other forms of property value localization are not supported.</span></span>

<span data-ttu-id="235a7-111">O exemplo a seguir mostra como as propriedades estáticas podem ser localizadas usando mapas de valores parciais com expressões regulares.</span><span class="sxs-lookup"><span data-stu-id="235a7-111">The following example shows how static properties can be localized using partial value maps with regular expressions.</span></span> <span data-ttu-id="235a7-112">Neste exemplo, o subconjunto predefinido de valores é inicializado no esquema usando instâncias estáticas.</span><span class="sxs-lookup"><span data-stu-id="235a7-112">In this example, the predefined subset of values is initialized in the schema using static instances.</span></span> <span data-ttu-id="235a7-113">O restante dos valores são fornecidos dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="235a7-113">The rest of the values are provided dynamically.</span></span>

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

<span data-ttu-id="235a7-114">Para obter mais informações, consulte [localizando propriedades estáticas](localizing-static-properties.md).</span><span class="sxs-lookup"><span data-stu-id="235a7-114">For more information, see [Localizing Static Properties](localizing-static-properties.md).</span></span>

 

 



