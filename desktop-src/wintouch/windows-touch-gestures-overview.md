---
title: Windows Visão geral dos gestos de toque
description: Esta seção descreve os vários gestos com suporte do Windows Touch.
ms.assetid: b2fa11a7-9abb-4149-96e3-e8c663c29d4a
keywords:
- Windows Toque, gestos
- gestos, sobre
- Windows Toque, suporte herddo
- gestos, suporte herddo
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: f2a0f6229afe4ad0d894a1cc2d40489f5d8371de3d7c42cefdccde619119df75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119587246"
---
# <a name="windows-touch-gestures-overview"></a>Windows Visão geral dos gestos de toque

Esta seção descreve os vários gestos com suporte do Windows Touch.

## <a name="gestures-overview"></a>Visão geral dos gestos

Windows O toque permite vários gestos que suportam contatos individuais e múltiplos. A imagem a seguir ilustra os vários gestos com suporte no Windows 7.

![ilustração mostrando os gestos que o Windows Touch dá suporte no Windows 7](images/gestures.png)

> [!Note]  
> Alguns reconhecedores são mais confiáveis na interpretação de gestos com vários contatos quando os contatos estão mais distantes uns dos outros.

## <a name="legacy-support"></a>Suporte herddo

Para suporte herdado, o manipulador de gestos padrão mapeia alguns gestos para Windows mensagens que foram usadas em versões anteriores do Windows. A tabela a seguir descreve como os gestos são mapeadas para mensagens herdadas.

| Gesto        | Descrição  | Mensagens geradas              |
|----------------|----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| Panorâmica            | O gesto de panoragem mapeia para usando a roda de rolagem.                  | **Wm_vscroll**<br/> **Wm_hscroll**<br/>       |
| Pressionar e manter pressionado | O gesto de pressionar e segurar é mapeando para clicar com o botão direito do mouse.     | **Wm_rbuttondown**<br/> **WM_RBUTTONUP**<br/> |
| Zoom           | O gesto de zoom dispara mensagens semelhantes a manter a tecla CTRL e girar a roda do mouse para rolar. | **WM_MOUSEWHEEL** com **MK_CONTROL** definido no *lParam* |

## <a name="interpreting-windows-touch-gestures"></a>Interpretando Windows gestos de toque

Windows Gestos de toque podem ser interpretados por desenvolvedores de aplicativos manipulando [**a mensagem WM_GESTURE**](wm-gesture.md) da função WndProc de um aplicativo. Depois de lidar com essa mensagem, você pode recuperar uma estrutura [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) que descreve o gesto. A **estrutura GESTUREINFO** terá informações assortadas que dependem do tipo de gesto.

A [**estrutura GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) é recuperada passando o handle para a estrutura de informações de gesto para a [**função GetGestureInfo.**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo)

Os sinalizadores a seguir indicam os vários estados dos gestos e são armazenados *em dwFlags*. 

| Nome        | Valor      | Descrição                      |
|-------------|------------|----------------------------------|
| GF_BEGIN   | 0x00000001 | Um gesto está começando.           |
| GF_INERTIA | 0x00000002 | Um gesto disparou a inércia. |
| GF_END     | 0x00000004 | Um gesto foi concluído.          |

> [!Note]  
> A maioria dos aplicativos **deve ignorar GID_BEGIN** e **GID_END** e passá-los para [DefWindowProc.](/windows/win32/api/winuser/nf-winuser-defwindowproca) Essas mensagens são usadas pelo manipulador de gestos padrão. O comportamento do aplicativo é  indefinido quando GID_BEGIN e **GID_END** mensagens são consumidas por um aplicativo de terceiros.

A tabela a seguir indica os vários identificadores para gestos. 

| Nome              | Valor | Descrição                 |
|-------------------|-------|-----------------------------|
| GID_BEGIN        | 1     | Um gesto está começando.      |
| GID_END          | 2     | Um gesto está terminando.        |
| GID_ZOOM         | 3     | O gesto de zoom.           |
| GID_PAN          | 4     | O gesto de panorcar.            |
| GID_ROTATE       | 5     | O gesto de rotação.       |
| GID_TWOFINGERTAP | 6     | O gesto de toque com dois dedos. |
| GID_PRESSANDTAP  | 7     | O gesto de pressionar e tocar.  |

> [!Note]  
> O **GID_PAN** gesto tem inércia integrado. No final de um gesto de panorático, mensagens de gesto de panorático adicionais são criadas pelo sistema operacional.

Os membros da estrutura [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) **ptsLocation** e **ullArguments** especificam um ponto (usando a estrutura **POINTS)** e informações adicionais sobre gestos dependendo do gesto. A tabela a seguir lista os valores associados a cada tipo de gesto.

| ID do gesto            | *ullArguments*                  | *ptsLocation*                       |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| **GID_ZOOM**         | Indica a distância entre os dois pontos.            | Indica o centro do zoom.   |
| **GID_PAN**          | Indica a distância entre os dois pontos.            | Indica a posição atual do painel.                    |
| **GID_ROTATE**       | Indica o ângulo de rotação se Se o **sinalizador GF_BEGIN** estiver definido. Caso contrário, essa é a alteração de ângulo desde que a rotação foi iniciada. Isso é assinado para indicar a direção da rotação. Use as [**macros GID_ROTATE_ANGLE_FROM_ARGUMENT**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_from_argument) [**e GID_ROTATE_ANGLE_TO_ARGUMENT**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_to_argument) para obter e definir o valor do ângulo. | Isso indica o centro da rotação, que é o ponto estacionário em que o objeto de destino é girado. |
| **GID_TWOFINGERTAP** | Indica a distância entre os dois dedos.           | Indica o centro dos dois dedos.                      |
| **GID_PRESSANDTAP**  | Indica o delta entre o primeiro dedo e o segundo dedo. Esse valor é armazenado em uma estrutura de **ponto** no menor 32 bits do membro *ullArguments* .                        | Indica a posição em que o primeiro dedo se resume.   |

## <a name="related-topics"></a>Tópicos relacionados

[Windows Gestos de toque](guide-multi-touch-gestures.md)