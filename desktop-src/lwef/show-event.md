---
title: Mostrar Evento
description: Mostrar Evento
ms.assetid: vs|msagent|~\pacontrol_7wrw.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b126c7726f8b8ed3ce1e83162cf41ad3223700630167448ff8a7655817a0604
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975731"
---
# <a name="show-event"></a>Mostrar Evento

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**
</dt> <dd>

Ocorre quando um caractere é exibido.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

**Sub** *agent*** \_ Show (ByVal* *  *CharacterID,* **ByVal** *Cause***)**



| Parte          | Descrição                                                                                                                                                                                                                                                                 |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Retorna a ID do caractere mostrado como uma cadeia de caracteres.                                                                                                                                                                                                                          |
| *Causa*       | Retorna um valor que indica o que causou a exibição do caractere. 2 O usuário mostrou o caractere (usando o menu ou comando de voz).<br/> 4 Seu aplicativo cliente mostrou o caractere.<br/> 6 Outro aplicativo cliente mostrou o caractere.<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Comentários

O servidor envia esse evento para todos os clientes do caractere. Para consultar o estado atual do caractere, use a [**propriedade Visible.**](visible-property.md)

### <a name="see-also"></a>Consulte Também

[**Ocultar evento**](hide-event.md), [ **VisibilityCause**](visibilitycause-property.md)


 

 





