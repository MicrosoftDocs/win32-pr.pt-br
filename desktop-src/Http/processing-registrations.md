---
title: Processando registros
description: As APIs do servidor HTTP usam o banco de dados de roteamento para aplicar verificações de acesso durante os registros.
ms.assetid: d72aa213-b8e8-4fe9-b98c-41114d2cea56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74454d888cccf083e27fc9067c8a5485e286b4f55df4c5c18f2b2e490dc9db39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118393839"
---
# <a name="processing-registrations"></a>Processando registros

As APIs do servidor HTTP usam o banco de dados de roteamento para aplicar verificações de acesso durante os registros. Um registro para um [URLPrefix](urlprefix-strings.md) deve passar uma série de verificações de acesso para garantir que o registro do usuário para o namespace tenha direitos de acesso. Use a função [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl) para adicionar um novo registro.

**Para adicionar um novo registro com HttpAddUrl**

1.  Se o número da porta no UrlPrefix tiver reservas ou registros para um esquema diferente do esquema no UrlPrefix, o registro falhará. Não há suporte para HTTP e HTTPS na mesma porta.
2.  O registro é integrado ao Bucket apropriado para o registro. Os buckets se baseiam no tipo de host da URL, conforme descrito na seção [Roteamento de solicitações de entrada](routing-incoming-requests.md) . As etapas a seguir são relativas a esse Bucket específico.
3.  Se existir uma entrada de registro duplicada, retorne um código de erro.
4.  Selecione entradas de reserva com componentes de esquema, host e porta que são iguais aos do UrlPrefix. A partir deles, localize a entrada com a correspondência de **relativeUri** mais longa. Se a entrada existir, verifique as permissões com base na ACL associada a essa entrada e retorne êxito. Se a entrada não existir, retornará um código de erro \_ já \_ existente.

Os exemplos a seguir ilustram o processo para instalar um registro no banco de dados de roteamento. As reservas 1 e 2 existem no banco de dados de roteamento.

-   Reserva 1: `https://+:80/vroot/subdir/` para usuário A e usuário C. Essa reserva é colocada no Bucket "+".
-   Reserva 2: `https://adatum.com:80/vroot/` para o usuário B. Essa reserva é colocada no Bucket "host explícito".
-   Registro: o `https://+:80/vroot/subdir/` usuário B falhará devido à reserva 1.
-   Registro: o `https://adatum.com:80/vroot/subdir/` usuário B tem sucesso devido à reserva 2.
-   Registro: `https://adatum.com:80/vroot/subdir/` por usuário C falha devido à reserva mais explícita 2. A reserva de curinga forte não tem significado no contexto da reserva ou do registro explícito.
-   Registro: `https://+:80/vroot/subdir/` por usuário A é executado com sucesso devido à reserva 1.
-   Registro: o `https://adatum.com:80/vroot/anotherdir/` usuário B tem sucesso devido à reserva 2.

A verificação de acesso para o registro não inclui verificações de privilégios de delegação. Não há verificações de acesso com base em reservas (consulte [**HttpRemoveUrl**](/windows/desktop/api/Http/nf-http-httpremoveurl)). O único requisito para excluir um registro dos EUA que o processo de chamada deve ter criado o registro.

 

 




