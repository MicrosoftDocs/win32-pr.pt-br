---
title: Evento ActiveClientChange
description: Evento ActiveClientChange
ms.assetid: 617b40e6-cafb-463e-8b36-2a12c468d3ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8137edd559d934fd1a478350cd1185885c7dc148
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159808"
---
# <a name="activeclientchange-event"></a>Evento ActiveClientChange

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Ocorre quando o cliente ativo do caractere é alterado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

**Sub** - *agente.* ActiveClientChange (ByVal *caractereid*, ByVal *ativo* **)**



| Parte          | Descrição                                                                                                                                                                                                                                                        |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Caractere de caracteres* | Retorna a ID do caractere para o qual o evento ocorreu.                                                                                                                                                                                                      |
| *Ativo*      | Um valor booliano que indica se o cliente se tornou ativo ou não ativo. **Verdadeiro** O aplicativo cliente tornou-se o cliente ativo do caractere. <br/> **Falso** O aplicativo cliente não é mais o cliente ativo do caractere.<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Comentários

Quando vários aplicativos cliente compartilham o mesmo caractere, o cliente ativo do caractere recebe a entrada do mouse (por exemplo, o controle do Microsoft Agent clica ou arrasta eventos). Da mesma forma, quando vários caracteres são exibidos, o cliente ativo do caractere superior (também conhecido como o cliente de entrada-ativo) recebe eventos de [comando](command-event.md) .

Quando o cliente ativo de um caractere é alterado, esse evento retorna a ID desse caractere e **true** se o aplicativo se tornou o cliente ativo do caractere ou **false** se não for mais o cliente ativo do caractere.

Um aplicativo cliente pode receber esse evento quando o usuário seleciona a entrada de um aplicativo cliente no menu pop-up do caractere ou por comando de voz, quando o aplicativo cliente altera seu status ativo ou quando outro aplicativo cliente sai de sua conexão com o agente. O Agent envia esse evento somente para os aplicativos cliente que são diretamente afetados; que se tornem o cliente ativo ou que parem de ser o cliente ativo.

### <a name="see-also"></a>Consulte Também

* * * * [ActivateInput * * evento *](activateinput-event.md)*, * * * * [ativo * * Propriedade * *](active-property.md), [* * * DeactivateInput * * evento * *](deactivateinput-event.md), [* * * * Ativar * * método *](activate-method.md) *


 

 





