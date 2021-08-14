---
title: Exemplos de alterações incompatíveis
description: Ao lidar com alterações incompatíveis, a norma de prática é a seguinte, uma vez que qualquer alteração pode ser incompatível retroativamente, a menos que seja muito bem compreendida.
ms.assetid: 5b893d79-b81d-4ede-8d49-71d85219c497
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0a8736093e8189570026489bc1753145b941b7429b704e2c9c68783ddefef0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930035"
---
# <a name="examples-of-incompatible-changes"></a>Exemplos de alterações incompatíveis

Ao lidar com alterações incompatíveis, a boa regra geral é a seguinte: qualquer alteração pode ser incompatível com versões anteriores, a menos que seja muito bem compreendida. Esta regra requer conhecimento das regras de NDR. Se você não souber qual é o NDR, não faça modificações. Exemplos de alterações que normalmente resultam em uma violação de acesso no aplicativo ou uma exceção de dados stub inválidos \_ \_ \_ levantados pelo mecanismo de marshaling são os seguintes:

-   Adicionar um novo método no meio de métodos antigos.
-   Adicionando ou removendo parâmetros de um método.
-   Alterar um atributo, por exemplo, um atributo de ponteiro: alterando \[ ref \] para \[ Unique \] ou \[ PTR \] ou vice-versa. Cada tipo de ponteiro tem uma representação de conexão diferente.
-   Alterar o tamanho dos dados: de curto para longo, de char para WCHAR \_ t (Unicode), adicionando um campo a uma estrutura, alterando o tamanho de uma matriz de tamanho fixo.
-   Adicionar braços de União a uma União com uma cláusula padrão.

Algumas alterações traiçoeiros ou incompatibilidades indesejadas entre um cliente e um servidor podem ocorrer da seguinte maneira:

-   Modificar um membro de um tipo composto, como uma estrutura ou uma matriz. Por exemplo, se uma \_ ID do cliente for alterada de um integral para um GUID, uma estrutura de registro de cliente \_ com o \_ campo ID do cliente se tornará incompatível. Isso pode ser difícil de detectar se estiver em cascata por vários níveis de inserção para um tipo de parâmetro remoto real.
-   Modificando um tipo importado. O tipo pode ser proveniente de um componente diferente que não é remoto diretamente, portanto, a alteração foi considerada compatível.
-   Usar \# ifdef em um arquivo IDL é uma má ideia para ifdef definições de tipo em um arquivo IDL — é um desastre aguardando a ocorrência. Inevitavelmente, devido à compilação ou a outros problemas, um cliente é compilado com um conjunto diferente de definições do que o servidor e acaba sendo incompatível.

 

 




