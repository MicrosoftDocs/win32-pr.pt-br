---
title: Evento BalloonShow
description: Evento BalloonShow
ms.assetid: 8a73e883-c003-480b-8a0a-e699caffe54c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de67318b02775619332fe60ea47fb27edb893c8b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364264"
---
# <a name="balloonshow-event"></a>Evento BalloonShow

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Ocorre quando o balão de palavra de um caractere é mostrado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

**Sub** *Agent* \_ **BalloonShow** **(ByVal** *characterid * * *)**



| Parte          | Descrição                                                       |
|---------------|-------------------------------------------------------------------|
| *Caractere de caracteres* | Retorna a ID do caractere associado à palavra balão. |



 

</dd> </dl>

### <a name="remarks"></a>Comentários

O servidor envia esse evento somente para os clientes do caractere (aplicativos que carregaram o caractere) que usa o balão de palavra.

### <a name="see-also"></a>Consulte Também

[**Evento BalloonHide**](balloonhide-event.md)


 

 




