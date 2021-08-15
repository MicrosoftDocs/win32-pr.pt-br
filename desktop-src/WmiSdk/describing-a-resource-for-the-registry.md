---
description: O registro do sistema contém dados relacionados a recursos.
ms.assetid: e66f1db8-a5f3-41d3-9835-34b81b9da5ed
ms.tgt_platform: multiple
title: Descrevendo um recurso para o registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30be25eed569f212e435827023eed132cf1c6ead49be37eabb6fe4ac30e8e3b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097266"
---
# <a name="describing-a-resource-for-the-registry"></a>Descrevendo um recurso para o registro

O registro do sistema contém dados relacionados a recursos. Esses dados estão localizados na seguinte chave do registro e são mantidos em um tipo de dados de registro especial chamado **reg \_ Resource \_ list**. Os aplicativos podem obter os dados relacionados ao recurso por meio do provedor de registro do sistema. Você pode adicionar e modificar os recursos do sistema no registro.

```
HKEY_LOCAL_MACHINE
   Hardware
      ResourceMap
```

O procedimento a seguir descreve como armazenar informações relacionadas ao recurso no registro do sistema.

**Para armazenar informações relacionadas ao recurso no registro do sistema**

1.  Crie uma cadeia de caracteres que contenha os campos a seguir.

    

    <table>
    <thead>
    <tr class="header">
    <th>Campo</th>
    <th>Contém</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Tipo de interface</td>
    <td>Um dos seguintes valores:<br/> <dl> Interna<br />
    ISA<br />
    EISA<br />
    Microchannel<br />
    TurboChannel<br />
    PCIBus<br />
    VMEBus<br />
    NuBus<br />
    PCMCIABus<br />
    CBus<br />
    MPIBus<br />
    MPSABus<br />
    </dl></td>
    </tr>
    <tr class="even">
    <td>Número do barramento</td>
    <td>Inteiro que especifica o número do barramento.</td>
    </tr>
    <tr class="odd">
    <td>Número de descritor parcial</td>
    <td>Inteiro que especifica o número do descritor.</td>
    </tr>
    <tr class="even">
    <td>Tipo de deslocamento ou de União</td>
    <td>Um dos seguintes valores:<br/> <dl> Port. Start<br />
    Port. PhysicalAddress<br />
    Port. Length<br />
    Interrupção. nível<br />
    Interrupção. vetor<br />
    Interrupção. afinidade<br />
    Memória. iniciar<br />
    Memória. PhysicalAddress<br />
    Memória. comprimento<br />
    DMA. Channel<br />
    DMA. porta<br />
    DMA. Reserved1<br />
    DeviceSpecificData. DataSize<br />
    DeviceSpecificData. Reserved1<br />
    DeviceSpecificData. Reserved2<br />
    </dl></td>
    </tr>
    </tbody>
    </table>

    

     

2.  Coloque a cadeia de caracteres na chave apropriada sob a chave do registro.

    ```
    HKEY_LOCAL_MACHINE
       Hardware
          ResourceMap
    ```

O exemplo de código a seguir descreve um descritor de recurso válido.

``` syntax
local|hkey_local_machine\hardware\resourcemap\
  hardware abstraction layer\
  pc compatible eisa/isa HAL|.raw("eisa",0,0,"interrupt.affinity")
```

O exemplo de código a seguir mostra uma sintaxe MOF válida para recuperar um descritor de recurso.

``` syntax
[DYNPROPS] 
class MyRegProp
{    
   [KEY]  
   STRING MyKey; 
   STRING MyReservedTranslated;
};

[DYNPROPS] 
instance of MyRegProp
{
   MyKey = "1";
   [PropertyContext("local|hkey_local_Machine\\hardware\\ResourceMap\\
                   System Resources\\Reserved|.Translated
                   (\"Internal\")(0)(1)(\"Memory.PhysicalAddress\")"),
   Dynamic, Provider("RegPropProv")] 
   MyReservedTranslated;
};
```

 

 




