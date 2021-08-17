---
title: Informações de segurança e de erro estendidas
description: As informações de erro estendidas oferecem dados muito úteis ao solucionar um problema de RPC, mas esses dados muitas são considerados confidenciais por organizações preocupados com a segurança.
ms.assetid: ca6ef213-e59d-4b4e-ae7e-f5b20d11fd01
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f246e86dee31ea5e755c45211e3bd949657cdf95c37bf6ab4de3706be09fdec3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925683"
---
# <a name="security-and-extended-error-information"></a>Informações de segurança e de erro estendidas

As informações de erro estendidas oferecem dados muito úteis ao solucionar um problema de RPC, mas esses dados muitas são considerados confidenciais por organizações preocupados com a segurança. Em consideração sobre esses problemas de segurança, as informações de erro estendidas são desativadas por padrão.

As informações de erro estendidas ainda são geradas quando as informações de erro estendidas são desabilitadas, mas as informações nunca são transmitidas entre os limites do processo ou do computador. Essa abordagem permite que informações de erro sejam usadas por ferramentas que têm acesso ao espaço de endereço do processo, como os depuradores. Quando ativado, as informações de erro estendidas são geradas e podem ser enviadas entre os limites do processo e do computador. Atualmente, as informações de erro estendidas são usadas para sequências de protocolo orientadas por conexão e RPC local (LRPC). Ele é parcialmente implementado para datagrams.

 

 




