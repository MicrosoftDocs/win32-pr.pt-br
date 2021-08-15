---
title: Mover evento
description: Mover evento
ms.assetid: 973e9e68-edbb-4741-b50e-57db96712df8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9938f79a0c23340c5ed34be52019afe5f9f3fa6caefb6920941cb17dc13c0fc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118476344"
---
# <a name="move-event"></a>Mover evento

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**
</dt> <dd>

Ocorre quando um caractere é movido.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

**Movimentação**  \_ **de sub-agente (ByVal** *CharacterID,* **ByVal** *X,* **ByVal** *Y,* **ByVal** *Cause***)**



| Parte          | Descrição                                                                                                                                                                                                                                                                                                                                   |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Retorna a ID do caractere que foi movido.                                                                                                                                                                                                                                                                                                   |
| *X*           | Retorna a coordenada x (em pixels) da borda superior do novo local do quadro de caracteres como um inteiro.                                                                                                                                                                                                                                         |
| *S*           | Retorna a coordenada y (em pixels) da borda esquerda do novo local do quadro de caracteres como um inteiro.                                                                                                                                                                                                                                        |
| *Causa*       | Retorna um valor que indica o que causou a movimentação do caractere. 1 O usuário arrastou o caractere.<br/> 2 Seu aplicativo cliente moveu o caractere.<br/> 3 Outro aplicativo cliente moveu o caractere.<br/> 4 O servidor do Agent moveu o caractere para mantê-lo na tela após uma alteração na resolução da tela.<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Comentários

Esse evento ocorre quando o usuário ou um aplicativo altera a posição do caractere. As coordenadas são relevantes para o canto superior esquerdo da tela. Esse evento é enviado somente aos clientes do caractere (aplicativos que carregaram o caractere).

**Consulte também**

[**Propriedade MoveCause**](movecause-property.md), [ **evento size**](size-event.md)

 

 





