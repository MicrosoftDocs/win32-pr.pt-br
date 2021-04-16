---
description: Um qualificador é uma cadeia de caracteres de dados que fornece mais informações sobre uma classe, instância, propriedade, método ou parâmetro.
ms.assetid: 6984b575-b365-49dd-aeab-a763430f434c
ms.tgt_platform: multiple
title: Adicionando um qualificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5a6f18f2b79bcd25b2b4ca75811157c9091e6eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105794591"
---
# <a name="adding-a-qualifier"></a>Adicionando um qualificador

Um qualificador é uma cadeia de caracteres de dados que fornece mais informações sobre uma classe, instância, propriedade, método ou parâmetro.

A definição de classe a seguir é um exemplo de uma classe derivada que tem qualificadores de classe.

``` syntax
[Dynamic, Provider ("ProviderX")] 
class MyDerivedClass : MyClass
{
    [key] string sKey;
    [Implemented] sint32 ValueMethod();
    [Implemented] sint32 MyMethod ([in, Id(0)] sint32 Param);
};
```

Os qualificadores podem ser divididos em qualificadores padrão, qualificadores CIM e qualificadores exclusivos incluem o seguinte:

-   Qualificador padrão

    Um qualificador padrão é um qualificador definido pelo WMI e comumente usado no código MOF. Por exemplo, os qualificadores [**dinâmico**](dynamic-qualifier.md) e de [**leitura**](standard-qualifiers.md) são qualificadores padrão. Para obter mais informações, consulte [qualificadores WMI](wmi-qualifiers.md).

-   Qualificador CIM

    Um qualificador CIM é um qualificador incluído na especificação CIM. Ao usar qualificadores CIM no código MOF, os qualificadores padrão são projetados especificamente com o WMI em mente. Para obter mais informações, consulte a [especificação CIM](https://www.dmtf.org/spec/cims.html/)do DMTF.

-   Qualificador exclusivo

    Um qualificador exclusivo é um qualificador definido especificamente para uma nova classe por um provedor de classe. Por exemplo, o qualificador de [**unidades**](standard-qualifiers.md) é um qualificador não padrão específico do provedor. Você pode criar seus próprios qualificadores para uso com seu provedor. Para obter mais informações sobre como criar um provedor, consulte [desenvolvendo um provedor WMI](developing-a-wmi-provider.md).

Seja qual for o seu qualificador, o processo principal que você executa é usar o qualificador em seu código MOF. Para obter mais informações, consulte [aplicando um qualificador](applying-a-qualifier.md). Você pode descrever ainda mais um qualificador com um tipo de qualificador. Um tipo de qualificador contém mais informações sobre como um provedor deve usar um qualificador. Para obter mais informações, consulte [descrevendo um qualificador com um tipo de qualificador](describing-a-qualifier-with-a-qualifier-flavor.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando classes formato MOF (MOF)](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



