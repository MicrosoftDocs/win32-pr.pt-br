---
title: Propriedade BackColor (recursos Windows ambiente herdado)
description: Propriedade BackColor
ms.assetid: a82c23bc-b280-4a52-9272-68879557cac7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f799e8b9e00a97770cd004e29df75da8345a6cc01531fce53079ea550402c68d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114806"
---
# <a name="backcolor-property-legacy-windows-environment-features"></a>Propriedade BackColor (recursos Windows ambiente herdado)

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**
</dt> <dd>

Retorna a cor da tela de fundo exibida atualmente na janela de balão de palavra para o caractere especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agent***. Caracteres ("**_CharacterID_*_"). Balloon.BackColor_*

</dd> </dl>

## <a name="remarks"></a>Comentários

O intervalo válido para uma cor RGB normal é de 0 a 16.777.215 (&HFFFFFF). O byte alto de um número nesse intervalo é igual a 0; os 3 bytes inferiores, do byte mínimo ao mais significativo, determinam a quantidade de vermelho, verde e azul, respectivamente. Cada um dos componentes vermelho, verde e azul é representado por um número entre 0 e 255 (&HFF).

 

 




