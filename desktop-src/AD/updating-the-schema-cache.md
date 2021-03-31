---
title: Atualizando o cache de esquema
description: Todas as informações gravadas em um servidor Active Directory são validadas em relação ao esquema.
ms.assetid: 948f8ec5-7207-4566-bd79-60cdd54231bf
ms.tgt_platform: multiple
keywords:
- Atualizando o AD do cache de esquema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2bf915d00b463b81a331ffe39b342f620a50417
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634907"
---
# <a name="updating-the-schema-cache"></a>Atualizando o cache de esquema

Todas as informações gravadas em um servidor Active Directory são validadas em relação ao esquema. O esquema é mantido na memória nos servidores de diretório (controladores de domínio) por motivos de desempenho. A versão na memória é atualizada automaticamente depois que a versão em disco é atualizada. A atualização automática ocorre cinco minutos após a aplicação da última alteração; aplicar outra alteração ao esquema na janela de 5 minutos redefine o temporizador para outros 5 minutos. Esse comportamento mantém o cache consistente, mas pode ser confuso, pois as alterações não aparecem no esquema até que o cache seja atualizado, mesmo que elas tenham sido aplicadas no disco.

Para atualizar o cache de esquema de Active Directory após uma atualização de esquema, ou se você quiser usar a atualização de esquema para operações que não sejam de esquema imediatamente, adicione o atributo **schemaUpdateNow** (é um atributo operacional) ao DSE raiz (DN em branco) com o valor 1. Uma atualização do cache de esquema será iniciada imediatamente. A chamada está sendo bloqueada. Se a chamada retornar sem erro, o cache será atualizado e todas as atualizações de esquema estarão prontas para serem usadas. Um retorno de erro indica que a atualização do cache não foi bem-sucedida. Os aplicativos que devem usar esse recurso devem ser projetados para acomodar a gravação de bloqueio, particularmente em fornecer os comentários do usuário, se o programa ou o script for executado interativamente.

O exemplo de código a seguir é um exemplo de script do LDIFDE que mostra como disparar um recarregamento de cache.

``` syntax
dn:
changetype: modify
add: schemaUpdateNow
schemaUpdateNow: 1
-
```

Para obter mais informações sobre como atualizar o cache de esquema programaticamente, consulte [código de exemplo para atualizar o cache de esquema](example-code-for-updating-the-schema-cache.md).

 

 




