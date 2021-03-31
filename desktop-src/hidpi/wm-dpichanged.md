---
title: Mensagem de WM_DPICHANGED (WinUser. h)
description: Enviado quando os pontos em vigor por polegada (DPI) de uma janela forem alterados.
ms.assetid: 97C458F2-89CD-45FF-ABEE-F158A3BCE0B8
keywords:
- DPI alta de mensagem de WM_DPICHANGED
topic_type:
- apiref
api_name:
- WM_DPICHANGED
api_location:
- WinUser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aafbce1e784e1f205f0d32e045785125c1fb5aaa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644733"
---
# <a name="wm_dpichanged-message"></a>Mensagem do WM \_ DPICHANGED

Enviado quando os pontos em vigor por polegada (DPI) de uma janela forem alterados. O DPI é o fator de escala para uma janela. Há vários eventos que podem fazer com que o DPI seja alterado. A lista a seguir indica as possíveis causas para a alteração em DPI.

-   A janela é movida para um novo monitor que tem um DPI diferente.
-   O DPI do monitor que hospeda as alterações da janela.

O DPI atual para uma janela sempre é igual ao último DPI enviado pelo **WM \_ DPICHANGED**. Esse é o fator de escala em que a janela deve ser dimensionada para os threads que reconhecem as alterações de DPI.


```C++
#define WM_DPICHANGED       0x02E0
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) do *wParam* contém o valor do eixo Y do novo DPI da janela. O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) do *wParam* contém o valor do eixo X do novo DPI da janela. Por exemplo, 96, 120, 144 ou 192. Os valores dos eixos X e Y são idênticos aos aplicativos do Windows.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**Rect**](/windows/desktop/api/windef/ns-windef-rect) que fornece um tamanho sugerido e a posição da janela atual dimensionada para o novo dpi. A expectativa é de que os aplicativos reposicionem e redimensionem o Windows com base nas sugestões fornecidas pelo *lParam* ao lidar com essa mensagem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se um aplicativo processar essa mensagem, ele deverá retornar zero.

## <a name="remarks"></a>Comentários

Essa mensagem só é relevante para processos por thread com reconhecimento de **\_ \_ \_ dpi \_ de monitor** ou **reconhecimento de DPI por segmentos com \_ \_ \_ \_ reconhecimento de monitor** . Ele poderá ser recebido em determinadas alterações de DPI se a janela de nível superior ou o processo estiver sendo executado como **dpi** ou **reconhecimento de dpi de sistema**, mas nessas situações poderá ser ignorado com segurança. Para obter mais informações sobre os diferentes tipos de conscientização, consulte reconhecimento de [**dpi de processo \_ \_**](/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-process_dpi_awareness) e [**\_ reconhecimento de DPI**](/windows/desktop/api/windef/ne-windef-dpi_awareness). As versões mais antigas do Windows exigiam reconhecimento de DPI para serem ligadas no nível de um aplicativo. Esses aplicativos usam **\_ \_ reconhecimento de dpi de processo**. Atualmente, o reconhecimento de DPI está vinculado a threads e a janelas individuais, e não a todo o aplicativo. Esses aplicativos usam **\_ reconhecimento de DPI**.

Você só precisa usar o eixo X ou o valor do eixo Y ao dimensionar seu aplicativo, pois eles são os mesmos.

Para tratar essa mensagem corretamente, você precisará redimensionar e reposicionar sua janela com base nas sugestões fornecidas pelo *lParam* e usando [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos). Se você não fizer isso, sua janela aumentará ou diminuirá em relação a todo o resto do novo monitor. Por exemplo, se um usuário estiver usando vários monitores e arrastar a janela de um monitor de 96 DPI para um monitor de 192 DPI, sua janela parecerá ser a metade grande em relação a outros itens no monitor de 192 DPI.

O valor base de DPI é definido como **\_ dpi de \_ tela \_ padrão do usuário** , que é definido como 96. Para determinar o fator de dimensionamento de um monitor, pegue o valor de DPI e divida por **\_ \_ \_ dpi de tela padrão do usuário**. A tabela a seguir fornece alguns valores de DPI de exemplo e fatores de dimensionamento associados.



| Valor de DPI | Porcentagem de dimensionamento |
|-----------|--------------------|
| 96        | 100%               |
| 120       | 125%               |
| 144       | 150%               |
| 192       | 200%               |



 

O exemplo a seguir fornece um exemplo de manipulador de alterações de DPI.


```C++
    case WM_DPICHANGED:
    {
        g_dpi = HIWORD(wParam);
        UpdateDpiDependentFontsAndResources();

        RECT* const prcNewWindow = (RECT*)lParam;
        SetWindowPos(hWnd,
            NULL,
            prcNewWindow ->left,
            prcNewWindow ->top,
            prcNewWindow->right - prcNewWindow->left,
            prcNewWindow->bottom - prcNewWindow->top,
            SWP_NOZORDER | SWP_NOACTIVATE);
        break;
    }
```



O código a seguir dimensiona linearmente um valor de 100% (96 DPI) para um DPI arbitrário definido por *g \_ dpi*.


```C++
    INT iBorderWidth100 = 5;
    iBorderWidth = MulDiv(iBorderWidth100, g_dpi, USER_DEFAULT_SCREEN_DPI);
```



Uma maneira alternativa de dimensionar um valor é converter o valor de DPI em um fator de escala e usá-lo.


```C++
    INT iBorderWidth100 = 5;
    FLOAT fscale = (float) g_dpi / USER_DEFAULT_SCREEN_DPI;
    iBorderWidth = iBorderWidth100 * fscale;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ apenas aplicativos de área de trabalho\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]<br/>                              |
| parâmetro<br/>                   | <dl> <dt>WinUser. h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**reconhecimento de DPI \_**](/windows/desktop/api/windef/ne-windef-dpi_awareness)
</dt> <dt>

[**\_reconhecimento de dpi de processo \_**](/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-process_dpi_awareness)
</dt> </dl>

 

