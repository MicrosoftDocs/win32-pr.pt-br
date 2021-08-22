---
description: Com as funções hash e assinatura digital, um usuário pode assinar digitalmente os dados para que qualquer outro usuário possa verificar se os dados não foram alterados desde que foram assinados. A identidade do usuário que assinou os dados também pode ser verificada.
ms.assetid: dbe70506-f0d9-4239-a3af-8494fd6d4149
title: Hashes e assinaturas digitais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdd6367217343a067bbdd0d5a4ad5e9f4f47e9b744ee9f159046259ec2e26185
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006484"
---
# <a name="hashes-and-digital-signatures"></a>Hashes e assinaturas digitais

Com as [funções hash e assinatura digital](cryptography-functions.md), um usuário pode assinar digitalmente os dados para que qualquer outro usuário possa verificar se os dados não foram alterados desde que foram assinados. A identidade do usuário que assinou os dados também pode ser verificada.

Uma [*assinatura digital*](../secgloss/d-gly.md) consiste em uma pequena quantidade de dados binários, normalmente menos de 256 bytes. Essa assinatura pode ser agrupada com a mensagem assinada ou armazenada separadamente, dependendo de como um aplicativo específico foi implementado.

O provedor de criptografia forte da Microsoft cria assinaturas digitais que estão em conformidade com os [*padrões de criptografia de chave pública*](../secgloss/p-gly.md) (PKCS) da RSA \# 1.

 

 
