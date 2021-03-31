---
title: Evento ActivateInput
description: Evento ActivateInput
ms.assetid: bc395750-5da0-4379-8eca-3195e936052c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e0b4fdf83256d58dd247dee85b639f5499f013e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006037"
---
# <a name="activateinput-event"></a>Evento ActivateInput

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Ocorre quando um cliente torna-se entrada-ativo.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

**Sub** *Agent* \_ ActivateInput **(ByVal** *characterid * * *)**



| Parte          | Descrição                                                                    |
|---------------|--------------------------------------------------------------------------------|
| *Caractere de caracteres* | Retorna a ID do caractere por meio do qual o cliente se torna ativo. |



 

</dd> </dl>

### <a name="remarks"></a>Comentários

O cliente de entrada-ativo recebe eventos de entrada de mouse e fala fornecidos pelo servidor. O servidor envia esse evento somente para o cliente que se torna de entrada-ativo.

Esse evento pode ocorrer quando o usuário alterna para o objeto de [comando](the-command-object.md) , por exemplo, escolhendo a entrada do objeto de comando na janela comandos ou no menu pop-up de um caractere. Isso também pode ocorrer quando o usuário seleciona um caractere (clicando ou falando com seu nome), quando um caractere se torna visível e quando o caractere de outro aplicativo cliente se torna oculto. Você também pode chamar o [método Activate](activate-method.md) (com o **estado** definido como 2) para tornar explicitamente o caractere mais alto, o que faz com que o aplicativo cliente torne-se entrada-ativo e dispare esse evento. No entanto, esse evento não ocorrerá se você usar o método Activate do método somente para especificar se o cliente é o cliente ativo do caractere.

### <a name="see-also"></a>Consulte Também

[Evento **DeactivateInput**](deactivateinput-event.md), [método **Activate**](activate-method.md)


 

 




