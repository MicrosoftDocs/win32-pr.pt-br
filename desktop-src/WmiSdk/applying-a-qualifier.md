---
description: Como muitas outras técnicas no formato MOF (MOF), a aplicação de um qualificador ao seu código é um processo relativamente simples.
ms.assetid: aaa5c921-bdcd-40e6-ab4b-9441a1957e5b
ms.tgt_platform: multiple
title: Aplicando um qualificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89a393c7d3764338a8365ad3959803a8a3f665dbf1b9bdb0bebaaa7121ee6cb9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118320133"
---
# <a name="applying-a-qualifier"></a>Aplicando um qualificador

Como muitas outras técnicas no formato MOF (MOF), a aplicação de um qualificador ao seu código é um processo relativamente simples.

Os únicos desafios reais são as seguintes restrições nas convenções de nomenclatura que o WMI impõe:

-   Um qualificador pode descrever uma classe, instância, propriedade, método ou parâmetro de método.
-   Os nomes de qualificador não podem ter sublinhados à esquerda ou à direita.
-   Um nome de qualificador não pode começar com um dígito.
-   Um nome de qualificador não pode conter caracteres especiais, como & \* @! ~ \\ /.
-   Todos os nomes de qualificador não diferenciam maiúsculas de minúsculas.
-   Você não pode redefinir os qualificadores WMI padrão ou quaisquer qualificadores descritos na especificação CIM DMTF.
-   Os tipos de qualificador não são declarados explicitamente.

    Se você não declarar um tipo de qualificador, o WMI assumirá o tipo como booliano com um valor de **true**. Caso contrário, o WMI digitará os qualificadores com base nos valores do qualificador que você declarar.

-   Ao criar seus próprios qualificadores, você deve prefixar o nome do esquema para o nome do qualificador.

    A finalidade dessa regra é evitar confusão com novos qualificadores.

-   Você pode criar matrizes homogêneos de qualificadores.

    O exemplo de código a seguir mostra como as matrizes de qualificador são especificadas com chaves que envolvem os valores.

    ``` syntax
    [StringArray{"hello", "there"}, SingleElementArray{3}]
    ```

-   O WMI não oferece suporte a tipos de automação não listados na referência, como VT \_ NULL. Para obter mais informações, consulte [MOF Data Types](mof-data-types.md).

O procedimento a seguir ajuda você a usar o C++ para adicionar um qualificador a uma propriedade.

**Para aplicar um qualificador usando C++**

-   Aplique o qualificador com uma chamada para o método [**IWbemQualifierSet::P UT**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) .

    Você pode usar outros métodos de [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) para recuperar ou excluir qualificadores existentes.

O procedimento a seguir ajuda a aplicar um qualificador em arquivos MOF.

**Para descrever uma palavra-chave ou um identificador com um qualificador usando o MOF**

-   Coloque um qualificador entre colchetes antes da palavra-chave ou do identificador descrito pelo qualificador.

    O exemplo de código a seguir mostra como os qualificadores são usados.

    ``` syntax
    [qualifiers...]
    class StdDisk
    {
      [qualifiers...]  uint32 dwNumCylinders;
      [qualifiers...]  uint32 dwNumHeads;
      [qualifiers...]  sint32 Method1();
      sint32 Method2([qualifiers...] Parameter1);
    };
    ```

    O exemplo a seguir descreve o posicionamento apropriado dos qualificadores.

    ``` syntax
    [Abstract]
    class MyClass
    {
        [Amendment, InstanceOf]  uint32 dwNumber;
        sint32 MyMethod ([in] sint32 Param);
    };
    ```

 

 



