---
Description: Enviado para uma janela depois que seu tamanho foi alterado.
ms.assetid: e3e14dcd-9236-48bd-a692-6985d8146f81
title: WM_SIZE mensagem (Winuser.h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 473e4e63523c7b97968e54349e5882b7e589fc7238d717ccf96563b5ce93388e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119548216"
---
# <a name="wm_size-message"></a>Mensagem WM \_ SIZE

Enviado para uma janela depois que seu tamanho foi alterado.

Uma janela recebe essa mensagem por meio de [**sua função WindowProc.**](/windows/win32/api/winuser/nf-winuser-defwindowproca)


```C++
#define WM_SIZE                         0x0005
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O tipo de reizing solicitado. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                                                                   | Significado                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="SIZE_MAXHIDE"></span><span id="size_maxhide"></span><dl> <dt>**TAMANHO \_ MAXHIDE**</dt> <dt>4</dt> </dl>       | A mensagem é enviada para todas as janelas pop-up quando alguma outra janela é maximizada.<br/>                              |
| <span id="SIZE_MAXIMIZED"></span><span id="size_maximized"></span><dl> <dt>**TAMANHO \_ MAXIMIZADA**</dt> <dt>2</dt> </dl> | A janela foi maximizada.<br/>                                                                          |
| <span id="SIZE_MAXSHOW"></span><span id="size_maxshow"></span><dl> <dt>**TAMANHO \_ MAXSHOW**</dt> <dt>3</dt> </dl>       | A mensagem é enviada para todas as janelas pop-up quando alguma outra janela foi restaurada para seu tamanho anterior.<br/>      |
| <span id="SIZE_MINIMIZED"></span><span id="size_minimized"></span><dl> <dt>**TAMANHO \_ MINIMIZADO**</dt> <dt>1</dt> </dl> | A janela foi minimizada.<br/>                                                                          |
| <span id="SIZE_RESTORED"></span><span id="size_restored"></span><dl> <dt>**TAMANHO \_ RESTAURADO**</dt> <dt>0</dt> </dl>    | A janela foi ressada, mas nem **o valor SIZE \_ MINIMIZED** nem **SIZE \_ MAXIMIZED** se aplica.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

A palavra de ordem baixa *de lParam* especifica a nova largura da área do cliente.

A palavra de ordem alta *de lParam* especifica a nova altura da área do cliente.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **LRESULT**

Se um aplicativo processa essa mensagem, ele deve retornar zero.

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

Exemplo de [Windows exemplos clássicos](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/multimedia/DirectWrite/HelloWorld/SimpleText.cpp) em GitHub.

## <a name="remarks"></a>Comentários

Se a função [**SetScrollPos**](https://msdn.microsoft.com/library/Cc411085(v=MSDN.10).aspx) ou [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) for chamada para uma janela filho como resultado da mensagem **WM \_ SIZE,** o parâmetro *bRedraw* ou *bRepaint* deverá ser não zero para fazer com que a janela seja pintada.

Embora a largura e a altura de uma janela sejam valores de 32 bits, o parâmetro *lParam* contém apenas os 16 bits de ordem baixa de cada um.

A [**função DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) envia as **mensagens WM \_ SIZE** e **WM \_ MOVE** quando processa a mensagem [**WM \_ WINDOWPOSCHANGED.**](wm-windowposchanged.md)
As **mensagens WM \_ SIZE** e **WM \_ MOVE** não serão enviadas se um aplicativo manipular a mensagem **WM \_ WINDOWPOSCHANGED** sem chamar **DefWindowProc**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**Hiword**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**Loword**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**Movewindow**](/windows/win32/api/winuser/nf-winuser-movewindow)
</dt> <dt>

[**WM \_ WINDOWPOSCHANGED**](wm-windowposchanged.md)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**Setscrollpos**](https://msdn.microsoft.com/library/Cc411085(v=MSDN.10).aspx)
</dt> </dl>

 

 
