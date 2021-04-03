---
title: Chamadas remotas para o Protocolo RPC SAM são restritas somente a administradores locais
description: O Protocolo RPC SAM está sendo restrito. Isso significa que somente os membros do grupo de Administradores local podem fazer chamadas remotas em relação a métodos nesse protocolo. Active Directory comportamento do controlador de domínio não é afetado.
ms.assetid: 816BFB8C-A8EE-44F4-864D-748AF8BCF1F8
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 669c20503551b0a380372524b898559dff472f2a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104084131"
---
# <a name="remote-calls-to-the-sam-rpc-protocol-are-restricted-to-only-local-administrators"></a>Chamadas remotas para o Protocolo RPC SAM são restritas somente a administradores locais

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]

O Protocolo RPC SAM está sendo restrito. Isso significa que somente os membros do grupo de Administradores local podem fazer chamadas remotas em relação a métodos nesse protocolo. Active Directory comportamento do controlador de domínio não é afetado.

## <a name="mitigations"></a>Atenuações

Verifique se os usuários corretos estão definidos como administradores no PC. A ACL usada para a verificação de acesso é configurável por meio da política de grupo.

 

 




