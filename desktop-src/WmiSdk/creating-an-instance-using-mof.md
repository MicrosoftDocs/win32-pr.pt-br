---
description: Você pode declarar uma instância básica de uma classe no serviço Windows Management usando Managed Object Format (MOF). Você também pode substituir os valores padrão de uma instância. Para obter mais informações, consulte Definindo um valor de propriedade de instância.
ms.assetid: 12eda062-9614-455d-ae99-7706c685137b
ms.tgt_platform: multiple
title: Criando uma instância usando MOF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05290fd02de80a905e74eeddeb1a04f316901209a97e0e298d038ac2f8888552
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097316"
---
# <a name="creating-an-instance-using-mof"></a>Criando uma instância usando MOF

Você pode declarar uma instância básica de uma classe no serviço Windows Management usando Managed Object Format (MOF). Você também pode substituir os valores padrão de uma instância. Para obter mais informações, consulte [Definindo um valor da propriedade de instância](#setting-an-instance-property-value).

O procedimento a seguir descreve como declarar uma instância básica de uma classe usando o código MOF.

**Para declarar uma instância básica de uma classe usando o código MOF**

1.  Use a **Instância de palavras-chave** seguida pelo nome da classe, chaves e um ponto e vírgula.

    O exemplo de código a seguir mostra como declarar uma instância de uma classe .

    ```mof
    instance of ClassName
    {
    };
    ```

    

2.  Quando terminar, insira o código MOF no repositório WMI usando o compilador MOF.

    Para obter mais informações, consulte [Compilando arquivos MOF](compiling-mof-files.md).

Uma instância de uma classe inclui todas as propriedades da classe . Se a classe for uma classe derivada, as instâncias incluirão as propriedades que pertencem a todas as classes mais altas na hierarquia. Cada classe da qual uma instância é criada tem uma ou mais propriedades de chave. Não é possível criar uma instância com mais de 256 chaves.

## <a name="setting-an-instance-property-value"></a>Definindo um valor da propriedade de instância

Como o WMI digita fortemente as propriedades, você não pode modificar tipos de propriedade. No entanto, você pode definir valores de propriedade em instâncias. Quando uma classe atribui um valor padrão a uma propriedade, o WMI atribui o valor padrão a cada instância. Você pode substituir esse valor em sua declaração de instância.

O procedimento a seguir descreve como definir um valor da propriedade ou substituir um valor padrão usando o código MOF.

**Para definir um valor da propriedade ou substituir um valor padrão usando o código MOF**

1.  Coloque uma instrução de atribuição entre as chaves da declaração de instância.

    O exemplo de código a seguir mostra como definir um valor da propriedade.

    ``` syntax
    instance of ClassName
    {
        Prop = "value";
    };
    ```

    O WMI não exige que você de definido nenhuma propriedade durante a criação da instância. A exceção é qualquer propriedade marcada com o [**Qualificador**](key-qualifier.md) de chave. Como o WMI usa propriedades de chave para identificar instâncias exclusivamente, você deve definir todas as propriedades de chave conforme as encontrar. Por outro lado, você não deve definir uma propriedade do sistema em uma declaração de instância. Em vez disso, o WMI atribui os valores apropriados a uma propriedade do sistema quando necessário.

2.  Quando terminar, insira o código MOF no repositório WMI com uma chamada para o compilador MOF.

    Para obter mais informações, consulte [Compilando arquivos MOF](compiling-mof-files.md).

Os exemplos de código a seguir mostram como uma instância especifica dados para propriedades definidas por uma classe.

``` syntax
class MyClass 
{
    [key] string   strProp;
    sint32   dwProp1;
    uint32       dwProp2;
};

instance of MyClass 
{
    strProp = "hello";
    dwProp1 = -1;
    dwProp2 = 0xffffffff;
};
```

No exemplo anterior, a classe define três propriedades: uma cadeia de caracteres, um inteiro com sinal de 32 bits e um inteiro sem sinal de 32 bits. A instância fornece valores de dados para cada uma dessas propriedades.

 

 



