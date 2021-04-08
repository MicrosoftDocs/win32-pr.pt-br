---
description: As cadeias de caracteres do construtor do objeto COM+ são cadeias de inicialização que são especificadas administrativamente para um componente.
ms.assetid: b4915dae-c97c-4d36-95ee-bb10dcb40845
title: Conceitos de cadeias de caracteres do construtor de objeto COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c32bffd35ad230efe1f22b52da10e1b4910d71da
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920257"
---
# <a name="com-object-constructor-strings-concepts"></a>Conceitos de cadeias de caracteres do construtor de objeto COM+

As cadeias de caracteres do construtor do objeto COM+ são cadeias de inicialização que são especificadas administrativamente para um componente. Você pode usar cadeias de caracteres de construtor de objeto para escrever um único componente com um grau de generalidade que permita que ele seja personalizado posteriormente para uma tarefa específica; ou seja, você pode executar a construção de objeto com parâmetros.

Por exemplo, você pode usar esse recurso para gravar um componente que contém uma conexão ODBC genérica e, posteriormente, especificar um DSN exato para o componente de forma administrativa. Se a configuração do sistema for alterada, você poderá alterar a cadeia de caracteres do construtor de acordo.

> [!Note]  
> As cadeias de caracteres do construtor de objeto não devem ser usadas para armazenar informações confidenciais de segurança.

 

Você pode usar cadeias de caracteres de construtor de objetos em conjunto com o [pool de objetos](com--object-pooling.md) para atingir um grau maior de granularidade em como pool e reutilizar recursos. Por exemplo, você pode criar vários componentes distintos, idênticos, exceto para cadeias de caracteres de construtor e CLSIDs, para manter pools distintos de objetos que contêm conexões utilizáveis por grupos distintos de clientes. Isso seria útil se as conexões fossem abertas de uma maneira que as associe a funções de segurança específicas — por exemplo, quando as conexões são abertas com alguma autenticação específica no banco de dados, Renderizando-as não reutilizáveis no caso geral.

Para fazer isso, você pode escrever um único componente genérico que se baseia em cadeias de caracteres do construtor de objetos, usando [**constructodeobjetoi**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct)e recompilá-lo para produzir vários componentes personalizáveis, cada um com um CLSID distinto. Em seguida, você pode personalizar administrativamente cada componente para abrir uma conexão apropriada com uma cadeia de caracteres de construtor, configurá-los para serem agrupados e eles serão mantidos em pools distintos por CLSID.

Você pode especificar uma cadeia de caracteres de Construtor quando um componente tiver sido gravado especificamente para reconhecer a cadeia de caracteres inserida. Os componentes podem acessar essas cadeias de caracteres programaticamente usando [**constructodeobjetoi**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct).

As cadeias de caracteres do Construtor são passadas no momento da criação do objeto quando a construção do objeto está habilitada administrativamente. O COM+ chama o método [**constructodeobjetoi:: Construct**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectconstruct-construct) que ele implementa. Dentro desse método, você pode acessar a cadeia de caracteres do construtor usando [**IObjectConstructString**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstructstring). Cadeias de caracteres vazias podem ser entradas válidas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pool de objetos COM+](com--object-pooling.md)
</dt> <dt>

[Especificando uma cadeia de caracteres de construtor de objeto para um componente](specifying-an-object-constructor-string-for-a-component.md)
</dt> <dt>

[Usando uma cadeia de caracteres de construtor de objeto para construir um componente](using-an-object-constructor-string-to-construct-a-component.md)
</dt> </dl>

 

 



