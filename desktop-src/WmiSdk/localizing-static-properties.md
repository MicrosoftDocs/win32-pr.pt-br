---
description: Você pode localizar propriedades estáticas usando mapas de valores parciais.
ms.assetid: 67e91454-c065-4ab2-a373-245c9392c71c
ms.tgt_platform: multiple
title: Localizando propriedades estáticas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecaba200b7880991d349c6e0c0196c88ffa54b11
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104298882"
---
# <a name="localizing-static-properties"></a>Localizando propriedades estáticas

Você pode localizar propriedades estáticas usando mapas de valores parciais.

O procedimento a seguir descreve como as propriedades estáticas podem ser localizadas usando mapas de valores parciais com expressões regulares.

**Para usar mapas de valor para localizar propriedades estáticas**

1.  Crie um arquivo MOF mestre (Mastervm. MOF).

    O exemplo de código a seguir pode ser usado para criar um arquivo MOF mestre (Mastervm. MOF).

    ```syntax
    [Locale(0x409)]
    class Group1
    {
        [key] string ID;
        [DisplayName("Numbers"),
            ValueMap{0,1,2,3}:amended,
            Values{"Zero", "One", "Two", "Three"}:amended]
        Uint32 Numbers;
    };
    ```

2.  Crie as versões de linguagem neutra e específica do idioma do arquivo MOF.

    Digite o comando a seguir em um prompt de comando para criar as versões de idioma neutro e específico do idioma do arquivo MOF.

    ```syntax
    mofcomp -MOF:LnVm.mof -MFL:LsVm.mfl -Amendment:MS_409 MasterVm.mof
    ```

    O compilador MOF gera os arquivos MOF específicos de linguagem e neutros de idioma, LnVm. mof e LsVm. MFL. Os valores em inglês americano para a propriedade [Numbers](numbers.md) são colocados no arquivo. MFL para o namespace American Inglês.

    O exemplo de código a seguir mostra o conteúdo do arquivo LsVm. MFL.

    ```syntax
    #pragma namespace("\\\\.\\root\\default")
    instance of __namespace{ name="ms_409";};
    #pragma namespace("\\\\.\\root\\default\\ms_409")

    [AMENDMENT, LOCALE(0x409)] 
    class Group1
    {
      [ValueMap{0, 1, 2, 3} : Amended,
          Values{"Zero", "One", "Two", "Three"} : Amended] 
      Uint32 Numbers;
    };
    ```

3.  Compile os dois arquivos MOF e armazene as informações de classe no repositório CIM.

    Digite o seguinte comando em um prompt de comando para compilar os dois arquivos MOF.

    ```syntax
    Mofcomp LnVm.mof 
    Mofcomp LsVm.mfl
    ```

4.  Localize o arquivo MFL para outras localidades.

    O exemplo de código a seguir mostra o conteúdo de um arquivo MFL para o namespace em francês.

    ```syntax
    #pragma namespace("\\\\.\\root\\default")
    instance of __namespace{ name="ms_40C";};
    #pragma namespace("\\\\.\\root\\default\\ms_40C")

    [AMENDMENT, LOCALE(0x40C)] 
    class Group1
    {
        [key] string ID;
        [ValueMap{0, 1, 2, 3} : Amended,
            Values{"Zero", "Un", "Deux", "Trois"} : Amended]
        Uint32 Numbers;
    };
    ```

O resultado líquido é que o nome de exibição e o valor da propriedade [Numbers](numbers.md) dependem da localidade do usuário conectado. Se o usuário especificar uma localidade que não foi fornecida, os dados do qualificador padrão vêm do namespace em inglês (MS \_ 409).

A implicação desse design é que cada valor de cadeia de caracteres é usado como um identificador de pesquisa, que não pode ser localizado. Ao definir esse esquema, você deve garantir que o valor que o provedor coloca é independente de localidade.

> [!Note]  
> No momento, o WMI não fornece suporte de tempo de execução para mapear valores para cadeias de caracteres definidas por qualificadores. A interpretação da sintaxe sugerida é a responsabilidade do aplicativo.

 

 

 



