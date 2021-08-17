---
title: Propriedade Name
description: A propriedade Name é uma cadeia de caracteres usada pelos clientes para identificar, encontrar ou anunciar um objeto para o usuário. Todos os objetos são suportados pela propriedade Name.
ms.assetid: 7533955a-9538-4ead-a6ca-f61dd1b4d5c5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce046ef693e9e52323cdb7484bbdc291127b958d88857de6a8be4522b88e33de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133769"
---
# <a name="name-property"></a>Propriedade Name

A **propriedade Name** é uma cadeia de caracteres usada pelos clientes para identificar, encontrar ou anunciar um objeto para o usuário. Todos os objetos são suportados **pela propriedade** Name.

Por exemplo, o texto em um controle de botão é seu nome, enquanto o nome de uma caixa de listagem ou controle de edição é o texto estático que precede imediatamente o controle na ordem de tabulação. Até mesmo objetos gráficos que não exibem um nome fornecem texto quando consultados para a **propriedade** Name.

A **propriedade** Name é recuperada chamando [**IAccessible::get \_ accName.**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)

## <a name="selecting-names"></a>Selecionando nomes

O nome de um objeto deve ser intuitivo para que os usuários entendam o significado ou a finalidade do objeto. Além disso, **a propriedade Name** deve ser exclusiva em relação a qualquer objeto irmão no pai.

A navegação nas tabelas apresenta problemas especialmente difíceis para alguns usuários. Portanto, os desenvolvedores de servidores devem tornar os nomes de célula de tabela o mais descritivos possíveis. Por exemplo, você pode criar um nome de célula combinando os nomes da linha e da coluna que ela ocupa, como "A1". No entanto, geralmente é melhor usar nomes mais descritivos, como "Nancy, Fevereiro", em que "Nancy" é a linha atual e "Fevereiro" é a coluna atual.

## <a name="delegating-requests"></a>Delegando solicitações

Se um objeto não tiver acesso à propriedade **Name,** ele delegará solicitações ao pai, identificando-se por sua ID filho. Por exemplo, se um cliente chamar  a propriedade Nome de um controle de edição, o controle de edição delegará a consulta ao pai, que retorna o valor do controle de texto estático que rotula o controle de edição.

 

 




