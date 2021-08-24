---
description: Efeito de envelope de volume
ms.assetid: 17b6d842-e79c-49b0-baa4-1535b4a2c6ae
title: Efeito de envelope de volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4ecb66914063596849522a0e4bb340fc84f7d80e5ea1113bfdae2d32e855d3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746946"
---
# <a name="volume-envelope-effect"></a>Efeito de envelope de volume

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O efeito de envelope de volume define o volume em um fluxo de áudio.

ID de classe (CLSID): {036A9790-C153-11D2-9EF7-006008039E37}

Nome da variável CLSID: CLSID \_ AudMixer

Propriedades



| Propriedade | Type   | Padrão | Descrição                                                                                                           |
|----------|--------|---------|-----------------------------------------------------------------------------------------------------------------------|
| Vol      | double | 1.0     | Volume, como uma porcentagem do volume criado. Você pode produzir fades de áudio variando esse valor de propriedade ao longo do tempo. |



 

## <a name="remarks"></a>Comentários

Cada objeto em uma linha do tempo pode ter no máximo um efeito de envelope de volume. Em uma composição ou grupo, o envelope de volume é aplicado primeiro, antes de qualquer outro efeito de áudio, independentemente de sua prioridade. Em uma fonte ou um controle, o efeito do volume é aplicado de acordo com sua prioridade.

 

 



