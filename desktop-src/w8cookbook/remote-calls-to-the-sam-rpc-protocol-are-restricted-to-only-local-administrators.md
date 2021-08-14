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
ms.openlocfilehash: ee009e3f346c7e7a179a324ec68834999acd711934ab5c64a3cae1845372dbdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118211331"
---
# <a name="remote-calls-to-the-sam-rpc-protocol-are-restricted-to-only-local-administrators"></a>Chamadas remotas para o Protocolo RPC SAM são restritas somente a administradores locais

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não oferece garantias, expressas ou implícitas, das informações aqui fornecidas.\]

O Protocolo RPC SAM está sendo restrito. Isso significa que somente os membros do grupo de Administradores local podem fazer chamadas remotas em relação a métodos nesse protocolo. Active Directory comportamento do controlador de domínio não é afetado.

## <a name="mitigations"></a>Atenuações

Verifique se os usuários corretos estão definidos como administradores no PC. A ACL usada para a verificação de acesso é configurável por meio da política de grupo.

 

 




