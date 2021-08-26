---
title: Alças implícitas versus explícitas
description: Para declarar um identificador de serialização, use o identificador primitivo identificador \_ t.
ms.assetid: 70d8665f-d793-46fc-bcbf-ecb24e746786
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f9f6dabc8a6e4d0e5ccac7ac8b94e1812d81a674b471015c868b32209fd9746
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020456"
---
# <a name="implicit-vs-explicit-handles"></a>Alças implícitas versus explícitas

Para declarar um identificador de serialização, use o identificador de tipo de [**identificador primitivo \_ t**](/windows/desktop/Midl/handle-t). Os alças de serialização podem ser explícitos ou implícitos. Especifique os alças implícitos no ACF do aplicativo usando o **\[ atributo de alça \_ implícita. \]** O compilador MIDL gerará uma variável de alça de serialização global. Os procedimentos de serialização com um alça implícito usam essa variável global para acessar um contexto de serialização válido.

Ao usar a codificação de tipo, as rotinas geradas que suportam a serialização de um tipo específico usam o identificador implícito global para acessar o contexto de serialização. Observe que as rotinas remotas podem precisar usar o alça implícito como um alça de associação. Certifique-se de que o alça implícito seja definido como um alça de serialização válido antes de fazer uma chamada de serialização.

Um handle explícito é especificado como um parâmetro do protótipo do procedimento de serialização no arquivo IDL ou também pode ser especificado usando o atributo **\[ de \_ \]** alça explícito no ACF. O parâmetro de alça explícito é usado para estabelecer o contexto de serialização adequado para o procedimento. Para estabelecer o contexto correto no caso de serialização de tipo, o [**\_**](/windows/desktop/Midl/handle-t) compilador gera as rotinas de suporte que usam o parâmetro t de identificador explícito como o identificador de serialização. Você deve fornecer um identificador de serialização válido ao chamar um procedimento de serialização ou rotina de suporte de tipo de serialização.

 

 