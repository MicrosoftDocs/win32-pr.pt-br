---
description: Uma matriz é uma lista indexada de valores de dados que são do mesmo tipo de dados, que você pode referenciar. Além das matrizes de cadeia de caracteres e numéricas, o MOF oferece suporte a matrizes de objetos e referências inseridas.
ms.assetid: f63c222f-499d-4776-8901-65cb8b142d2b
ms.tgt_platform: multiple
title: Matrizes MOF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0443f2ef3b3fe8fca398e281de71b0927a4f06f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164859"
---
# <a name="mof-arrays"></a>Matrizes MOF

Uma matriz é uma lista indexada de valores de dados que são do mesmo tipo de dados, que você pode referenciar. Além das matrizes de cadeia de caracteres e numéricas, o MOF oferece suporte a matrizes de objetos e referências inseridas.

As regras a seguir definem uma matriz MOF:

-   Colchetes usados após o identificador de propriedade especifique uma matriz em uma definição de classe.

    ``` syntax
    Class ArrayDataSample1
    {
        string strArray1[];
    };
    ```

-   Todas as matrizes devem ser unidimensionais.
-   As matrizes podem ser desassociadas ou ter um tamanho explícito.

    ``` syntax
    Class MyClass
    {
        sint32 MyMethod1 ([in, id(0)] Win32_LogicalDisk DiskArray1[]);
        sint32 MyMethod2 ([in, id(0)] Win32_LogicalDisk DiskArray2[32]);
    };
    ```

    O WMI implementa matrizes vinculadas e não associadas como estruturas **SafeArray** , o que permite que o WMI varie as dimensões da matriz em tempo de execução. Quando você declara uma matriz com um tamanho explícito, o WMI armazena o tamanho como um qualificador e trata o tamanho como o tamanho máximo sugerido. No entanto, o WMI pode expandir o tamanho, se necessário. A alteração do tamanho explícito não tem nenhum efeito sobre os dados reais.

-   As matrizes são inicializadas especificando-se os valores do tipo apropriado em uma lista separada por vírgulas.

    ``` syntax
    Class ArrayDataSample2
    {
        [key] string s;
        string strArray2[] = {"hello", "there"};
        sint32 dwArray[] = {1,2,3};
    };
    ```

-   Uma matriz de referências é declarada como uma matriz de cadeias de caracteres de caminho de objeto.

    Ao declarar uma cadeia de caracteres de caminho de objeto, não coloque o espaço em branco entre os elementos do caminho do objeto. O exemplo a seguir descreve como declarar uma referência de caminho de objeto.

    ``` syntax
    Class ClassWithRefArray
        { 
        [key] string s; 
        object ref refArray[]; 
        };

    instance of ClassWithRefArray
        {
        s = 23;
        refArray = {"Disk.Name=\"C:\"", "Disk.Name=\"E:\""};
        };
    ```

-   Você pode usar uma matriz como um parâmetro para um método, mas não como um valor de retorno para um parâmetro de entrada ou de entrada/saída.
-   Todos os elementos em uma matriz são criados como valores do mesmo tipo.

    Se os elementos de uma matriz forem do tipo de **objeto** , você poderá inserir qualquer tipo de objeto na matriz. Por outro lado, se você declarar um tipo específico de objeto, o WMI permitirá apenas objetos dessa classe ou subclasse na matriz. Os exemplos a seguir mostram declarações de matriz que incluem o uso do tipo de **objeto** .

    ``` syntax
    Class EmbedClass
    {
        [key] sint32 PropOfClass;
    };

    Class ArrayDataClass
    {
        [key] string s;
        string strArray1[];
        string strArray2[] = {"hello", "there"};
        sint32 dwArray[] = {1,2,3};
        EmbedClass objArray[];
    };

    instance of ArrayDataClass
    { 
        s = "keyStuff";
        strArray1 = { "1.2.3.4", "1.2.3.5", "1.2.3.7"};
        strArray2 = 
            {
                "SELECT * FROM RegistryKeyChangeEvent",
                "SELECT * FROM RegistryValueChangeEvent",
                "SELECT * FROM RegistryTreeChangeEvent"
            };
        dwArray  = { 1,2,3,5,6 };
        objArray = {
                       instance of EmbedClass{PropOfClass=3;},
                       instance of EmbedClass{PropOfClass=4;}
                   };
    };
    ```

 

 



