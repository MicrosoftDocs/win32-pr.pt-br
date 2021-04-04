---
title: Visão geral dos gestos do Windows Touch
description: Esta seção descreve os vários gestos com suporte do Windows Touch.
ms.assetid: b2fa11a7-9abb-4149-96e3-e8c663c29d4a
keywords:
- Toque do Windows, gestos
- gestos, sobre
- Windows Touch, suporte herdado
- gestos, suporte herdado
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: 2290477aa8b26e937fe6d5f300ed1fea32872f5d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007838"
---
# <a name="windows-touch-gestures-overview"></a>Visão geral dos gestos do Windows Touch

Esta seção descreve os vários gestos com suporte do Windows Touch.

## <a name="gestures-overview"></a>Visão geral dos gestos

O Windows Touch permite vários gestos que dão suporte a um e vários contatos. A imagem a seguir ilustra os vários gestos com suporte no Windows 7.

![ilustração mostrando os gestos com suporte do Windows Touch no Windows 7](images/gestures.png)

> [!Note]  
> Alguns reconhecedores são mais confiáveis na interpretação de gestos com vários contatos quando os contatos estão mais distantes uns dos outros.

## <a name="legacy-support"></a>Suporte herdado

Para suporte herdado, o manipulador de gestos padrão mapeia alguns gestos para mensagens do Windows que foram usadas em versões anteriores do Windows. A tabela a seguir descreve como os gestos são mapeados para mensagens herdadas.

| Gesto        | Descrição  | Mensagem (ns) gerada (s)              |
|----------------|----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| Panorâmica            | O gesto de panorâmica é mapeado para usar a roda de rolagem.                  | **WM_VSCROLL**<br/> **WM_HSCROLL**<br/>       |
| Pressionar e manter pressionado | O gesto de pressionar e segurar é mapeado para o clique com o botão direito do mouse.     | **WM_RBUTTONDOWN**<br/> **WM_RBUTTONUP**<br/> |
| Zoom           | O gesto de zoom dispara mensagens que são semelhantes à retenção da tecla CTRL e gira a roda do mouse para rolar. | **WM_MOUSEWHEEL** com **MK_CONTROL** definido no *lParam* |

## <a name="interpreting-windows-touch-gestures"></a>Interpretando gestos de toque do Windows

Os gestos de toque do Windows podem ser interpretados por desenvolvedores de aplicativos manipulando a mensagem [**WM_GESTURE**](wm-gesture.md) da função WndProc de um aplicativo. Depois de manipular essa mensagem, você pode recuperar uma estrutura [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) que descreve o gesto. A estrutura **GESTUREINFO** terá informações classificadas que dependem do tipo de gesto.

A estrutura [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) é recuperada passando o identificador para a estrutura de informações de gesto para a função [**GetGestureInfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo) .

Os sinalizadores a seguir indicam os vários Estados dos gestos e são armazenados no *dwFlags*. 

| Nome        | Valor      | Descrição                      |
|-------------|------------|----------------------------------|
| GF_BEGIN   | 0x00000001 | Um gesto está sendo iniciado.           |
| GF_INERTIA | 0x00000002 | Um gesto disparou inércia. |
| GF_END     | 0x00000004 | Um gesto foi concluído.          |

> [!Note]  
> A maioria dos aplicativos deve ignorar o **GID_BEGIN** e **GID_END** e passá-los para [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca). Essas mensagens são usadas pelo manipulador de gestos padrão. O comportamento do aplicativo é indefinido quando as mensagens de **GID_BEGIN** e **GID_END** são consumidas por um aplicativo de terceiros.

A tabela a seguir indica os vários identificadores para gestos. 

| Nome              | Valor | Descrição                 |
|-------------------|-------|-----------------------------|
| GID_BEGIN        | 1     | Um gesto está sendo iniciado.      |
| GID_END          | 2     | Um gesto está terminando.        |
| GID_ZOOM         | 3     | O gesto de zoom.           |
| GID_PAN          | 4     | O gesto de panorâmica.            |
| GID_ROTATE       | 5     | O gesto de rotação.       |
| GID_TWOFINGERTAP | 6     | Gesto de toque de dois dedos. |
| GID_PRESSANDTAP  | 7     | O gesto de pressionar e tocar.  |

> [!Note]  
> O gesto de **GID_PAN** tem inércia internos. No final de um gesto de Pan, mensagens de gesto de panorâmica adicionais são criadas pelo sistema operacional.

Os membros da estrutura [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) **ptsLocation** e **ullArguments** especificam um ponto (usando a estrutura de **pontos** ) e informações adicionais sobre gestos, dependendo do gesto. A tabela a seguir lista os valores associados a cada tipo de gesto.

| ID do gesto            | *ullArguments*                  | *ptsLocation*                       |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| **GID_ZOOM**         | Indica a distância entre os dois pontos.            | Indica o centro do zoom.   |
| **GID_PAN**          | Indica a distância entre os dois pontos.            | Indica a posição atual da Pan.                    |
| **GID_ROTATE**       | Indica o ângulo de rotação se o sinalizador de **GF_BEGIN** estiver definido. Caso contrário, essa é a alteração de ângulo desde que a rotação foi iniciada. Isso é assinado para indicar a direção da rotação. Use as macros [**GID_ROTATE_ANGLE_FROM_ARGUMENT**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_from_argument) e [**GID_ROTATE_ANGLE_TO_ARGUMENT**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_to_argument) para obter e definir o valor do ângulo. | Isso indica o centro da rotação que é o ponto estacionário no qual o objeto de destino é girado. |
| **GID_TWOFINGERTAP** | Indica a distância entre os dois dedos.           | Indica o centro dos dois dedos.                      |
| **GID_PRESSANDTAP**  | Indica o Delta entre o primeiro dedo e o segundo dedo. Esse valor é armazenado em uma estrutura de **ponto** no menor 32 bits do membro *ullArguments* .                        | Indica a posição em que o primeiro dedo se resume.   |

## <a name="related-topics"></a>Tópicos relacionados

[Gestos de toque do Windows](guide-multi-touch-gestures.md)