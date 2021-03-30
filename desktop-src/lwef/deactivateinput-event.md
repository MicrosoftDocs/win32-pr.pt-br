---
title: Evento DeactivateInput
description: Evento DeactivateInput
ms.assetid: 59747932-82be-45d5-8465-73798904e8a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b2fe1ff13b599fe5fbcf2dac22e548a0432f415
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916394"
---
# <a name="deactivateinput-event"></a>Evento DeactivateInput

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Ocorre quando um cliente se torna não-entrada-ativo.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

**Sub** *Agent * * * \_ DeactivateInput* *  **(ByVal** *characterid * * *)**



| Parte          | Descrição                                                                    |
|---------------|--------------------------------------------------------------------------------|
| *Caractere de caracteres* | Retorna a ID do caractere que faz com que o cliente se torne não-entrada-ativo. |



 

</dd> </dl>

### <a name="remarks"></a>Comentários

Um cliente de não entrada-ativo não recebe mais eventos de mouse ou fala do servidor (a menos que ele se torne de entrada-ativo novamente). O servidor envia esse evento somente para o cliente que se torna não-ativo.

Esse evento ocorre quando o aplicativo cliente é de entrada-ativo e o usuário escolhe a legenda de outro cliente no menu pop-up de um caractere ou na janela comandos de voz ou você chama o método [**Activate**](activate-method.md) e define o parâmetro **State** como 0. Isso também pode ocorrer quando o usuário seleciona o nome de outro caractere clicando ou falando. Você também receberá esse evento quando seu caractere estiver oculto ou se outro caractere ficar visível.

### <a name="see-also"></a>Consulte Também

[**Evento ActivateInput**](activateinput-event.md)


 

 




