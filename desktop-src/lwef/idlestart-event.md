---
title: Evento IdleStart
description: Evento IdleStart
ms.assetid: 3d97c26b-b88a-42e3-9072-0bc65510efc2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 706aafc13cb1639484539e3d08b305df217ecec8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105790332"
---
# <a name="idlestart-event"></a>Evento IdleStart

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Ocorre quando o servidor define um caractere para o estado **deixar** .

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

**Sub** *Agent * * * \_ IdleStart* *  **(ByVal** *characterid * * *)**



| Parte          | Descrição                                         |
|---------------|-----------------------------------------------------|
| *Caractere de caracteres* | Retorna a ID do caractere deixar como uma cadeia de caracteres. |



 

</dd> </dl>

### <a name="remarks"></a>Comentários

O servidor envia esse evento para todos os clientes do caractere.

### <a name="see-also"></a>Consulte Também

[**Evento IdleComplete**](idlecomplete-event.md)


 

 




