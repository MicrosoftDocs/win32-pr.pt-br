---
title: Propriedade MoveCause
description: Propriedade MoveCause
ms.assetid: 8f78a6da-8498-4a39-a4b9-5ab7a43d97f5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc7f91d068befa2b919c04818c46dbc1a48faa0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822665"
---
# <a name="movecause-property"></a>Propriedade MoveCause

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Retorna um valor inteiro que especifica o que causou a última movimentação do caractere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agente* do. **Caracteres ("***characterid***"). MoveCause**



| Valor | Descrição                                                                                |
|-------|--------------------------------------------------------------------------------------------|
| 0     | O caractere não foi movido.                                                          |
| 1     | O usuário moveu o caractere.                                                              |
| 2     | Seu aplicativo moveu o caractere.                                                      |
| 3     | Outro aplicativo cliente moveu o caractere.                                            |
| 4     | O servidor do agente moveu o caractere para mantê-lo na tela após a alteração da resolução da tela. |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Você pode usar essa propriedade para determinar o que causou o caractere a ser movido, quando mais de um aplicativo estiver compartilhando (carregado) o mesmo caractere. Esses valores são os mesmos retornados pelo evento de [**movimentação**](move-event.md) .

## <a name="see-also"></a>Consulte Também

[**Mover evento**](move-event.md), [ **método MoveTo**](moveto-method.md)


 

 




