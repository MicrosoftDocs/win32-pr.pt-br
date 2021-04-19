---
title: Propriedade ListeningTip
description: Propriedade ListeningTip
ms.assetid: 02a678bb-5eb6-495f-b339-35170a44b15e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 402fd970bf902f034fd6ffb713029e3a27095c8e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105797557"
---
# <a name="listeningtip-property"></a>Propriedade ListeningTip

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

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


 

 




