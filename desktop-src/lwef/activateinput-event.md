---
title: Evento ActivateInput
description: Evento ActivateInput
ms.assetid: bc395750-5da0-4379-8eca-3195e936052c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db21d605a014002063a7c5aa42554a06adb1ed35296242944de789daeb3155c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610676"
---
# <a name="activateinput-event"></a>Evento ActivateInput

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**
</dt> <dd>

Ocorre quando um cliente se torna ativo de entrada.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

 *Sub-agente* \_ ActivateInput **(ByVal** *CharacterID***)**



| Parte          | Descrição                                                                    |
|---------------|--------------------------------------------------------------------------------|
| *CharacterID* | Retorna a ID do caractere por meio do qual o cliente se torna input-active. |



 

</dd> </dl>

### <a name="remarks"></a>Comentários

O cliente de entrada ativa recebe eventos de entrada de mouse e de fala fornecidos pelo servidor. O servidor envia esse evento somente para o cliente que se torna input-active.

Esse evento pode ocorrer quando o usuário alterna para o objeto [Command,](the-command-object.md) por exemplo, escolhendo a entrada do objeto Command na Janela Comandos ou no menu pop-up de um caractere. Isso também pode ocorrer quando o usuário seleciona um caractere (clicando ou falando seu nome), quando um caractere fica visível e quando o caractere de outro aplicativo cliente fica oculto. Você também pode chamar o método [Activate](activate-method.md) (com **Estado** definido como 2) para tornar explicitamente o caractere mais alto, o que faz com que seu aplicativo cliente se torne ativo de entrada e acione esse evento. No entanto, esse evento não ocorrerá se você usar o método Activate Method somente para especificar se o cliente é o cliente ativo do caractere.

### <a name="see-also"></a>Consulte Também

[**Evento DeactivateInput**](deactivateinput-event.md), [ **método Activate**](activate-method.md)


 

 




