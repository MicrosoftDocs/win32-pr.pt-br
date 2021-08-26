---
description: Um contexto de dispositivo privado permite que um aplicativo evite recuperar e inicializar um contexto de dispositivo de exibição sempre que o aplicativo precisa desenhar em uma janela.
ms.assetid: 8de5a14b-a8b3-42a5-81f3-bf3c357052cb
title: Contextos de dispositivo de exibição privada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ce63fddbc2e351b166308c9ca3ce674be1a0026851af7bb1192c49cc961cdee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092876"
---
# <a name="private-display-device-contexts"></a>Contextos de dispositivo de exibição privada

Um *contexto de dispositivo* privado permite que um aplicativo evite recuperar e inicializar um contexto de dispositivo de exibição sempre que o aplicativo precisa desenhar em uma janela. Os contextos de dispositivo privado são úteis para janelas que exigem muitas alterações nos valores dos atributos do contexto do dispositivo para prepará-lo para desenho. Os contextos de dispositivo privado reduzem o tempo necessário para preparar o contexto do dispositivo e, portanto, o tempo necessário para realizar o desenho na janela.

Um aplicativo direciona o sistema a criar um contexto de dispositivo privado para uma janela especificando o estilo OWNDC do CS \_ na classe de janela. O sistema cria um contexto de dispositivo privado exclusivo sempre que cria uma nova janela que pertence à classe . Inicialmente, o contexto do dispositivo privado tem os mesmos valores padrão para atributos como um contexto de dispositivo comum, mas o aplicativo pode modificá-los a qualquer momento. O sistema preserva as alterações no contexto do dispositivo durante a vida útil da janela ou até que o aplicativo faça alterações adicionais.

Um aplicativo pode recuperar um handle para o contexto do dispositivo privado usando a [**função GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) a qualquer momento após a criação da janela. O aplicativo deve recuperar o alça apenas uma vez. Depois disso, ele pode manter e usar o lidar com qualquer número de vezes. Como um contexto de dispositivo privado não faz parte do cache de contexto do dispositivo de exibição, um aplicativo nunca precisa liberar o contexto do dispositivo usando a [**função ReleaseDC.**](/windows/desktop/api/Winuser/nf-winuser-releasedc)

O sistema ajusta automaticamente o contexto do dispositivo para refletir as alterações na janela, como movimentação ou tamanho. Isso garante que todas as janelas sobrepostas sempre sejam recortados corretamente; ou seja, nenhuma ação é exigida pelo aplicativo para garantir o recorte. No entanto, o sistema não revisa o contexto do dispositivo para incluir a região de atualização. Portanto, ao processar uma mensagem [**WM \_ PAINT,**](wm-paint.md) o aplicativo deve incorporar a região de atualização chamando [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) ou recuperando a região de atualização e intersecndo-a com a região de recorte atual. Se o aplicativo não chamar **BeginPaint**, ele deverá validar explicitamente a região de atualização usando a [**função ValidateRect**](/windows/desktop/api/Winuser/nf-winuser-validaterect) ou [**ValidateRgn.**](/windows/desktop/api/Winuser/nf-winuser-validatergn) Se o aplicativo não validar a região de atualização, a janela receberá uma série infinita de **mensagens WM \_ PAINT.**

Como [**BeginPaint oculta**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) o achamado se uma janela estiver sendo exibido, um aplicativo que chama **BeginPaint** também deve chamar a [**função EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) para restaurar o caret. **EndPaint** não tem nenhum outro efeito em um contexto de dispositivo privado.

Embora um contexto de dispositivo privado seja conveniente de usar, ele faz uso intensivo de memória em termos de recursos do sistema, exigindo 800 ou mais bytes para armazenar. Os contextos de dispositivo privado são recomendados quando as considerações de desempenho superam os custos de armazenamento.

O sistema inclui o contexto do dispositivo privado ao enviar a mensagem [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) para o aplicativo. As seleções atuais do contexto do dispositivo privado, incluindo o modo de mapeamento, estão em vigor quando o aplicativo ou o sistema processa essas mensagens. Para evitar efeitos indesejáveis, o sistema usa coordenadas lógicas ao apagar o plano de fundo; por exemplo, ele usa a [**função GetClipBox**](/windows/desktop/api/Wingdi/nf-wingdi-getclipbox) para recuperar as coordenadas lógicas da área para apagar e passa essas coordenadas para a [**função FillRect.**](/windows/desktop/api/Winuser/nf-winuser-fillrect) Aplicativos que processam essas mensagens podem usar técnicas semelhantes.

Um aplicativo pode usar a [**função GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) para forçar o sistema a retornar um contexto de dispositivo comum para a janela que tem um contexto de dispositivo privado. Isso é útil para realizar toques rápidos em uma janela sem alterar os valores atuais dos atributos do contexto do dispositivo privado.

 

 
