---
title: Evento AgentPropertyChange
description: Evento AgentPropertyChange
ms.assetid: 56607e9c-99eb-42c1-987a-0f2bc3f82d75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bd643797e766543877497330a995d492f982d8a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005300"
---
# <a name="agentpropertychange-event"></a>Evento AgentPropertyChange

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Ocorre quando o usuário altera uma propriedade na janela Opções de caractere avançadas.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

**Sub** - *agente. * * * AgentPropertyChange**

</dd> </dl>

### <a name="remarks"></a>Comentários

Esse evento indica quando o usuário alterou e aplicou qualquer propriedade incluída na janela de opção de caractere avançado.

No seu código para tratar esse evento, você pode consultar as configurações de propriedade específicas dos objetos [AudioOutput](the-audiooutput-object.md) ou [SpeechInput](the-speechinput-object.md) .

### <a name="see-also"></a>Consulte Também

[**Evento DefaultCharacterChange**](defaultcharacterchange-event.md)


 

 




