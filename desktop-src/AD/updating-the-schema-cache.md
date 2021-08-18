---
title: Atualizando o cache de esquema
description: Todas as informações que são escritas em um servidor do Active Directory são validadas em relação ao esquema.
ms.assetid: 948f8ec5-7207-4566-bd79-60cdd54231bf
ms.tgt_platform: multiple
keywords:
- Atualizando o AD do Cache de Esquema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff477ce97aab2e0e49522309d386a7e1c37b31e3b8171ef20c626fdaaa5b53a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024524"
---
# <a name="updating-the-schema-cache"></a>Atualizando o cache de esquema

Todas as informações que são escritas em um servidor do Active Directory são validadas em relação ao esquema. O esquema é mantido na memória em servidores de diretório (controladores de domínio) por motivos de desempenho. A versão na memória é atualizada automaticamente após a atualização da versão em disco. A atualização automática ocorre cinco minutos após a última alteração ser aplicada; aplicar outra alteração ao esquema na janela de 5 minutos redefine o temporizador por mais 5 minutos. Esse comportamento mantém o cache consistente, mas pode ser confuso, pois as alterações não aparecem no esquema até que o cache seja atualizado, mesmo que elas foram aplicadas no disco.

Para atualizar o cache de esquema do Active Directory após uma atualização de esquema ou se você quiser usar a atualização de esquema para operações que não são de esquema imediatamente, adicione o atributo **schemaUpdateNow** (é um atributo operacional) à DSE raiz (DN em branco) com o valor 1. Uma atualização de cache de esquema será iniciar imediatamente. A chamada está bloqueando. Se a chamada retornar sem erro, o cache será atualizado e todas as atualizações de esquema estarão prontas para serem usadas. Um retorno de erro indica que a atualização do cache não foi bem-sucedida. Os aplicativos que devem usar esse recurso devem ser projetados para acomodar a gravação de bloqueio, especialmente ao dar comentários ao usuário, se o programa ou o script for executado interativamente.

O exemplo de código a seguir é um script LDIFDE de exemplo que mostra como disparar um recarregamento de cache.

``` syntax
dn:
changetype: modify
add: schemaUpdateNow
schemaUpdateNow: 1
-
```

Para obter mais informações sobre como atualizar o cache de esquema programaticamente, consulte Código de exemplo para [atualizar o cache de esquema.](example-code-for-updating-the-schema-cache.md)

 

 




