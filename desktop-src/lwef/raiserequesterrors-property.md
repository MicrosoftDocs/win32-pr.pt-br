---
title: Propriedade RaiseRequestErrors
description: Propriedade RaiseRequestErrors
ms.assetid: 60eb4478-526e-492a-8fb3-d1e54eff9868
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 081a47eef17378c24df5bdbcb0f5141b0dece45ec9933f289d0b3da9193793d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118246609"
---
# <a name="raiserequesterrors-property"></a>Propriedade RaiseRequestErrors

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**
</dt> <dd>

Retorna ou define se são gerados erros para solicitações.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agent***. Booliano RaiseRequestErrors* *  \[  =  \]



| Parte      | Descrição                                                                                                                                                                                            |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *booleano* | Um valor booliana que determina se erros em solicitações são gerados.<br/> **Erros de**    solicitação True (Padrão) são gerados. <br/> **False**     Erros de solicitação não são gerados.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa propriedade permite que você determine se o servidor gera erros que ocorrem com métodos que suportam [**objetos request.**](/windows/desktop/lwef/the-request-object) Por exemplo, se você especificar um nome de animação que não existe em um método [**Play,**](play-method.md)o servidor gera um erro (exibindo a mensagem de erro), a menos que você de definir essa propriedade como **False.**

Pode ser útil para linguagens de programação que não fornecem recuperação quando um erro é gerado. No entanto, tenha cuidado ao definir essa propriedade como **False,** pois pode ser mais difícil encontrar erros em seu código.

 

