---
title: As chamadas remotas para o protocolo SAM RPC são restritas somente a administradores locais
description: O protocolo SAM RPC está sendo restrito. Isso significa que somente os membros do grupo administrador local podem fazer chamadas remotas em relação a métodos nesse protocolo. O comportamento do controlador de domínio do Active Directory não é afetado.
ms.assetid: 816BFB8C-A8EE-44F4-864D-748AF8BCF1F8
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ee009e3f346c7e7a179a324ec68834999acd711934ab5c64a3cae1845372dbdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118211331"
---
# <a name="remote-calls-to-the-sam-rpc-protocol-are-restricted-to-only-local-administrators"></a>As chamadas remotas para o protocolo SAM RPC são restritas somente a administradores locais

\[Algumas informações estão relacionadas ao produto pré-lançado, que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não oferece garantias, expressas ou implícitas, das informações aqui fornecidas.\]

O protocolo SAM RPC está sendo restrito. Isso significa que somente os membros do grupo administrador local podem fazer chamadas remotas em relação a métodos nesse protocolo. O comportamento do controlador de domínio do Active Directory não é afetado.

## <a name="mitigations"></a>Atenuações

Verifique se os usuários certos estão definidos como administradores no computador. A ACL usada para a verificação de acesso é configurável por meio da política de grupo.

 

 




