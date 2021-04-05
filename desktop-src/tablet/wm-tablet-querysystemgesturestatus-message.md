---
description: Enviado quando o sistema solicita uma janela que os gestos do sistema desejam receber.
ms.assetid: 5b747b3c-3b77-4913-932f-182114d1f674
title: Mensagem de WM_TABLET_QUERYSYSTEMGESTURESTATUS (Tpcshrd. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 395196f963cae9b8d18697276e546f1eba05b245
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827072"
---
# <a name="wm_tablet_querysystemgesturestatus-message"></a>\_Mensagem de Tablet QUERYSYSTEMGESTURESTATUS do WM \_

Enviado quando o sistema solicita uma janela que os gestos do sistema desejam receber.


```C++
#define WM_TABLET_DEFBASE                    0x02C0
#define WM_TABLET_QUERYSYSTEMGESTURESTATUS   (WM_TABLET_DEFBASE + 12)       
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Não usado.

</dd> <dt>

*lParam* 
</dt> <dd>

Um valor de ponto que representa as coordenadas da tela.

</dd> </dl>

## <a name="remarks"></a>Comentários

Ao lidar com essa mensagem, você pode desabilitar dinamicamente os movimentos de regiões de uma janela.

> [!Note]  
> O *lParam* pode ser convertido em coordenadas x e em coordenadas y usando as `GET_X_LPARAM` `GET_Y_LPARAM` macros e.

 

Por padrão, sua janela receberá todos os eventos de gesto do sistema. Você pode escolher quais eventos deseja que sua janela receba e quais eventos você gostaria de desabilitar respondendo à mensagem de **\_ Tablet \_ QUERYSYSTEMGESTURESTATUS do WM** em seu **WndProc**. A mensagem de **\_ Tablet \_ QUERYSYSTEMGESTURESTATUS do WM** é definida em tpcshrd. h. Os valores para habilitar e desabilitar gestos do sistema Tablet System também são definidos em tpcshrd. h da seguinte maneira:

``` syntax
#define TABLET_DISABLE_PRESSANDHOLD        0x00000001
#define TABLET_DISABLE_PENTAPFEEDBACK      0x00000008
#define TABLET_DISABLE_PENBARRELFEEDBACK   0x00000010
#define TABLET_DISABLE_TOUCHUIFORCEON      0x00000100
#define TABLET_DISABLE_TOUCHUIFORCEOFF     0x00000200
#define TABLET_DISABLE_TOUCHSWITCH         0x00008000
#define TABLET_DISABLE_FLICKS              0x00010000
#define TABLET_ENABLE_FLICKSONCONTEXT      0x00020000
#define TABLET_ENABLE_FLICKLEARNINGMODE    0x00040000
#define TABLET_DISABLE_SMOOTHSCROLLING     0x00080000
#define TABLET_DISABLE_FLICKFALLBACKKEYS   0x00100000
#define TABLET_ENABLE_MULTITOUCHDATA       0x01000000
```

> [!Note]
>
> Desabilitar a operação de pressionar e manter irá melhorar a capacidade de resposta para cliques do mouse, pois essa funcionalidade cria um tempo de espera para distinguir entre as duas operações.

 

Tenha cuidado ao manipular a mensagem de **\_ Tablet \_ QUERYSYSTEMGESTURESTATUS do WM** . **WM \_ O TABLET \_ QUERYSYSTEMGESTURESTATUS** é passado usando a função [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) . Se você chamar métodos em uma interface COM, esse objeto deverá estar dentro do mesmo processo. Caso contrário, COM gera uma exceção.

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra como desabilitar movimentos para uma região usando o WM \_ Tablet \_ QUERYSYSTEMGESTURESTATUS.


```C++
#include <windowsx.h>        

(...)        
        
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam){
    case WM_TABLET_QUERYSYSTEMGESTURESTATUS:
        int x = GET_X_LPARAM(lParam);
        int y = GET_Y_LPARAM(lParam);
        if (x < xThreashold && y < yThreshold){
            // no flicks in the region specified by the threashold
            return TABLET_DISABLE_FLICKS;
        }
        // flicks will happen otherwise
        return 0;
}        
        
```



O exemplo a seguir mostra como desabilitar vários recursos de movimentos para uma janela inteira.


```C++
const DWORD dwHwndTabletProperty = 
    TABLET_DISABLE_PRESSANDHOLD | // disables press and hold (right-click) gesture
    TABLET_DISABLE_PENTAPFEEDBACK | // disables UI feedback on pen up (waves)
    TABLET_DISABLE_PENBARRELFEEDBACK | // disables UI feedback on pen button down (circle)
    TABLET_DISABLE_FLICKS; // disables pen flicks (back, forward, drag down, drag up)
        
void SetTabletpenserviceProperties(HWND hWnd){
    ATOM atom = ::GlobalAddAtom(MICROSOFT_TABLETPENSERVICE_PROPERTY);    
    ::SetProp(hWnd, MICROSOFT_TABLETPENSERVICE_PROPERTY, reinterpret_cast<HANDLE>(dwHwndTabletProperty));
    ::GlobalDeleteAtom(atom);
}        
        
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                 |
| parâmetro<br/>                   | <dl> <dt>Tpcshrd. h</dt> </dl> |



 

 
