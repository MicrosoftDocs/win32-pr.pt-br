---
title: Evento IdleStart
description: Evento IdleStart
ms.assetid: 3d97c26b-b88a-42e3-9072-0bc65510efc2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81458d4c88bc5db4ae4231ecb4ca47f456700917f42d6ccdfe5a6013bc288849
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119716046"
---
# <a name="idlestart-event"></a>Evento IdleStart

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**
</dt> <dd>

Ocorre quando o servidor define um caractere para o **estado de Idling.**

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

**Sub** *agente*** \_ IdleStart* *  **(ByVal** *CharacterID***)**



| Parte          | Descrição                                         |
|---------------|-----------------------------------------------------|
| *CharacterID* | Retorna a ID do caractere de idling como uma cadeia de caracteres. |



 

</dd> </dl>

### <a name="remarks"></a>Comentários

O servidor envia esse evento para todos os clientes do caractere.

### <a name="see-also"></a>Consulte Também

[**Evento IdleComplete**](idlecomplete-event.md)


 

 




