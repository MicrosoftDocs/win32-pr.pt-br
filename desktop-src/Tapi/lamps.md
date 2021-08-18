---
description: As lâmpadas em um dispositivo de telefone podem ser acesas em uma variedade de modos de iluminação diferentes.
ms.assetid: d8e8ef57-9faa-4122-b99a-3956362cd9d8
title: Lâmpadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 150e499dbd66ca772d35855c4cdb086bbb1ecc12617f55bcd33dccf8435e8771
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117762280"
---
# <a name="lamps"></a>Lâmpadas

As lâmpadas em um dispositivo de telefone podem ser acesas em uma variedade de modos de iluminação diferentes. Ao contrário dos padrões de toque, os modos de lâmpada são mais uniformes em conjuntos de telefone de diferentes fornecedores. Um conjunto comum de modos de lâmpada é definido pela API. Uma lâmpada identificada por seu identificador de botão de lâmpada pode ser acesa em um determinado modo de lâmpada. Uma lâmpada também pode ser consultada para o seu modo de lâmpada atual.

As funções TAPI usadas para lâmpadas são [**phoneSetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonesetlamp), que acende uma lâmpada em um dispositivo de telefone aberto especificado em um determinado modo de iluminação e [**phoneGetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonegetlamp), que retorna o modo de lâmpada atual da lâmpada especificada.

Quando uma lâmpada de um dispositivo de telefone é alterada, uma mensagem de [**\_ estado de telefone**](phone-state.md) é enviada ao aplicativo para notificar o aplicativo sobre a alteração de estado. Os parâmetros dessa mensagem fornecem uma indicação da alteração.

 

 



