---
description: As classes usadas para manter os dados do registro são definidas com vários qualificadores padrão.
ms.assetid: d4786880-6c50-4e36-9a16-47de430e77a9
ms.tgt_platform: multiple
title: Definindo uma classe de registro com qualificadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f45fdff611814eadbf57eabedf7444d098666918
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827843"
---
# <a name="defining-a-registry-class-with-qualifiers"></a>Definindo uma classe de registro com qualificadores

As classes usadas para manter os dados do registro são definidas com vários qualificadores padrão.

Veja a seguir uma lista dos qualificadores padrão:

-   [Dinâmico](standard-wmi-qualifiers.md) e [ **provedor**](/windows/desktop/api/Provider/nl-provider-provider)

    Você pode anexar o qualificador **dinâmico** a uma classe ou uma instância. O qualificador **dinâmico** marca a classe ou instância como gerenciada dinamicamente por um provedor. Quando **dinâmico** aparece em uma classe ou instância, o qualificador do [**provedor**](/windows/desktop/api/Provider/nl-provider-provider) também deve aparecer. O qualificador do **provedor** identifica o provedor específico que deve gerenciar a classe ou instância dinâmica.

-   [ClassContext](standard-wmi-qualifiers.md)

    O qualificador **ClassContext** é anexado a uma classe. Especifica o caminho para a chave do registro que contém as informações que a classe representa.

    O qualificador **ClassContext** tem o seguinte formato.

    ``` syntax
    MACHINE_NAME|Subtree\\KeyPath
    ```

    O valor de KeyPath poderá ser longo se incluir chaves com subchaves.

    O exemplo a seguir mostra o qualificador **ClassContext** que contém o caminho para um dispositivo de transporte de computador específico.

    ``` syntax
    Machine_Name|HKEY_LOCAL_MACHINE\\SOFTWARE\\MICROSOFT\\WBEM\\TRANSPORTS
    ```

O modelo a seguir para uma definição de classe ilustra o uso dos qualificadores **dinâmico**, [**Provider**](/windows/desktop/api/Provider/nl-provider-provider)e **ClassContext** . O provedor chamado pelo qualificador do **provedor** é o provedor de registro do sistema de instância. Lembre-se de que os caminhos do registro não diferenciam maiúsculas de minúsculas, assim como os nomes do qualificador.

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

Os aplicativos de gerenciamento também podem usar o provedor de registro do sistema para recuperar e modificar dados de registro para uma chave específica.

 

 



