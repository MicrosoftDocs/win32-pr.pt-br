---
description: Uma classe de associação é um tipo especial de classe que define uma relação entre duas outras classes.
ms.assetid: 21fd6e39-5dd3-41b8-a2f5-0135a6637ce8
ms.tgt_platform: multiple
title: Declarando uma classe de associação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd569d1dc20ba40be6d19f3009ab4311f69e04ca3e8a01031e74a9c84b461552
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119244416"
---
# <a name="declaring-an-association-class"></a>Declarando uma classe de associação

Uma classe de associação é um tipo especial de classe que define uma relação entre duas outras classes.

O procedimento a seguir descreve como criar uma classe de associação usando o código MOF.

**Para criar uma classe de associação usando o código MOF**

1.  Atribua **o qualificador** De associação à sua classe.

    Embora seja possível criar uma classe com referências a  objetos ou classes, o uso do qualificador Association não apenas torna claro que sua classe é uma classe de associação, mas, como uma melhor prática, garante que sua classe funcione totalmente como uma classe de associação.

2.  Crie duas referências dentro da classe que descreve as duas instâncias de objeto que você deseja associar usando o **tipo ref.**

    As referências associam os dois objetos na associação, contendo caminhos para os objetos . Embora não seja necessário, use as propriedades de referência como propriedades de chave também.

    Embora você possa criar referências totalmente qualificadas ou relativas ao namespace, o WMI tem suporte limitado apenas para referências entre namespaces. Especificamente, somente objetos definidos estaticamente podem fazer referência entre si entre limites de namespace; Objetos dinamicamente com suporte não podem fazer referência uns aos outros.

    Se necessário, use os **qualificadores HasClassRef** e **Classref** em conjunto com o tipo **ref** de objeto para referenciar uma classe.

    O WMI dá suporte a **ter um ponto de** referência ref para uma instância e o outro ponto de referência de objeto para uma classe.  Nesse caso, sua classe de associação descreveria uma associação que associa instâncias a classes.

    O exemplo de código a seguir descreve a sintaxe para usar **HasClassRef** e **Classref** com um **tipo de** objeto.

    ``` syntax
    [HasClassRefs, Association]
    class SomeAssocClass
    {
         [key, classref{ "MyEndpoint", "OtherContainer" }]
         object ref ep1;
         [key] object ref ep2;
    }; 
    ```

    No exemplo anterior, a referência **ep1** pode apontar para as definições de classe para a **classe MyEndpoint** ou a **classe OtherContainer.** Observe que, embora você deve digitar fracamente a classe de referência, não é possível digitar fracamente o qualificador **Classref** em si; isso reduziria significativamente a eficiência do mecanismo de consulta WMI. A digitação fraca está criando uma referência que pode conter qualquer tipo de dados usando a palavra-chave **object** e **o tipo de dados ref.** Para usar **hasClassRef** com êxito, você deve definir os sabores de qualificador relevantes para propagar para todas as instâncias e subclasses.

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

4.  Quando terminar, compile o código MOF com o compilador MOF.

    Para obter mais informações, consulte [Compilando arquivos MOF](compiling-mof-files.md).

O exemplo de código na Etapa 3 define a classe de associação **MyAssocClass.** A **classe MyAssocClass** define uma relação entre **ClassX** e **ClassY.** As **propriedades PathToClassX** **e PathToClassY** contêm caminhos de objeto para as instâncias das classes a serem associadas. A **palavra-chave ToInstance** é um dos vários sinalizadores de tipo que o WMI define para fornecer informações sobre o uso de um qualificador. A **palavra-chave ToInstance** indica que o WMI deve propagar o qualificador **de** Associação para todas as instâncias da classe de associação. Ao verificar esse qualificador de instância, o software cliente pode determinar que uma instância pertence a uma classe de associação, sem precisar recuperar a definição de classe para procurar o **qualificador De** associação. Para obter mais informações, consulte [Descrevendo um qualificador com um qualificador flavor](describing-a-qualifier-with-a-qualifier-flavor.md) e [referências](references.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Projetando classes Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



