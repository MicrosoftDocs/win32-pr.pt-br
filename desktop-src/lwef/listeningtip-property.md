---
title: Propriedade ListeningTip
description: Propriedade ListeningTip
ms.assetid: 02a678bb-5eb6-495f-b339-35170a44b15e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d6a743eb26d1e2b57d106e72d77c3774938ffe7e56ca4ba4147001d74bb99f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665436"
---
# <a name="listeningtip-property"></a>Propriedade ListeningTip

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Retorna um valor booleano que indica a configuração de usuário atual para a dica de escuta.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintaxe** 
</dt> <dd>

*Agent * * *. SpeechInput.ListeningTip**



| Valor     | Descrição                    |
|-----------|--------------------------------|
| **Verdadeiro**  | A dica de escuta está habilitada.  |
| **Falso** | A dica de escuta está desabilitada. |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

A propriedade **ListeningTip** indica se a opção Exibir dica de escuta na folha de propriedades do Microsoft Agent (opções avançadas de caracteres) está habilitada. Quando **ListeningTip** retorna **true** e a entrada de fala está habilitada, o servidor exibe a janela de gorjeta quando o usuário pressiona a tecla de escuta.

## <a name="see-also"></a>Consulte Também

[**Evento AgentPropertyChange**](agentpropertychange-event.md)


 

 




