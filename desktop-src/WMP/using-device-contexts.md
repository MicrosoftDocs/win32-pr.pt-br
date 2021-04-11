---
title: Usando contextos de dispositivo
description: Usando contextos de dispositivo
ms.assetid: 2e8de313-6218-4401-a578-73140e7fdae1
keywords:
- visualizações, contexto do dispositivo
- visualizações personalizadas, contexto do dispositivo
- visualizações, função render
- visualizações personalizadas, função render
- Função render, contexto do dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08c315d5004565644750f4adcd099fc165e81575
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292323"
---
# <a name="using-device-contexts"></a>Usando contextos de dispositivo

O contexto do dispositivo é um identificador padrão para um contexto de dispositivo. Você precisa disso para muitas funções de desenho para que o Microsoft Windows saiba em qual janela desenhar. Por exemplo, para desenhar um retângulo, você precisa especificar o contexto do dispositivo.


```C++
HDC hdc;
::Rectangle( hdc, 1, 1, 100, 100 );

```



O contexto do dispositivo é especificado pelo Windows Media Player por meio da função **render** . Se o seu plug-in renderizar usando uma janela, você precisará usar o contexto do dispositivo dessa janela. Use este contexto de dispositivo para qualquer ferramenta de desenho que exija um contexto de dispositivo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Implementando renderização**](implementing-render.md)
</dt> </dl>

 

 




