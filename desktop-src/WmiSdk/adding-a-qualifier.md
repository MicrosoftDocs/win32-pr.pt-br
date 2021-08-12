---
description: Um qualificador é uma cadeia de caracteres de dados que fornece mais informações sobre uma classe, instância, propriedade, método ou parâmetro.
ms.assetid: 6984b575-b365-49dd-aeab-a763430f434c
ms.tgt_platform: multiple
title: Adicionando um qualificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 333c24e89d711a8998c58c6201776d5d4c50cc1107f4c9ca4308d9cc992b44dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118557819"
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

Qualificadores podem ser divididos em qualificadores padrão, qualificadores CIM e qualificadores exclusivos incluem o seguinte:

-   Qualificador padrão

    Um qualificador padrão é um qualificador definido pelo WMI e comumente usado no código MOF. Por exemplo, os [**qualificadores Dynamic**](dynamic-qualifier.md) [**e Read**](standard-qualifiers.md) são qualificadores padrão. Para obter mais informações, consulte [Qualificadores WMI](wmi-qualifiers.md).

-   Qualificador CIM

    Um qualificador CIM é um qualificador incluído na especificação CIM. Embora use qualificadores CIM no código MOF, os qualificadores padrão são projetados especificamente com o WMI em mente. Para obter mais informações, consulte a Especificação [cim](https://www.dmtf.org/spec/cims.html/)DMTF .

-   Qualificador exclusivo

    Um qualificador exclusivo é um qualificador definido especificamente para uma nova classe por um provedor de classe. Por exemplo, o [**qualificador Unidades**](standard-qualifiers.md) é um qualificador não padrão específico do provedor. Você pode criar seus próprios qualificadores para uso com seu provedor. Para obter mais informações sobre como criar um provedor, consulte [Desenvolvendo um provedor WMI](developing-a-wmi-provider.md).

Seja qual for o seu qualificador, o processo principal que você executa é usar o qualificador em seu código MOF. Para obter mais informações, [consulte Aplicando um qualificador](applying-a-qualifier.md). Você pode descrever ainda mais um qualificador com um sabor de qualificador. Um sabor de qualificador contém mais informações sobre como um provedor deve usar um qualificador. Para obter mais informações, consulte [Descrevendo um qualificador com um qualificador Flavor](describing-a-qualifier-with-a-qualifier-flavor.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Projetando classes Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



