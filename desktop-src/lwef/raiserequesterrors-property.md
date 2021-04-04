---
title: Propriedade RaiseRequestErrors
description: Propriedade RaiseRequestErrors
ms.assetid: 60eb4478-526e-492a-8fb3-d1e54eff9868
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf9e559f999db663a8a9f5874f6d16a10e1e78ac
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104162242"
---
# <a name="raiserequesterrors-property"></a>Propriedade RaiseRequestErrors

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Retorna ou define se erros de solicitações são gerados.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*Agent * * *. RaiseRequestErrors* *  \[  =  *booliano*\]



| Parte      | Descrição                                                                                                                                                                                            |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *booleano* | Um valor booliano que determina se erros em solicitações são gerados.<br/> Erros de solicitação **true** (padrão) são gerados. <br/> **Falso**     Os erros de solicitação não são gerados.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa propriedade permite que você determine se o servidor gera erros que ocorrem com métodos que dão suporte a objetos de [**solicitação**](/windows/desktop/lwef/the-request-object) . Por exemplo, se você especificar um nome de animação que não exista em um método [**Play**](play-method.md), o servidor gerará um erro (exibindo a mensagem de erro), a menos que você defina essa propriedade como **false**.

Pode ser útil para linguagens de programação que não fornecem recuperação quando um erro é gerado. No entanto, tenha cuidado ao definir essa propriedade como **false**, pois pode ser mais difícil encontrar erros em seu código.

 

