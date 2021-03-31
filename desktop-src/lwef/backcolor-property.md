---
title: Propriedade BackColor (recursos de ambiente herdado do Windows)
description: Propriedade BackColor
ms.assetid: a82c23bc-b280-4a52-9272-68879557cac7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3332fcc6a9081b52300dbee4c69c77602e84a62e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103644188"
---
# <a name="backcolor-property-legacy-windows-environment-features"></a>Propriedade BackColor (recursos de ambiente herdado do Windows)

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Retorna a cor do plano de fundo atualmente exibida na janela de balão do caractere especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agente ***. Caracteres ("**_characterid_*_"). Balloon. BackColor_*

</dd> </dl>

## <a name="remarks"></a>Comentários

O intervalo válido para uma cor RGB normal é de 0 a 16.777.215 (&HFFFFFF). O byte alto de um número neste intervalo é igual a 0; os 3 bytes inferiores, do menos ao byte mais significativo, determinam a quantidade de vermelho, verde e azul, respectivamente. Cada um dos componentes vermelho, verde e azul é representado por um número entre 0 e 255 (&HFF).

 

 




