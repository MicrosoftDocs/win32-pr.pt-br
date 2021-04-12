---
title: Nomes de exibição de classe e atributo
description: Este tópico contém informações e diretrizes para nomes de exibição de classe e atributo.
ms.assetid: c85905b2-ed8b-4032-8c54-fd4de8b34ecf
ms.tgt_platform: multiple
keywords:
- exibir nomes de exibição de AD, classe e atributo de especificadores de exibição
- ANÚNCIOS de nomes de exibição de classe
- nome de exibição do atributo AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d65cd6ac6fc3077ff0d2bba15ffa9904b147654
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104453953"
---
# <a name="class-and-attribute-display-names"></a>Nomes de exibição de classe e atributo

O especificador de exibição para uma classe de objeto contém os seguintes atributos que podem ser usados para especificar os nomes de exibição localizados usados na interface do usuário para objetos dessa classe:

-   O atributo **classDisplayName** é uma cadeia de caracteres Unicode de valor único que especifica o nome de exibição da classe.
-   O atributo **attributeDisplayNames** é uma propriedade com vários valores que especifica os nomes a serem usados na interface do usuário para os atributos da classe de objeto.

Os valores de **attributeDisplayNames** são cadeias de caracteres Unicode; cada elemento consiste em um par de nomes delimitados por vírgula:


```C++
<attribute name>,<display text>
```



Neste exemplo, " &lt; nome do atributo &gt; " é o **lDAPDisplayName** do atributo e " &lt; texto de exibição &gt; " é o texto a ser exibido como o nome desse atributo na interface do usuário.

## <a name="guidelines-for-class-and-attribute-display-names"></a>Diretrizes para nomes de exibição de classe e atributo

Como muitos fornecedores podem estender classes com novos atributos ou criar classes totalmente novas, é importante que os nomes de exibição de classe e atributo sejam inequívocas e não resultem em conflitos.

Cada fornecedor deve prefixar o nome de exibição da classe com um identificador amigável exclusivo com base no nome do fornecedor. Por exemplo, se a empresa fictícia, a Fabrikam Inc., criar uma nova classe derivada da classe "Contact", ela poderá ter um nome de exibição de classe exclusivo "fabrikam Contact".

Se um fornecedor estende uma classe existente com novos atributos, ele deve novamente identificar exclusivamente o nome de exibição do atributo para que nenhum conflito ocorra com outros nomes de exibição de atributo. Novamente, a prefixação do nome de exibição do atributo com identificador amigável exclusivo com base no nome do fornecedor é uma prática recomendada. Por exemplo, se a empresa Fabrikam estende a classe user com um novo atributo HR, ela poderia exibir exclusivamente o atributo como "informações da Fabrikam HR".

Além disso, de uma perspectiva de localização, cada fornecedor deve localizar os nomes de exibição de classe e atributo em cada idioma com suporte no Windows 2000.

## <a name="adding-a-value-to-the-attributedisplaynames-attribute"></a>Adicionando um valor ao atributo attributeDisplayNames

**Para adicionar um valor de mapeamento de nome ao atributo **attributeDisplayNames****

1.  Determine se o valor de mapeamento de nome para o atributo existe. Se um valor de mapeamento de nome for substituído, primeiro exclua o valor existente, usando o método [**IADs::P utex**](/windows/desktop/api/iads/nf-iads-iads-putex) , com o parâmetro *lnControlCode* definido **como \_ Propriedade ADS \_ delete** e o parâmetro *vProp* definido como o valor a ser removido. Não use a **\_ Propriedade ADS \_ Clear** ou **a \_ \_ atualização da propriedade ADS** para *lnControlCode*.
2.  Crie a cadeia de caracteres que representa o nome de exibição do atributo. Para obter um exemplo, consulte o formato acima.
3.  Use o método [**IADs::P utex**](/windows/desktop/api/iads/nf-iads-iads-putex) com o parâmetro *lnControlCode* definido como **Propriedade do ADS \_ \_ Append** para adicionar o novo valor.
4.  Chame [**IADs:: setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) para confirmar as alterações no diretório.

Para obter mais informações sobre como nomear novas classes e atributos, consulte [nomenclatura de atributos e classes](naming-attributes-and-classes.md).

 

 