---
title: Escolhendo um nível de autenticação
description: Ao escolher um nível de autenticação, use a diretriz a seguir.
ms.assetid: 6efb4162-5884-4bcb-86da-4809f89f0c26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98ac5610efad7ae1149d3c6555e2a005e3870a4f0e55983a17457bfa130561f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073456"
---
# <a name="choosing-an-authentication-level"></a>Escolhendo um nível de autenticação

Ao escolher um nível de autenticação, use a diretriz a seguir. Se não importa se os dados que estão sendo enviados podem ser interceptados e modificados e se os dados recebidos podem ser interceptados ou modificados, use RPC \_ C \_ AUTHN LEVEL NONE, que é \_ \_ o padrão. Se os dados não devem ser modificados e os dados privados não estão sendo enviados ou recebidos, use RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ INTEGRITY. Em todos os outros casos, use RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY.

Não use RPC \_ C \_ AUTHN \_ LEVEL \_ DEFAULT, RPC \_ C \_ AUTHN \_ LEVEL \_ CONNECT, RPC \_ C AUTHN LEVEL CALL ou \_ \_ \_ RPC C \_ \_ AUTHN \_ LEVEL \_ PKT. Um invasor sofisticado pode quebrar esses níveis de autenticação e torná-los ineficaz. Cada um desses níveis torna um pouco mais difícil para um invasor interceptar e modificar dados e representar, mas a segurança não é realmente obtida. Como o nível de sofisticação de um invasor raramente é conhecido, essas não são escolhas inteligentes.

 

 




