---
description: Alguns conjuntos de telefone oferecem suporte à noção de baixar dados do ou carregar dados para o dispositivo de telefone, o que permite que o conjunto de telefone seja programado de várias maneiras.
ms.assetid: 5734107d-8104-4d8a-b3f7-3cc2a48f71ca
title: Áreas de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed05d6233a8c8ed31a2d00d28970a517ef181f00689c7da34673d3044fffb4dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117946139"
---
# <a name="data-areas"></a>Áreas de dados

Alguns conjuntos de telefone oferecem suporte à noção de baixar dados do ou carregar dados para o dispositivo de telefone, o que permite que o conjunto de telefone seja programado de várias maneiras. A TAPI modela esses conjuntos de telefone como tendo uma ou mais áreas de download ou de upload. Cada área é identificada por um número que varia de zero para o número de áreas de dados disponíveis no telefone menos uma. Os tamanhos de cada área podem variar. O formato dos dados em si é específico do dispositivo.

A função TAPI [**phoneSetData**](/windows/desktop/api/Tapi/nf-tapi-phonesetdata) baixa um buffer de dados para uma determinada área de dados no dispositivo de telefone, e a função [**phoneGetData**](/windows/desktop/api/Tapi/nf-tapi-phonegetdata) carrega o conteúdo de uma determinada área de dados no dispositivo de telefone para um buffer.

Quando uma área de dados de um dispositivo de telefone é alterada, uma mensagem de [**\_ estado de telefone**](phone-state.md) é enviada ao aplicativo para notificar o aplicativo sobre a alteração de estado. Os parâmetros dessa mensagem fornecem uma indicação da alteração.

 

 



