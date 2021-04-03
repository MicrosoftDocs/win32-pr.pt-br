---
title: Mostrar evento
description: Mostrar evento
ms.assetid: vs|msagent|~\pacontrol_7wrw.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6964164e14c759a971e5ceeda542a5c27131663
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822445"
---
# <a name="show-event"></a>Mostrar evento

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Ocorre quando um caractere é exibido.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

**Sub** *agente * * * \_ Mostrar (ByVal* *  *characterid*, **ByVal** *causa * * *)**



| Parte          | Descrição                                                                                                                                                                                                                                                                 |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Caractere de caracteres* | Retorna a ID do caractere mostrado como uma cadeia de caracteres.                                                                                                                                                                                                                          |
| *Causa*       | Retorna um valor que indica o que causou o caractere a ser exibido. 2 o usuário mostrou o caractere (usando o menu ou comando de voz).<br/> 4 seu aplicativo cliente mostrou o caractere.<br/> 6 outro aplicativo cliente mostrou o caractere.<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Comentários

O servidor envia esse evento para todos os clientes do caractere. Para consultar o estado atual do caractere, use a propriedade [**Visible**](visible-property.md) .

### <a name="see-also"></a>Consulte Também

[**Ocultar evento**](hide-event.md), [ **VisibilityCause**](visibilitycause-property.md)


 

 





