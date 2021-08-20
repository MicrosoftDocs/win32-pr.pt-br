---
title: Representação
description: Representação é a capacidade de um thread executar em um contexto de segurança diferente do contexto do processo que possui o thread.
ms.assetid: b33ca3b0-0423-4338-b3d6-4bb3db3d3e1b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67654c3a894a985f5f3da7c25e2c2a2f095787fa659233d450165ccbdd5217c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117919238"
---
# <a name="impersonation"></a>Representação

Representação é a capacidade de um thread executar em um contexto de segurança diferente do contexto do processo que possui o thread. Ao executar no contexto de segurança do cliente, o servidor "é" o cliente, até certo ponto. O thread do servidor usa um token de acesso que representa as credenciais do cliente para obter acesso aos objetos aos quais o cliente tem acesso.

O principal motivo para a representação é fazer com que as verificações de acesso sejam executadas em relação à identidade do cliente. Usar a identidade do cliente para verificações de acesso pode fazer com que o acesso seja restrito ou expandido, dependendo do que o cliente tem permissão para fazer. Por exemplo, suponha que um servidor de arquivos tenha arquivos contendo informações confidenciais e que cada um desses arquivos seja protegido por uma ACL. Para ajudar a impedir que um cliente obtenha acesso não autorizado a informações nesses arquivos, o servidor pode representar o cliente antes de acessar os arquivos.

## <a name="access-tokens-for-impersonation"></a>Tokens de acesso para representação

Tokens de acesso são objetos que descrevem o contexto de segurança de um processo ou thread. Eles fornecem informações que incluem a identidade de uma conta de usuário e um subconjunto dos privilégios disponíveis para a conta de usuário. Cada processo tem um *token de acesso* primário que descreve o contexto de segurança da conta de usuário associada ao processo. Por padrão, o sistema usa o token primário quando um thread do processo interage com um objeto securável. No entanto, quando um thread representa um cliente, o thread de representação tem um token de acesso primário e um *token de representação*. O token de representação representa o contexto de segurança do cliente e esse token de acesso é aquele usado para verificações de acesso durante a representação. Quando a representação é final, o thread reverte para usar apenas o token de acesso primário.

Você pode usar a [**função OpenProcessToken**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocesstoken) para obter um handle para o token primário de um processo. Use a [**função OpenThreadToken**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) para obter um handle para o token de representação de um thread.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tokens de acesso](/windows/desktop/SecAuthZ/access-tokens)
</dt> <dt>

[Delegação e representação](delegation-and-impersonation.md)
</dt> </dl>

 

 