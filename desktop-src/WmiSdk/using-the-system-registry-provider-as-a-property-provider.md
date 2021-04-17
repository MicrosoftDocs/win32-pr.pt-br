---
description: Você pode usar o provedor de registro do sistema como uma instância ou um provedor de propriedades.
ms.assetid: 0a8198c0-57c1-4d96-9965-3867c8c0e738
ms.tgt_platform: multiple
title: Usar o provedor de registro do sistema como um provedor de propriedades
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 64fc701843438b4d173b1914ed2ac86214fe685e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105762357"
---
# <a name="use-the-system-registry-provider-as-a-property-provider"></a>Usar o provedor de registro do sistema como um provedor de propriedades

Você pode usar o [provedor de registro do sistema](/previous-versions/windows/desktop/regprov/system-registry-provider) como uma instância ou um provedor de propriedades.

Se você optar por acessar as interfaces do provedor de propriedades, deverá marcar suas classes WMI para indicar sua intenção.

**Para usar o provedor de registro do sistema como um provedor de propriedades**

-   Defina sua classe WMI com os qualificadores **DynProps**, [**Provider**](/windows/desktop/api/Provider/nl-provider-provider)e **PropertyContext** Standard.

    O qualificador **DynProps** identifica uma classe como tendo propriedades que são mantidas pelo provedor de propriedades identificado pelo qualificador do [**provedor**](/windows/desktop/api/Provider/nl-provider-provider) . O qualificador **PropertyContext** especifica o nome do valor do registro a ser armazenado pela propriedade. O formato do qualificador **PropertyContext** é o mesmo que o formato do qualificador **ClassContext** com valores *valueName* e *expression* adicionais.

    ``` syntax
    MACHINE_NAME | Subtree\\KeyPath [|valuename [expression]]
    ```

    *ValueName* e *expression* são opcionais. A configuração *valorname* só será usada se o valor do registro tiver um nome. A *expressão* também é opcional e é usada para dados do descritor de recursos. Para obter mais informações, consulte [descrevendo um recurso para o registro](describing-a-resource-for-the-registry.md).

    O exemplo de código a seguir mostra como a classe usa o provedor de registro do sistema como um provedor de propriedades para manter suas propriedades não chave.

    ``` syntax
    [DYNPROPS]
    class PropReg {

        [KEY]  STRING  MyKey;
        STRING Logging;
        STRING Events;
        uint32 Resource1;
    };

    [DYNPROPS]
    instance of PropReg
    {
      MyKey = "a";

      [PropertyContext("local|hkey_local_Machine\\software\\microsoft\\
       wbem\\cimom|Logging"), Dynamic, Provider("RegPropProv")]  Logging;

      [PropertyContext("local|hkey_local_Machine\\software\\microsoft\\
       wbem\\cimom|EnableEvents"), Dynamic, Provider("RegPropProv")]
       Events;

      [PropertyContext("local|hkey_local_Machine\\hardware\\
       ResourceMap\\Hardware Abstraction Layer\\PC Compatible Eisa/isa 
       hal|.raw(\"Internal\")(0)(0)(\"interrupt.vector\")"), Dynamic, 
       Provider("RegPropProv")]  Resource1;
    };
    ```

 

 
