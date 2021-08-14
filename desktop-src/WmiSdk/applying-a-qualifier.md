---
description: Como muitas outras técnicas no Managed Object Format (MOF), aplicar um qualificador ao seu código é um processo relativamente simples.
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

Como muitas outras técnicas no Managed Object Format (MOF), aplicar um qualificador ao seu código é um processo relativamente simples.

Os únicos desafios reais são as seguintes restrições em convenções de nomen entre as que o WMI impõe:

-   Um qualificador pode descrever uma classe, instância, propriedade, método ou parâmetro de método.
-   Nomes de qualificador não podem ter sublinhados à frente ou à frente.
-   Um nome de qualificador não pode começar com um dígito.
-   Um nome de qualificador não pode conter caracteres especiais, como & \* @ ! ~ \\ /.
-   Todos os nomes de qualificador não são sensíveis a maiúsculas e minúsculas.
-   Você não pode redefinir os qualificadores WMI padrão ou os qualificadores descritos na especificação CIM de DMTF.
-   Os tipos de qualificador não são declarados explicitamente.

    Se você não declarar um tipo qualificador, o WMI assumirá o tipo como booliana com um valor **true.** Caso contrário, os qualificadores de tipos WMI com base nos valores de qualificador declarados.

-   Ao criar seus próprios qualificadores, você deve prefixar o nome do esquema para o nome do qualificador.

    A finalidade dessa regra é evitar confusão com novos qualificadores.

-   Você pode criar matrizes homogêneas de qualificadores.

    O exemplo de código a seguir mostra como as matrizes de qualificador são especificadas com chaves que envolvem os valores.

    ``` syntax
    [StringArray{"hello", "there"}, SingleElementArray{3}]
    ```

-   O WMI não dá suporte a tipos de automação não listados na referência, como VT \_ NULL. Para obter mais informações, consulte [Tipos de dados MOF](mof-data-types.md).

O procedimento a seguir ajuda você a usar o C++ para adicionar um qualificador a uma propriedade.

**Para aplicar um qualificador usando C++**

-   Aplique o qualificador com uma chamada ao [**método IWbemQualifierSet::P ut.**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put)

    Você pode usar outros métodos de [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) para recuperar ou excluir qualificadores existentes.

O procedimento a seguir ajuda você a aplicar um qualificador em arquivos MOF.

**Para descrever uma palavra-chave ou identificador com um qualificador usando MOF**

-   Coloque um qualificador entre colchetes antes da palavra-chave ou identificador descrito pelo qualificador.

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

    O exemplo a seguir descreve o posicionamento adequado dos qualificadores.

    ``` syntax
    [Abstract]
    class MyClass
    {
        [Amendment, InstanceOf]  uint32 dwNumber;
        sint32 MyMethod ([in] sint32 Param);
    };
    ```

 

 



