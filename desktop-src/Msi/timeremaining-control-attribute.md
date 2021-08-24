---
description: Esse atributo permite que um controle de texto exiba o número aproximado de minutos e segundos restantes para uma instalação.
ms.assetid: e1302449-7f80-4881-bd76-49d386bfdafb
title: Atributo de controle timepersisting
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 907db993731172343418fc92d86f2fbab04cf6f41c2a1627bc76e2cd557f505d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810726"
---
# <a name="timeremaining-control-attribute"></a>Atributo de controle timepersisting

Esse atributo permite que um controle de texto exiba o número aproximado de minutos e segundos restantes para uma instalação. Um registro passado para o controle de texto contém um inteiro que representa o número de segundos restantes. O controle de texto pesquisa a [tabela UIText](uitext-table.md) em busca de uma cadeia de caracteres chamada timecontinueing e formata o inteiro em uma cadeia de caracteres apropriada que exibe minutos e segundos.

## <a name="valid-controls"></a>Controles válidos

[Text](text-control.md)

## <a name="associated-bit-flags"></a>Sinalizadores de bits associados

Este atributo não usa sinalizadores de bit.

## <a name="remarks"></a>Comentários

Consulte [atributos de controle](control-attributes.md) e o controle que você precisa criar sob [controles](controls.md).

 

 



