---
title: Fornecendo controles para cortar e alongar imagens
description: Fornecendo controles para cortar e alongar imagens
ms.assetid: cc62d70d-3f5f-477c-bc09-ab8ab0a9dce3
keywords:
- Macro MCIWndGetSource
- Macro MCIWndPutSource
- Macro MCIWndGetDest
- Macro MCIWndPutDest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cd0889b40204e7c99ec782e454dba2cdeebfe79
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640477"
---
# <a name="providing-controls-for-cropping-and-stretching-images"></a>Fornecendo controles para cortar e alongar imagens

O MCIWnd permite cortar e alongar imagens de um clipe de vídeo. Para entender esses recursos, você precisa entender as relações entre o *tamanho do quadro*, o *retângulo de origem*, o retângulo de *destino* e a *área de reprodução*.

Um clipe de vídeo consiste em vários quadros, cada um contendo uma imagem. O tamanho do quadro de um videoclipe é o tamanho da imagem no quadro atual. Normalmente, um videoclipe tem um tamanho de quadro porque todas as imagens no clipe têm o mesmo tamanho.

O retângulo de origem é uma área retangular que sobrepõe os quadros de um clipe de vídeo. O retângulo de origem define a parte de cada quadro exibido durante a reprodução. Quando um clipe de vídeo é carregado com MCIWnd, o retângulo de origem é inicializado com as mesmas dimensões e posição que o quadro inicial do clipe de vídeo.

O retângulo de destino é uma área retangular que define uma janela de reprodução virtual. O retângulo de destino recebe os dados da imagem do retângulo de origem para cada quadro do clipe de vídeo. Quando as dimensões do retângulo de origem e destino são diferentes, o MCIWnd ajusta os dados de imagem horizontal e verticalmente conforme necessário para preencher o retângulo de destino. Quando um clipe de vídeo é carregado com MCIWnd, o retângulo de destino é inicializado com as mesmas dimensões e posição que o quadro inicial do clipe de vídeo.

A área de reprodução é a parte de uma janela MCIWnd que um aplicativo usa para exibir o clipe de vídeo. A área de reprodução é a área do cliente de uma janela MCIWnd ou a parte da área do cliente que exclui a barra de ferramentas MCIWnd. Quando um clipe de vídeo é carregado com MCIWnd, a área de reprodução é inicializada com as mesmas dimensões e posição que o quadro inicial do clipe de vídeo.

Você pode cortar um clipe de vídeo usando as macros [**MCIWndGetSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource) e [**MCIWndPutSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndputsource) para alterar o retângulo de origem. Cortar uma imagem determina apenas qual parte dos quadros é exibida durante a reprodução; Ele não altera o conteúdo do arquivo que está sendo reproduzido. Antes de cortar uma imagem, você pode recuperar o tamanho atual do retângulo de origem usando **MCIWndGetSource**. Depois que o novo tamanho e o local do retângulo de origem forem calculados, você poderá definir os limites de corte do retângulo de origem usando **MCIWndPutSource**.

Você pode alongar um clipe de vídeo usando as macros [**MCIWndGetDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdest) e [**MCIWndPutDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest) para alterar o retângulo de destino. Ao alongar um clipe de vídeo, você aumenta ou reduz o tamanho do quadro de um clipe de vídeo verticalmente, horizontalmente ou em ambas as direções. Antes de alongar uma imagem, você pode recuperar o tamanho atual e o local do retângulo de destino usando **MCIWndGetDest**. A macro **MCIWndPutDest** permite redefinir o retângulo de destino. O alongamento pode distorcer a imagem durante a reprodução, mas não altera o conteúdo do arquivo que está sendo reproduzido.

Se o tamanho do retângulo de destino se tornar maior que a área de reprodução, você poderá especificar qual parte da área de reprodução exibirá o clipe de vídeo usando **MCIWndPutDest**.

> [!Note]  
> A macro [**MCIWndPutDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest) não altera o tamanho da área de reprodução. Para alongar a janela MCIWnd junto com o retângulo de destino, você precisa saber o tamanho atual da janela MCIWnd e emitir novas dimensões de janela com base no retângulo de destino. Você pode recuperar as dimensões da janela MCIWnd usando a função [GetWindowRect](/windows/win32/api/winuser/nf-winuser-getwindowrect) e redimensionar a janela do MCIWnd usando a função [SetWindowPos](/windows/win32/api/winuser/nf-winuser-setwindowpos) .

 

 

 