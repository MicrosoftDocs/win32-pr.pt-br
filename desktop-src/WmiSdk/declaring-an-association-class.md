---
description: Uma classe de associação é um tipo especial de classe que define uma relação entre duas outras classes.
ms.assetid: 21fd6e39-5dd3-41b8-a2f5-0135a6637ce8
ms.tgt_platform: multiple
title: Declarando uma classe de associação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 083ce578ca912290fd026f225799793f89685aab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011508"
---
# <a name="declaring-an-association-class"></a>Declarando uma classe de associação

Uma classe de associação é um tipo especial de classe que define uma relação entre duas outras classes.

O procedimento a seguir descreve como criar uma classe de associação usando o código MOF.

**Para criar uma classe de associação usando código MOF**

1.  Atribua o qualificador de **Associação** à sua classe.

    Embora seja possível criar uma classe com referências a objetos ou classes, usar o qualificador de **Associação** não apenas torna claro que sua classe é uma classe de associação, mas, como prática recomendada, garante que sua classe funcione totalmente como uma classe de associação.

2.  Crie duas referências dentro da classe que descreve as duas instâncias de objeto que você deseja associar em conjunto usando o tipo **ref** .

    As referências associam os dois objetos na associação, contendo caminhos aos objetos. Embora não seja necessário, use as propriedades de referência como propriedades de chave também.

    Embora você possa criar referências totalmente qualificadas ou relativas a namespace, o WMI tem apenas suporte limitado para referências de namespace cruzado. Especificamente, somente objetos definidos estaticamente podem referenciar uns aos outros nos limites do namespace; os objetos com suporte dinâmico não podem fazer referência uns aos outros.

    Se necessário, use os qualificadores **HasClassRef** e **Classref** em conjunto com o tipo de referência de **objeto** para fazer referência a uma classe.

    O WMI dá suporte a um ponto de referência **ref** a uma instância, e a outra referência de **objeto** aponta para uma classe. Nesse caso, sua classe de associação descreveria uma associação que associa instâncias a classes.

    O exemplo de código a seguir descreve a sintaxe para usar **HasClassRef** e **Classref** com um tipo de **objeto** .

    ``` syntax
    [HasClassRefs, Association]
    class SomeAssocClass
    {
         [key, classref{ "MyEndpoint", "OtherContainer" }]
         object ref ep1;
         [key] object ref ep2;
    }; 
    ```

    No exemplo anterior, a referência **ep1** pode apontar para as definições de classe da classe **myEndpoint** ou da classe **OtherContainer** . Observe que, embora você deva digitar de tipo fraco a classe de referência, não é possível digitar fracamente o qualificador **Classref** ; Isso reduziria severamente a eficiência do mecanismo de consulta do WMI. A digitação fraca é criar uma referência que possa conter qualquer tipo de dados usando a palavra-chave **Object** e o tipo de dados **ref** . Para usar o **HasClassRef** com êxito, você deve definir os tipos de qualificador relevantes para propagar para todas as instâncias e subclasses.

3.  Crie outras propriedades conforme necessário.

    O exemplo de código a seguir mostra que o WMI atualmente não dá suporte a classes de associação com menos ou mais de duas propriedades de referência.

    ``` syntax
    [Association : ToInstance] 
    class MyAssocClass
    {
        ClassX ref PathToClassX ;
        ClassY ref PathToClassY ;
    };
    ```

4.  Quando terminar, compile seu código MOF com o compilador MOF.

    Para obter mais informações, consulte [compilando arquivos MOF](compiling-mof-files.md).

O exemplo de código na etapa 3 define a classe de associação **MyAssocClass** . A classe **MyAssocClass** define uma relação entre **ClassX** e **classe**. As propriedades **PathToClassX** e **PathToClassY** contêm caminhos de objeto para as instâncias das classes a serem associadas. A palavra-chave **ToInstance** é um dos vários sinalizadores de tipo que o WMI define para fornecer informações sobre o uso de um qualificador. A palavra-chave **ToInstance** indica que o WMI deve propagar o qualificador de **Associação** para todas as instâncias da classe de associação. Ao marcar esse qualificador de instância, o software cliente pode determinar que uma instância pertence a uma classe de associação, sem precisar recuperar a definição de classe para procurar o qualificador de **Associação** . Para obter mais informações, consulte [descrevendo um qualificador com um tipo de qualificador](describing-a-qualifier-with-a-qualifier-flavor.md) e [referências](references.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando classes formato MOF (MOF)](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



