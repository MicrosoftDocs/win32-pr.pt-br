---
title: Mover evento
description: Mover evento
ms.assetid: 973e9e68-edbb-4741-b50e-57db96712df8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31facb1d57b807fb0322783a291b77ef5a7c1487
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822664"
---
# <a name="move-event"></a>Mover evento

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Ocorre quando um caractere é movido.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

 Movimentação de *subagente* \_ **(ByVal** *caractereid*, **ByVal** *X*, **ByVal** *Y*, **ByVal** *causa * * *)**



| Parte          | Descrição                                                                                                                                                                                                                                                                                                                                   |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Caractere de caracteres* | Retorna a ID do caractere movido.                                                                                                                                                                                                                                                                                                   |
| *X*           | Retorna a coordenada x (em pixels) da borda superior do novo local do quadro de caracteres como um inteiro.                                                                                                                                                                                                                                         |
| *S*           | Retorna a coordenada y (em pixels) da borda esquerda do novo local do quadro de caracteres como um inteiro.                                                                                                                                                                                                                                        |
| *Causa*       | Retorna um valor que indica o que causou a movimentação do caractere. 1 o usuário arrastou o caractere.<br/> 2 o aplicativo cliente moveu o caractere.<br/> 3 outro aplicativo cliente moveu o caractere.<br/> 4 o servidor do agente moveu o caractere para mantê-lo na tela após a alteração da resolução da tela.<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Comentários

Esse evento ocorre quando o usuário ou um aplicativo altera a posição do caractere. As coordenadas são relevantes para o canto superior esquerdo da tela. Esse evento é enviado somente para os clientes do caractere (aplicativos que carregaram o caractere).

**Consulte também**

[**Propriedade MoveCause**](movecause-property.md), [ **evento size**](size-event.md)

 

 





