---
title: Mensagem de WM_GESTURE (WinUser. h)
description: Passa informações sobre um gesto.
ms.assetid: 4167aeb0-2c31-4b7b-ad1b-e6d37da09ef8
keywords:
- WM_GESTURE a mensagem Windows Touch
topic_type:
- apiref
api_name:
- WM_GESTURE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d1184d1f54d110f84630a727decb91ad28e6c08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369756"
---
# <a name="wm_gesture-message"></a>Mensagem de gesto do WM \_

Passa informações sobre um gesto.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Fornece informações que identificam o comando de gesto e os valores de argumento específicos do gesto. Essas informações são as mesmas informações passadas para o membro **ullArguments** da estrutura [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) .

</dd> <dt>

*lParam* 
</dt> <dd>

Fornece um identificador para informações que identificam o comando de gesto e os valores de argumento específicos do gesto. Essas informações são recuperadas chamando [**GetGestureInfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se um aplicativo processar essa mensagem, ele deverá retornar 0.

Se o aplicativo não processar a mensagem, ele deverá chamar [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca). Não fazer isso fará com que o aplicativo vazasse memória porque o identificador de entrada por toque não será fechado e a memória do processo associada não será liberada.

## <a name="remarks"></a>Comentários

A tabela a seguir lista os comandos de gesto com suporte.



| ID do gesto            | Valor (*dwID*) | Descrição                                                                                                                                                                                                                                                                          |
|-----------------------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **início de GID \_**        | 1              | Indica que um gesto genérico está começando.                                                                                                                                                                                                                                            |
| **fim do GID \_**          | 2              | Indica uma extremidade de gesto genérico.                                                                                                                                                                                                                                                     |
| **ZOOM de GID \_**         | 3              | Indica início do zoom, movimentação de zoom ou parada de zoom. A primeira mensagem de comando de **\_ zoom GID** começa um zoom, mas não causa nenhum zoom. O segundo comando **GID de \_ zoom** dispara um zoom relativo ao estado contido no primeiro **\_ zoom GID**.                                    |
| **deslocamento de GID \_**          | 4              | Indica a movimentação de panorâmica ou o início da panorâmica. O primeiro comando de **\_ Pan de GID** indica um início panorâmico, mas não executa nenhum movimento panorâmico. Com a segunda mensagem de comando de **\_ Pan de GID** , o aplicativo começará a panorâmica.                                                                            |
| **rotação de GID \_**       | 5              | Indica o movimento de girar ou girar para começar. A primeira mensagem de comando **GID \_ Rotate** indica uma movimentação de giro ou de giro, mas não será girada. A segunda mensagem de comando **GID \_ Rotate** disparará uma operação de rotação relativa ao estado contido na primeira **\_ rotação de GID**. |
| **GID \_ TWOFINGERTAP** | 6              | Indica gesto de toque com dois dedos.                                                                                                                                                                                                                                                    |
| **GID \_ PRESSANDTAP**  | 7              | Indica o gesto de pressionar e tocar.                                                                                                                                                                                                                                                 |



 

> [!Note]  
> Para habilitar o suporte herdado, as mensagens com os comandos de gesto de **\_ encerramento** de **GID \_ begin** e GID precisam ser encaminhadas usando [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).

 

A tabela a seguir indica os argumentos de gestos passados nos parâmetros *lParam* e *wParam* .



| ID do gesto            | Gesto        | *ullArgument*                                                                                                                                                                                                                                                                                                                                                                                            | *ptsLocation* na estrutura [**GestureInfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo)                                                  |
|-----------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| **ZOOM de GID \_**         | Ampliar/reduzir    | Indica a distância entre os dois pontos.                                                                                                                                                                                                                                                                                                                                                           | Indica o centro do zoom.                                                                                 |
| **deslocamento de GID \_**          | Panorâmica            | Indica a distância entre os dois pontos.                                                                                                                                                                                                                                                                                                                                                           | Indica a posição atual da Pan.                                                                        |
| **rotação de GID \_**       | Girar (pivô) | Indica o ângulo de rotação se o sinalizador de **\_ início GF** estiver definido. Caso contrário, essa é a alteração de ângulo desde que a rotação foi iniciada. Isso é assinado para indicar a direção da rotação. Use o [**ângulo \_ \_ de giro \_ de GID de \_ argumento**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_from_argument) e o ângulo de rotação de GID para macros de [**\_ \_ \_ \_ argumento**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_to_argument) para obter e definir o valor de ângulo. | Isso indica o centro da rotação que é o ponto estacionário no qual o objeto de destino é girado. |
| **GID \_ TWOFINGERTAP** | Toque com dois dedos | Indica a distância entre os dois dedos.                                                                                                                                                                                                                                                                                                                                                          | Indica o centro dos dois dedos.                                                                          |
| **GID \_ PRESSANDTAP**  | Pressione e toque em  | Indica o Delta entre o primeiro dedo e o segundo dedo. Esse valor é armazenado nos menores 32 bits do *ullArgument* em uma estrutura de **ponto** .                                                                                                                                                                                                                                             | Indica a posição em que o primeiro dedo se resume.                                                       |



 

> [!Note]  
> Todas as distâncias e posições são fornecidas em coordenadas de tela físicas.

 

> [!Note]  
> Os parâmetros *dwID* e *ullArgument* só devem ser considerados para acompanhar os \_ \* comandos GID e não devem ser alterados por aplicativos.

 

## <a name="examples"></a>Exemplos

O código a seguir ilustra como obter informações específicas do gesto associadas a essa mensagem.

> [!Note]  
> Você sempre deve encaminhar mensagens sem tratamento para [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) e deve fechar o manipulador de entrada de gesto para as mensagens que você manipula com uma chamada para [**CloseGestureInfoHandle**](/windows/desktop/api/winuser/nf-winuser-closegestureinfohandle). Neste exemplo, o comportamento do manipulador de gestos padrão será suprimido porque o identificador TOUCHINPUT é fechado em cada um dos casos de gesto. Se você removeu os casos no código acima para mensagens sem tratamento, o manipulador de gestos padrão processaria as mensagens sendo encaminhados para [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) no caso padrão.

 


```C++
  LRESULT DecodeGesture(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam){
    // Create a structure to populate and retrieve the extra message info.
    GESTUREINFO gi;  
    
    ZeroMemory(&gi, sizeof(GESTUREINFO));
    
    gi.cbSize = sizeof(GESTUREINFO);

    BOOL bResult  = GetGestureInfo((HGESTUREINFO)lParam, &gi);
    BOOL bHandled = FALSE;

    if (bResult){
        // now interpret the gesture
        switch (gi.dwID){
           case GID_ZOOM:
               // Code for zooming goes here     
               bHandled = TRUE;
               break;
           case GID_PAN:
               // Code for panning goes here
               bHandled = TRUE;
               break;
           case GID_ROTATE:
               // Code for rotation goes here
               bHandled = TRUE;
               break;
           case GID_TWOFINGERTAP:
               // Code for two-finger tap goes here
               bHandled = TRUE;
               break;
           case GID_PRESSANDTAP:
               // Code for roll over goes here
               bHandled = TRUE;
               break;
           default:
               // A gesture was not recognized
               break;
        }
    }else{
        DWORD dwErr = GetLastError();
        if (dwErr > 0){
            //MessageBoxW(hWnd, L"Error!", L"Could not retrieve a GESTUREINFO structure.", MB_OK);
        }
    }
    if (bHandled){
        return 0;
    }else{
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
  }
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                               |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                                  |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Notificações](notifications.md)
</dt> <dt>

[Guia de programação de gestos do Windows Touch](guide-multi-touch-gestures.md)
</dt> </dl>

 

