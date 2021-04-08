---
description: As lâmpadas em um dispositivo de telefone podem ser acesas em uma variedade de modos de iluminação diferentes.
ms.assetid: d8e8ef57-9faa-4122-b99a-3956362cd9d8
title: Lâmpadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e01005c282b7a86b4b8c8ee27348ba4cf8d43db9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011550"
---
# <a name="lamps"></a>Lâmpadas

As lâmpadas em um dispositivo de telefone podem ser acesas em uma variedade de modos de iluminação diferentes. Ao contrário dos padrões de toque, os modos de lâmpada são mais uniformes em conjuntos de telefone de diferentes fornecedores. Um conjunto comum de modos de lâmpada é definido pela API. Uma lâmpada identificada por seu identificador de botão de lâmpada pode ser acesa em um determinado modo de lâmpada. Uma lâmpada também pode ser consultada para o seu modo de lâmpada atual.

As funções TAPI usadas para lâmpadas são [**phoneSetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonesetlamp), que acende uma lâmpada em um dispositivo de telefone aberto especificado em um determinado modo de iluminação e [**phoneGetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonegetlamp), que retorna o modo de lâmpada atual da lâmpada especificada.

Quando uma lâmpada de um dispositivo de telefone é alterada, uma mensagem de [**\_ estado de telefone**](phone-state.md) é enviada ao aplicativo para notificar o aplicativo sobre a alteração de estado. Os parâmetros dessa mensagem fornecem uma indicação da alteração.

 

 



