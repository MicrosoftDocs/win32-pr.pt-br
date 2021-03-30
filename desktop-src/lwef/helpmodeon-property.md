---
title: Propriedade HelpModeOn
description: Propriedade HelpModeOn
ms.assetid: 4a9b5fd3-12e2-489b-8ce0-9b66b01f517a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43662469c6461e92186a92daddb505b851f8740a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636043"
---
# <a name="helpmodeon-property"></a>Propriedade HelpModeOn

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Retorna ou define se o modo de ajuda contextual está ativado para o caractere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agente do. ***Caracteres ("*** characterid * * *"). HelpModeOn* *  \[  =  *booliano*\]



| Parte      | Descrição                                                                                                                                                       |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *booleano* | Uma expressão booliana que especifica se o modo de ajuda contextual está ativado. **Verdadeiro** O modo de ajuda está ativado. <br/> **False** (padrão) o modo de ajuda é desativado.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Quando você define essa propriedade como **true**, o ponteiro do mouse muda para a imagem de ajuda contextual quando movido sobre o caractere ou sobre o menu pop-up para o caractere. Quando o usuário clica ou arrasta o caractere ou clica em um item no menu pop-up do caractere, o servidor dispara o evento [**HelpComplete**](helpcomplete-event.md) e sai do modo de ajuda.

No modo de ajuda, o servidor não envia os eventos de [**clique**](click-event.md), [**DragStart**](dragstart-event.md), [**DragComplete**](dragcomplete-event.md)e [**Command**](command-event.md) , a menos que você defina a propriedade [**AutoPopupMenu**](autopopupmenu-property.md) como **true**. Nesse caso, o servidor enviará o evento de **clique** (não sai do modo de ajuda), mas apenas para o botão direito do mouse para permitir que você exiba o menu pop-up.

Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.

## <a name="see-also"></a>Consulte Também

[**Evento HelpComplete**](helpcomplete-event.md)


 

 





