---
description: Usando um contexto de dispositivo de classe, um aplicativo pode usar um único contexto de dispositivo de exibição para cada janela que pertence a uma classe especificada.
ms.assetid: fc76abbf-68da-47f2-8145-4fad806297b4
title: A classe exibe contextos de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b8e4ca7f7d51f3dd50f50a07ab44496d56e4a78effb78f33e9eed6f5ffc3745
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062476"
---
# <a name="class-display-device-contexts"></a>A classe exibe contextos de dispositivo

Usando um *contexto de dispositivo de classe*, um aplicativo pode usar um único contexto de dispositivo de exibição para cada janela que pertence a uma classe especificada. Os contextos de dispositivo de classe geralmente são usados com janelas de controle que são desenhadas usando os mesmos valores de atributo. Assim como os contextos de dispositivo privado, os contextos de dispositivo de classe minimizam o tempo necessário para preparar um contexto de dispositivo para o desenho.

O sistema fornece um contexto de dispositivo de classe para uma janela se ele pertence a uma classe de janela que tem o \_ estilo cs CLASSDC. O sistema cria o contexto do dispositivo ao criar a primeira janela que pertence à classe e, em seguida, usa o mesmo contexto de dispositivo para todas as janelas criadas subsequentemente na classe. Inicialmente, o contexto do dispositivo de classe tem os mesmos valores padrão para atributos como um contexto de dispositivo comum, mas o aplicativo pode modificá-los a qualquer momento. O sistema preserva todas as alterações, exceto a região de recorte e a origem do dispositivo, até que a última janela na classe tenha sido destruída. Uma alteração feita para uma janela se aplica a todas as janelas nessa classe.

Um aplicativo pode recuperar o identificador para o contexto do dispositivo de classe usando a função [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) a qualquer momento após a primeira janela ter sido criada. O aplicativo pode manter e usar o identificador sem liberá-lo porque o contexto do dispositivo de classe não faz parte do cache de contexto do dispositivo de vídeo. Se o aplicativo criar outra janela na mesma classe de janela, o aplicativo deverá recuperar o contexto do dispositivo de classe novamente. A recuperação do contexto do dispositivo define a origem de dispositivo e a região de recorte corretas para a nova janela. Depois que o aplicativo recupera o contexto do dispositivo de classe para uma nova janela na classe, o contexto do dispositivo não pode mais ser usado para desenhar na janela original sem recuperá-lo novamente para essa janela. Em geral, cada vez que ele deve desenhar em uma janela, um aplicativo deve recuperar explicitamente o contexto do dispositivo de classe para a janela.

Os aplicativos que usam contextos de dispositivo de classe sempre devem chamar [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) ao processar uma mensagem de [**\_ pintura do WM**](wm-paint.md) . A função define a origem do dispositivo e a região de recorte corretas para a janela e incorpora a região de atualização. O aplicativo também deve chamar [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) para restaurar o cursor se **BeginPaint** o HID. **EndPaint** não tem nenhum outro efeito em um contexto de dispositivo de classe.

O sistema passa o contexto do dispositivo de classe ao enviar a mensagem do [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) para o aplicativo, permitindo que os valores de atributo atuais afetem qualquer desenho realizado pelo aplicativo ou pelo sistema ao processar essa mensagem. Como poderia fazer com que uma janela tenha um contexto de dispositivo privado, um aplicativo pode usar [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) para forçar o sistema a retornar um contexto de dispositivo comum para a janela que tem um contexto de dispositivo de classe.

O uso de contextos de dispositivo de classe não é recomendado.

 

 
