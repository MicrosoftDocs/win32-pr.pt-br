---
description: As classes usadas para manter os dados do Registro são definidas com vários qualificadores padrão.
ms.assetid: d4786880-6c50-4e36-9a16-47de430e77a9
ms.tgt_platform: multiple
title: Definindo uma classe do Registro com qualificadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f42e3c383a5d71d66c88f388aa1745f8a8324568a7fd85ac0f48e5e2cff30e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117925222"
---
# <a name="defining-a-registry-class-with-qualifiers"></a>Definindo uma classe do Registro com qualificadores

As classes usadas para manter os dados do Registro são definidas com vários qualificadores padrão.

Veja a seguir uma lista dos qualificadores padrão:

-   [Dinâmico](standard-wmi-qualifiers.md) e [ **provedor**](/windows/desktop/api/Provider/nl-provider-provider)

    Você pode anexar **o qualificador** dinâmico a uma classe ou a uma instância. O **qualificador** Dinâmico marca a classe ou a instância como gerenciada dinamicamente por um provedor. Quando **Dynamic** aparece em uma classe ou instância, o [**qualificador do**](/windows/desktop/api/Provider/nl-provider-provider) provedor também deve aparecer. O **qualificador** Do provedor identifica o provedor específico que deve gerenciar a classe ou a instância dinâmica.

-   [ClassContext](standard-wmi-qualifiers.md)

    O **qualificador ClassContext** é anexado a uma classe. Ele especifica o caminho para a chave do Registro que contém as informações que a classe representa.

    O **qualificador ClassContext** tem o seguinte formato.

    ``` syntax
    MACHINE_NAME|Subtree\\KeyPath
    ```

    O valor de KeyPath poderá ser longo se incluir chaves com sub-chaves.

    O exemplo a seguir mostra o **qualificador ClassContext** que contém o caminho para um dispositivo de transporte de computador específico.

    ``` syntax
    Machine_Name|HKEY_LOCAL_MACHINE\\SOFTWARE\\MICROSOFT\\WBEM\\TRANSPORTS
    ```

O modelo a seguir para uma definição de classe ilustra o uso dos qualificadores **Dynamic,** [**Provider**](/windows/desktop/api/Provider/nl-provider-provider)e **ClassContext.** O provedor chamado pelo qualificador **Do** provedor é o provedor de Registro do Sistema da instância. Esteja ciente de que os caminhos do Registro não são sensíveis a maiúsculas e minúsculas, assim como nomes de qualificador.

``` syntax
[dynamic, provider("RegProv"), 
    ClassContext("local|hkey_local_machine\\software\\microsoft
    \\WBEM\\transports\\Network Transport Modules")]

class RegTrans
{
  [key] string  TransportsGUID;
  [PropertyContext("Name")] string Name;
  [PropertyContext("Independent")] uint32 Enabled;
};
```

Os aplicativos de gerenciamento também podem usar o provedor do Registro do Sistema para recuperar e modificar dados do Registro para uma chave específica.

 

 



