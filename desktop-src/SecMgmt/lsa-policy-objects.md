---
description: A LSA armazena informações de política de segurança local em um conjunto de objetos. Seu aplicativo pode consultar ou editar a política de segurança local acessando esses objetos.
ms.assetid: c8ed5cd8-55cf-43e7-92a3-9bd17a1147a9
title: Objetos de política LSA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1481b6a6f49e973ecc2a2e1b53830bf22c67a77f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921842"
---
# <a name="lsa-policy-objects"></a>Objetos de política LSA

A LSA armazena informações de política de segurança local em um conjunto de objetos. Seu aplicativo pode consultar ou editar a política de segurança local acessando esses objetos.

O conjunto consiste nos quatro objetos a seguir:

-   A [política](policy-object.md) contém informações de política global.
-   [TrustedDomain](trusteddomain-object.md) contém informações sobre um domínio confiável.
-   [Conta](account-object.md) contém informações sobre um usuário, grupo ou conta de grupo local.
-   [Os dados privados](private-data-object.md) contêm informações protegidas, como senhas de conta de servidor. Essas informações são armazenadas como cadeias de caracteres criptografadas.

Para obter mais informações sobre como usar as funções de política LSA para gerenciar as informações armazenadas nesses objetos, consulte [usando a política LSA](using-lsa-policy.md).

 

 



