---
description: A ferramenta SetReg define o valor das chaves do Registro que controlam o comportamento do processo de verificação de certificado Authenticode.
ms.assetid: c34c00fe-da99-4c2e-9e9a-0ef6406ae5ae
title: Usando SetReg
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e0de37d236b978217d8c2a713e9595fbaad70afb69beb32cd0f5200738d2d8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118896733"
---
# <a name="using-setreg"></a>Usando SetReg

A ferramenta SetReg define o valor das chaves do Registro que controlam o comportamento do processo de verificação de certificado Authenticode. Essas chaves, chamadas de Chaves de Estado de Publicação de Software, controlam se é preciso confiar em uma raiz de teste, permitir a aprovação offline de certificados, testar datas de expiração do certificado e executar verificações de revogação.

O comando a seguir lista a sintaxe e as opções para usar SetReg.

**setreg -?**

O comando a seguir torna uma raiz de teste confiável. Por padrão, uma raiz de teste não é confiável. Depois que quaisquer alterações nos valores de chave são feitas, uma lista do valor atual de todos os valores de chave é exibida. Se a **opção -q** for usada, os valores de chave não serão exibidos.

**setreg 1 TRUE**

O comando a seguir torna uma raiz de teste nãotruda e faz com que toda a verificação verifique a revogação. A **opção -q** é usada para que a lista de valores de chave não seja exibida

**setreg -q 1 FALSE 3 TRUE**

> [!Note]  
> Comandos, opções e argumentos não são sensíveis a minúsculas.

 

 

 



