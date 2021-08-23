---
title: Evento DeactivateInput
description: Evento DeactivateInput
ms.assetid: 59747932-82be-45d5-8465-73798904e8a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98fe94d7d4e737d83dfb734bcc5b35c60bddf96dcf8b07c43df3b89817da21b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610526"
---
# <a name="deactivateinput-event"></a>Evento DeactivateInput

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

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


 

 




