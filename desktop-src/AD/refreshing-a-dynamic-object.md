---
title: Atualizando um objeto dinâmico
description: Um cliente pode atualizar a TTL (vida útil) de uma determinada entrada de diretório para mantê-la ativa em uma das duas maneiras de executar uma atualização LDAP para o valor de seu atributo entryTTL antes que a entrada seja coletada pelo lixo.
ms.assetid: 5f51013c-b278-4ef7-a235-b238eed79a35
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7866c423fcb715289793a7beefa564150954257
ms.sourcegitcommit: 4d6ff888fd5825e78bc8fd5cdb21d4b542205039
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2020
ms.locfileid: "105769080"
---
# <a name="refreshing-a-dynamic-object"></a>Atualizando um objeto dinâmico

Um cliente pode atualizar a TTL (vida útil) de uma determinada entrada de diretório para mantê-la ativa em uma das duas maneiras:

-   Executar uma atualização LDAP para o valor de seu atributo **entryTTL** antes que a entrada seja coletada pelo lixo. Esse método de atualização de uma entrada dinâmica no diretório é um recurso adicional (opcional) de Active Directory Domain Services que não é especificado pelo RFC 2589.
-   Executar uma operação estendida LDAP com um OID de 1.3.6.1.4.1.1466.101.119.1 para a atualização de TTL, conforme estipulado no RFC 2589. Esse OID é definido como **o \_ \_ OID de \_ op \_ estendido de TTL LDAP** em WINLDAP. H.

 
* * Comentário * * *: os objetos dinâmicos são removidos pelo coletor de lixo quando expiraram, não há nenhuma fase do objeto sendo uma marca de exclusão quando expirado. Você precisa ter cuidado com a latência de replicação do AD ao atualizar objetos. Você precisa garantir que a atualização para atualizar o TTL chegue cedo o suficiente para que todas as réplicas do contexto de nomenclatura (catálogo completo e global) vejam a transação de atualização antes que o objeto expire localmente.

 




