---
title: Atualize um objeto dinâmico
description: Um cliente pode atualizar a TTL (Vida Vida) de uma determinada entrada de diretório para mantê-la a vivo de uma das duas maneiras Executando uma atualização LDAP para o valor de seu atributo entryTTL antes que a entrada seja coletada como lixo.
ms.assetid: 5f51013c-b278-4ef7-a235-b238eed79a35
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6c351b559da8d08ccca3346f7126a9bbe47fcd3774486ea64a8dff29ac7e799
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025165"
---
# <a name="refreshing-a-dynamic-object"></a>Atualize um objeto dinâmico

Um cliente pode atualizar a TTL (Vida Vida) de uma determinada entrada de diretório para mantê-la a vivo de uma das duas maneiras:

-   Executar uma atualização LDAP para o valor de seu **atributo entryTTL** antes que a entrada seja coletada como lixo. Esse método de atualização de uma entrada dinâmica no diretório é um recurso adicional (opcional) do Active Directory Domain Services que não é especificado pelo RFC 2589.
-   Executar uma operação estendida LDAP com um OID de 1.3.6.1.4.1.1466.101.119.1 para atualização de TTL, conforme estipulado na RFC 2589. Esse OID é definido como **LDAP \_ TTL \_ EXTENDED OP \_ \_ OID** em WINLDAP.H.

 
**Comentário***: objetos dinâmicos são removidos pelo Coletor de Lixo quando expiram, não há nenhuma fase do objeto sendo uma lápis quando ele tiver expirado. Você precisa ter cuidado com a latência de replicação do AD ao atualizar objetos. Você precisa garantir que a atualização para atualizar o TTL chegue cedo o suficiente para que todas as réplicas do contexto de nomengo (catálogo completo e global) vejam a transação de atualização antes que o objeto expire localmente.

 




