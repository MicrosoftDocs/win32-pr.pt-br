---
title: Propriedade HelpModeOn
description: Propriedade HelpModeOn
ms.assetid: 4a9b5fd3-12e2-489b-8ce0-9b66b01f517a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 489de1893e96bf2d4cc38ef9e788a726db8b9fd4dfbdc9ae3cd1b60f9bc02f91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962736"
---
# <a name="helpmodeon-property"></a>Propriedade HelpModeOn

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**
</dt> <dd>

Retorna ou define se o modo de Ajuda contextutivo está em para o caractere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agent.***Characters("**_CharacterID_*_"). Booliana HelpModeOn_ *  \[  =  \]



| Parte      | Descrição                                                                                                                                                       |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *booleano* | Uma expressão booliana que especifica se o modo de Ajuda contextutivo está. **True** O modo de ajuda está em. <br/> **O modo** de Ajuda False (Padrão) está desligado.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Quando você configura essa propriedade como **True**, o ponteiro do mouse muda para a imagem de Ajuda contextunte quando movido sobre o caractere ou sobre o menu pop-up para o caractere. Quando o usuário clica ou arrasta o caractere ou clica em um item no menu pop-up do caractere, o servidor dispara o evento [**HelpComplete**](helpcomplete-event.md) e sai do modo de Ajuda.

No modo de Ajuda, o servidor não envia os eventos [**Click**](click-event.md), [**DragStart**](dragstart-event.md), [**DragComplete**](dragcomplete-event.md)e [**Command,**](command-event.md) a menos que você de definir a propriedade [**AutoPopupMenu**](autopopupmenu-property.md) como **True.** Nesse caso, o servidor  enviará o evento Click (não sai do modo ajuda), mas apenas para o botão direito do mouse para permitir que você exibir o menu pop-up.

Essa propriedade se aplica somente ao uso do caractere pelo aplicativo cliente; A configuração não afeta outros clientes do caractere ou outros caracteres do aplicativo cliente.

## <a name="see-also"></a>Consulte Também

[**Evento HelpComplete**](helpcomplete-event.md)


 

 





