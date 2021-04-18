---
title: Propriedade Name
description: A propriedade Name é uma cadeia de caracteres usada pelos clientes para identificar, localizar ou anunciar um objeto para o usuário. Todos os objetos dão suporte à propriedade Name.
ms.assetid: 7533955a-9538-4ead-a6ca-f61dd1b4d5c5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e93d8b90190f81179d681600f4b1bfacf4665e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105807892"
---
# <a name="name-property"></a>Propriedade Name

A propriedade **Name** é uma cadeia de caracteres usada pelos clientes para identificar, localizar ou anunciar um objeto para o usuário. Todos os objetos dão suporte à propriedade **Name** .

Por exemplo, o texto em um controle de botão é seu nome, enquanto o nome de uma caixa de listagem ou controle de edição é o texto estático que precede imediatamente o controle na ordem de tabulação. Até mesmo objetos gráficos que não exibem um nome fornecem texto quando consultados para a propriedade **Name** .

A propriedade **Name** é recuperada chamando [**IAccessible:: get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname).

## <a name="selecting-names"></a>Selecionando nomes

O nome de um objeto deve ser intuitivo para que os usuários compreendam o significado ou a finalidade do objeto. Além disso, a propriedade **Name** deve ser exclusiva em relação a qualquer objeto irmão no pai.

A navegação dentro de tabelas apresenta problemas especialmente difíceis para alguns usuários. Portanto, os desenvolvedores de servidor devem tornar os nomes de célula da tabela o mais descritivo possível. Por exemplo, você pode criar um nome de célula combinando os nomes da linha e coluna que ele ocupa, como "a1". No entanto, geralmente é melhor usar nomes mais descritivos, como "Nancy, fevereiro", em que "Nancy" é a linha atual e "fevereiro" é a coluna atual.

## <a name="delegating-requests"></a>Delegando solicitações

Se um objeto não tiver acesso à sua propriedade **Name** , ele delegará solicitações para seu pai, identificando-se por sua ID filho. Por exemplo, se um cliente chama a propriedade **Name** de um controle de edição, o controle de edição delega a consulta para seu pai, que retorna o valor do controle de texto estático que rotula o controle de edição.

 

 




