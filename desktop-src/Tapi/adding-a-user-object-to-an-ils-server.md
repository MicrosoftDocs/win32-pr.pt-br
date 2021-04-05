---
description: O fragmento de código a seguir ilustra a publicação de um objeto de usuário em um servidor ILS. Depois que um objeto de usuário é publicado, partes remotas podem usar o objeto de usuário para fazer chamadas para o usuário especificado.
ms.assetid: 8b68886c-0df5-4005-bcd5-1a18336f5192
title: Adicionando um objeto de usuário a um servidor ILS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f85b15dcdbca47187cf4155dfbf7535d06718c19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646970"
---
# <a name="adding-a-user-object-to-an-ils-server"></a>Adicionando um objeto de usuário a um servidor ILS

\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O fragmento de código a seguir ilustra a publicação de um objeto de usuário em um servidor ILS. Depois que um objeto de usuário é publicado, partes remotas podem usar o objeto de usuário para fazer chamadas para o usuário especificado.

Este fragmento pressupõe que [a conexão com um servidor ILS](connecting-to-an-ils-server.md) já foi executada.


```C++
hr = pDirectory->AddDirectoryObject(pDirectoryObject);
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**ITDirectory**](/windows/desktop/api/Rend/nn-rend-itdirectory)
</dt> <dt>

[**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject)
</dt> <dt>

[**ITDirectoryObjectUser**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectuser)
</dt> </dl>

 

 



