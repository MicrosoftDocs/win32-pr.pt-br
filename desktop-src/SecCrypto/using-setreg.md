---
description: A ferramenta SetReg define o valor das chaves do registro que controlam o comportamento do processo de verificação do certificado Authenticode.
ms.assetid: c34c00fe-da99-4c2e-9e9a-0ef6406ae5ae
title: Usando SetReg
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 706463f86d38a03bc3416713be7427df55424d09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090915"
---
# <a name="using-setreg"></a>Usando SetReg

A ferramenta SetReg define o valor das chaves do registro que controlam o comportamento do processo de verificação do certificado Authenticode. Essas chaves, chamadas de chaves de estado de publicação de software, controlam se deve confiar em uma raiz de teste, permitir a aprovação offline de certificados, testar as datas de validade do certificado e executar verificações de revogação.

O comando a seguir lista a sintaxe e as opções para usar o SetReg.

**setreg-?**

O comando a seguir torna uma raiz de teste confiável. Por padrão, uma raiz de teste não é confiável. Depois que qualquer alteração nos valores de chave for feita, uma lista do valor atual de todos os valores de chave será exibida. Se a opção **-q** for usada, os valores de chave não serão exibidos.

**setreg 1 verdadeiro**

O comando a seguir torna uma raiz de teste não confiável e faz com que toda a verificação Verifique a revogação. A opção **-q** é usada para que a lista de valores de chave não seja exibida

**setreg-q 1 FALSE 3 TRUE**

> [!Note]  
> Comandos, opções e argumentos não diferenciam maiúsculas de minúsculas.

 

 

 



