---
description: Esse atributo permite que um controle de texto exiba o número aproximado de minutos e segundos restantes para uma instalação.
ms.assetid: e1302449-7f80-4881-bd76-49d386bfdafb
title: Atributo de controle timepersisting
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 668cabe4832e6460b4ab01fcc048e2f8e1bbdf66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169837"
---
# <a name="timeremaining-control-attribute"></a>Atributo de controle timepersisting

Esse atributo permite que um controle de texto exiba o número aproximado de minutos e segundos restantes para uma instalação. Um registro passado para o controle de texto contém um inteiro que representa o número de segundos restantes. O controle de texto pesquisa a [tabela UIText](uitext-table.md) em busca de uma cadeia de caracteres chamada timecontinueing e formata o inteiro em uma cadeia de caracteres apropriada que exibe minutos e segundos.

## <a name="valid-controls"></a>Controles válidos

[Text](text-control.md)

## <a name="associated-bit-flags"></a>Sinalizadores de bits associados

Este atributo não usa sinalizadores de bit.

## <a name="remarks"></a>Comentários

Consulte [atributos de controle](control-attributes.md) e o controle que você precisa criar sob [controles](controls.md).

 

 



