---
description: Um tipo de qualificador é um sinalizador que descreve mais informações sobre um qualificador.
ms.assetid: a7d9d1c0-9386-4c90-9788-993b35ed12db
ms.tgt_platform: multiple
title: Descrevendo um qualificador com um tipo de qualificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 525cfc2c590ec8916e2e9538b3e8224e97b3b5dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165332"
---
# <a name="describing-a-qualifier-with-a-qualifier-flavor"></a>Descrevendo um qualificador com um tipo de qualificador

Um [*tipo de qualificador*](gloss-q.md) é um sinalizador que descreve mais informações sobre um qualificador. Por exemplo, o tipo de qualificador restrito informa que o WMI não deve propagar o qualificador associado para quaisquer classes ou instâncias derivadas. Você pode definir tipos usando o código MOF ou programaticamente. Embora você possa descrever uma variedade de efeitos com versões, as principais finalidades dos sinalizadores de tipo é definir como o WMI propaga qualificadores por meio de herança.

O WMI define vários tipos de qualificador que você pode anexar a qualquer qualificador, independentemente da origem do qualificador. No entanto, algumas versões não são apropriadas para todos os tipos de qualificador. O tipo **ToSubClass** , por exemplo, é apropriado apenas para qualificadores definidos para uma classe. Não é possível anexar **ToSubClass** a um qualificador usado para descrever uma instância.

Você pode usar tipos para descrever uma variedade de efeitos diferentes para qualificadores. Por exemplo, flavor pode indicar se um qualificador pode ser localizado. No entanto, uma das principais finalidades de um tipo de qualificador é descrever se uma classe pai pode passar qualificadores para uma subclasse ou instância de classe. Você também pode usar tipos para determinar se uma propriedade de classe passa um qualificador para uma propriedade de instância. Por fim, use os tipos para indicar se uma subclasse pode substituir o valor original de um qualificador herdado. No entanto, os qualificadores que você declara para uma classe ou instância não se propagam para as propriedades dessa classe ou instância. Além disso, os tipos que estabelecem permissões de substituição serão válidos somente se você também definir os tipos **ToInstance** ou **ToSubClass** .

Um tipo pode ser atribuído globalmente a um qualificador para um arquivo MOF inteiro usando a sintaxe a seguir, na qual o espaço em branco atua como o delimitador quando vários tipos são especificados.

``` syntax
Qualifier QualifierName : flavor1 <flavor2...>;
```

Os tipos globais se aplicam a todos os usos subsequentes do qualificador no arquivo MOF. As instruções de tipo global podem ocorrer em qualquer lugar no arquivo fora de um bloco de declaração de objeto. Os tipos redefinidos no nível de classe, instância ou propriedade substituem as declarações de tipo global para o escopo desse objeto.

Não é possível definir um novo tipo. Embora você possa criar um novo qualificador, use somente os [tipos de qualificador](qualifier-flavors.md) existentes para descrever o novo qualificador.

**Para definir os tipos de qualificador no MOF**

-   Declare os tipos que descrevem um determinado qualificador após o nome do qualificador, entre os colchetes do qualificador. Use o espaço em branco como o delimitador entre vários tipos.

    O exemplo a seguir mostra o padrão para anexar qualificadores predefinidos.

    ``` syntax
    [qualifier1 : flavor1 flavor2 flavor3, qualifier2 : flavor1]
    ```

Você pode adicionar o qualificador tipos programaticamente apenas em C++. Essa operação não está disponível na [API de script para WMI](scripting-api-for-wmi.md), embora você possa adicionar um novo qualificador chamando [**SWbemQualifierSet. Add**](swbemqualifierset-add.md).

**Para atribuir um tipo usando C++**

-   Chame o método [**IWbemQualifierSet::P UT**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) com o parâmetro *lFlavor* definido como uma das constantes definidas para o método.

 

 



