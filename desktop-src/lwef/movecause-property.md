---
title: Propriedade MoveCause
description: Propriedade MoveCause
ms.assetid: 8f78a6da-8498-4a39-a4b9-5ab7a43d97f5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa797338e64edfd67ae2347f2983df624464df923a64883e3adc5143671b15dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117883827"
---
# <a name="movecause-property"></a>Propriedade MoveCause

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Retorna um valor inteiro que especifica o que causou a última movimentação do caractere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agente* do. **Caracteres ("**_characterid_*_"). MoveCause_*



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


 

 




