---
Description: Enviado a uma janela após a alteração de seu tamanho.
ms.assetid: e3e14dcd-9236-48bd-a692-6985d8146f81
title: Mensagem de WM_SIZE (WinUser. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 04afafd3faafc4ea8c400472254dcf4ec4afa050
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752546"
---
# <a name="wm_size-message"></a>Mensagem de tamanho do WM \_

Enviado a uma janela após a alteração de seu tamanho.

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) .


```C++
#define WM_SIZE                         0x0005
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O tipo de redimensionamento solicitado. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                                                                   | Significado                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="SIZE_MAXHIDE"></span><span id="size_maxhide"></span><dl> <dt>**Tamanho \_ MAXHIDE**</dt> <dt>4</dt> </dl>       | A mensagem é enviada para todas as janelas pop-up quando alguma outra janela é maximizada.<br/>                              |
| <span id="SIZE_MAXIMIZED"></span><span id="size_maximized"></span><dl> <dt>**Tamanho \_ MAXIMIZAdo**</dt> <dt>2</dt> </dl> | A janela foi maximizada.<br/>                                                                          |
| <span id="SIZE_MAXSHOW"></span><span id="size_maxshow"></span><dl> <dt>**Tamanho \_ MAXSHOW**</dt> <dt>3</dt> </dl>       | A mensagem é enviada para todas as janelas pop-up quando alguma outra janela é restaurada para seu tamanho anterior.<br/>      |
| <span id="SIZE_MINIMIZED"></span><span id="size_minimized"></span><dl> <dt>**Tamanho \_ MINIMIZAdo**</dt> <dt>1</dt> </dl> | A janela foi minimizada.<br/>                                                                          |
| <span id="SIZE_RESTORED"></span><span id="size_restored"></span><dl> <dt>**Tamanho \_ RESTAURAdo**</dt> <dt>0</dt> </dl>    | A janela foi redimensionada, mas nem o valor de **tamanho \_ minimizado** nem de **tamanho \_ maximizado** se aplica.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

A palavra de ordem inferior de *lParam* especifica a nova largura da área do cliente.

A palavra de ordem superior do *lParam* especifica a nova altura da área do cliente.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **LRESULT**

Se um aplicativo processar essa mensagem, ele deverá retornar zero.

## <a name="example"></a>Exemplo

```cpp
/******************************************************************
*                                                                 *
*  SimpleText::OnResize                                           *
*                                                                 *
*  If the application receives a WM_SIZE message, this method     *
*  resize the render target appropriately.                        *
*                                                                 *
******************************************************************/

void SimpleText::OnResize(UINT width, UINT height)
{
    if (pRT_)
    {
        D2D1_SIZE_U size;
        size.width = width;
        size.height = height;
        pRT_->Resize(size);
    }
}

LRESULT CALLBACK SimpleText::WndProc(HWND hwnd, UINT message, WPARAM wParam, LPARAM lParam)
{
   
    SimpleText *pSimpleText = reinterpret_cast<SimpleText *>(
                ::GetWindowLongPtr(hwnd, GWLP_USERDATA));

    if (pSimpleText)
    {
        switch(message)
        {
        case WM_SIZE:
            {
                UINT width = LOWORD(lParam);
                UINT height = HIWORD(lParam);
                pSimpleText->OnResize(width, height);
            }
            return 0;

// ...

```

Exemplo de [exemplos clássicos do Windows](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/multimedia/DirectWrite/HelloWorld/SimpleText.cpp) no github.

## <a name="remarks"></a>Comentários

Se a função [**SetScrollPos**](https://msdn.microsoft.com/library/Cc411085(v=MSDN.10).aspx) ou [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) for chamada para uma janela filho como resultado da mensagem de **\_ tamanho do WM** , o parâmetro *bRedraw* ou *bRepaint* deverá ser diferente de zero para fazer com que a janela seja repintada.

Embora a largura e a altura de uma janela sejam valores de 32 bits, o parâmetro *lParam* contém apenas os 16 bits de ordem inferior de cada um.

A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) envia o **\_ tamanho do WM** e as mensagens de **\_ movimentação do WM** quando processa a mensagem do [**WM \_ WINDOWPOSCHANGED**](wm-windowposchanged.md) .
O **\_ tamanho do WM** e as mensagens de **\_ movimentação do WM** não serão enviadas se um aplicativo manipular a mensagem do **WM \_ WINDOWPOSCHANGED** sem chamar **DefWindowProc**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow)
</dt> <dt>

[**WINDOWPOSCHANGED do WM \_**](wm-windowposchanged.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**SetScrollPos**](https://msdn.microsoft.com/library/Cc411085(v=MSDN.10).aspx)
</dt> </dl>

 

 
