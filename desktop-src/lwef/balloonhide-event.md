---
title: Evento BalloonHide
description: Evento BalloonHide
ms.assetid: dd1f3e83-f3d9-496e-9a54-b3a23b2403da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 062a82afcabb3597ca8c254e039c231b52033657
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160338"
---
# <a name="balloonhide-event"></a>Evento BalloonHide

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Ocorre quando o balão de palavra de um caractere é ocultado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

**Sub** *Agent* \_ **BalloonHide** **(ByVal** *characterid * * *)**



| Parte          | Descrição                                                       |
|---------------|-------------------------------------------------------------------|
| *Caractere de caracteres* | Retorna a ID do caractere associado à palavra balão. |



 

</dd> </dl>

### <a name="remarks"></a>Comentários

O servidor envia esse evento somente para os clientes do caractere (aplicativos que carregaram o caractere) que usa o balão de palavra.

### <a name="see-also"></a>Consulte Também

[**Evento BalloonShow**](balloonshow-event.md)


 

 




