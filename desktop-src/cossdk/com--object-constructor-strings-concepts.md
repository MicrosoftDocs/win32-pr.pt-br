---
description: As cadeias de caracteres do construtor de objeto COM+ são cadeias de caracteres de inicialização que são especificadas administrativamente para um componente.
ms.assetid: b4915dae-c97c-4d36-95ee-bb10dcb40845
title: Conceitos de cadeias de caracteres do construtor de objeto COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9baef62780950e93043a48c2ccf13910faf7c692dc534f984ffd028e0b342dcd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029516"
---
# <a name="com-object-constructor-strings-concepts"></a>Conceitos de cadeias de caracteres do construtor de objeto COM+

As cadeias de caracteres do construtor de objeto COM+ são cadeias de caracteres de inicialização que são especificadas administrativamente para um componente. Você pode usar cadeias de caracteres de construtor de objeto para escrever um único componente com um grau de generalidade que permite que ele seja personalizado posteriormente para uma tarefa específica; ou seja, você pode executar a construção de objeto com parâmetros.

Por exemplo, você pode usar esse recurso para escrever um componente que contém uma conexão ODBC genérica e, posteriormente, especificar um DSN exato para o componente administrativamente. Se a configuração do sistema for mudada, você poderá alterar a cadeia de caracteres do construtor de acordo.

> [!Note]  
> As cadeias de caracteres do construtor de objeto não devem ser usadas para armazenar informações confidenciais de segurança.

 

Você pode usar cadeias de caracteres do construtor de objeto em conjunto com o [pool de](com--object-pooling.md) objetos para obter um grau maior de granularidade em como você faz pool e reutilizar recursos. Por exemplo, você pode criar vários componentes distintos, idênticos, exceto para cadeias de caracteres de construtor e CLSIDs, para manter pools distintos de objetos que mantêm conexões que podem ser utilizados por grupos distintos de clientes. Isso seria útil se as conexões são abertas de uma maneira que as associe a funções de segurança específicas, como quando as conexões são abertas com alguma autenticação específica no banco de dados, tornando-as não reutilizáveis no caso geral.

Para fazer isso, você pode escrever um único componente genérico que se baseia em cadeias de caracteres de construtor de objeto, usando [**IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct)e recompilá-lo para produzir vários componentes personalizáveis, cada um com um CLSID distinto. Em seguida, você pode personalizar administrativamente cada componente para abrir uma conexão apropriada com uma cadeia de caracteres de construtor, configurá-los para serem em pool e eles serão mantidos em pools distintos por CLSID.

Você pode especificar uma cadeia de caracteres de construtor quando um componente tiver sido gravado especificamente para reconhecer a cadeia de caracteres que você inserir. Os componentes podem acessar essas cadeias de caracteres programaticamente [**usando IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct).

As cadeias de caracteres do construtor são passadas no momento da criação do objeto somente quando a construção do objeto está habilitada administrativamente. COM+ chama o [**método IObjectConstruct::Construct**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectconstruct-construct) que ele implementa. Dentro desse método, você pode acessar a cadeia de caracteres do construtor usando [**IObjectConstructString**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstructstring). Cadeias de caracteres vazias podem ser entradas válidas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pool de objetos COM+](com--object-pooling.md)
</dt> <dt>

[Especificando uma cadeia de caracteres de construtor de objeto para um componente](specifying-an-object-constructor-string-for-a-component.md)
</dt> <dt>

[Usando uma cadeia de caracteres do construtor de objeto para construir um componente](using-an-object-constructor-string-to-construct-a-component.md)
</dt> </dl>

 

 



