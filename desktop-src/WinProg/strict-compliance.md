---
title: Conformidade estrita
description: Um código-fonte que compila com êxito pode produzir mensagens de erro quando você habilita a verificação de tipo estrito.
ms.assetid: 88368fec-b375-4ad0-aa13-ffadf0338a44
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02d04c3a849dc62647758e3515728e3dd3f65dcb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366277"
---
# <a name="strict-compliance"></a>Conformidade estrita

Um código-fonte que compila com êxito pode produzir mensagens de erro quando você habilita a verificação de tipo **estrito** . As seções a seguir descrevem os requisitos mínimos para fazer com que seu código seja compilado quando **Strict** estiver habilitado. Etapas adicionais são recomendadas, especialmente para produzir código portátil.

## <a name="general-requirements"></a>Requisitos gerais

O requisito principal é que você deve declarar tipos de identificador e ponteiros de função corretos em vez de depender de tipos mais gerais. Você não pode usar um tipo de identificador em que outro é esperado. Isso também significa que você pode precisar alterar as declarações de função e usar mais conversões de tipo.

Para obter melhores resultados, o tipo de **identificador** genérico deve ser usado somente quando necessário.

## <a name="declaring-functions-within-your-application"></a>Declarando funções dentro de seu aplicativo

Verifique se todas as funções de aplicativo estão declaradas. É recomendável colocar todas as declarações de função em um arquivo de inclusão, pois você pode facilmente examinar suas declarações e procurar os tipos de parâmetro e de retorno que devem ser alterados.

Se você usar a opção de compilador **/ZG** para criar arquivos de cabeçalho para suas funções, lembre-se de que obterá resultados diferentes dependendo se você tiver habilitado a verificação de tipo **estrito** . Com **Strict** Disabled, todos os tipos de identificador geram o mesmo tipo base. Com o **Strict** Enabled, eles geram tipos de base diferentes. Para evitar conflitos, você precisa recriar o arquivo de cabeçalho sempre que habilitar ou desabilitar **estrito**, ou editar o arquivo de cabeçalho para usar os tipos **HWND**, **HDC**, **Handle** e assim por diante, em vez dos tipos base.

Qualquer declaração de função que você copiou do Windows. h para o código-fonte pode ter sido alterada e sua declaração local pode estar desatualizada. Remova sua declaração local.

## <a name="types-that-require-casts"></a>Tipos que exigem conversões

Algumas funções têm tipos de retorno genéricos ou parâmetros. Por exemplo, a função [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) retorna dados que podem ser qualquer número de tipos, dependendo do contexto. Quando você vir qualquer uma dessas funções em seu código-fonte, verifique se você usa a conversão de tipo correta e se ela é a mais específica possível. A lista a seguir é um exemplo dessas funções.

-   [**LocalLock**](/windows/desktop/api/winbase/nf-winbase-locallock)
-   [**GlobalLock**](/windows/desktop/api/winbase/nf-winbase-globallock)
-   [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga)
-   [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga)
-   [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage)
-   [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
-   [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea)

Ao chamar [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage), [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)ou [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea), você deve primeiro converter o resultado para o tipo **uint \_ PTR**. Você precisa tomar etapas semelhantes para qualquer função que retorne um valor **\_ PTR** **LRESULT** ou Long, em que o resultado contenha um identificador. Isso é necessário para escrever código portátil porque o tamanho de um identificador varia, dependendo da versão do Windows. A conversão (**uint \_ PTR**) garante a conversões corretas. O código a seguir mostra um exemplo em que **SendMessage** retorna um identificador para um pincel:


```C++
HBRUSH hbr;

hbr = (HBRUSH)(UINT_PTR)SendMessage(hwnd, WM_CTLCOLOR, ..., ...);
```



O parâmetro **CreateWindow** e **CreateWindowEx** *HMENU* às vezes é usado para passar um identificador de controle de inteiro (ID). Nesse caso, você deve converter a ID para um tipo **HMENU** :


```C++
HWND hwnd;
int id;

hwnd = CreateWindow(
        TEXT("Button"), TEXT("OK"), BS_PUSHBUTTON,
        x, y, cx, cy, hwndParent,
        (HMENU)id,    // Cast required here
        hinst,
        NULL);
```



## <a name="additional-considerations"></a>Considerações adicionais

Para aproveitar ao máximo o benefício da verificação de tipo **estrito** , há diretrizes adicionais que você deve seguir. Seu código será mais portátil em versões futuras do Windows se você fizer as seguintes alterações.

Os tipos **wParam**, **lParam**, **LRESULT** e **LPVOID** são *tipos de dados polimórficos*. Eles mantêm diferentes tipos de dados em momentos diferentes, mesmo quando a verificação de tipo **estrito** está habilitada. Para obter o benefício da verificação de tipo, você deve converter valores desses tipos assim que possível. (Observe que os decifradores de mensagens reconvertem automaticamente *wParam* e *lParam* para você de maneira portátil.)

Tome cuidado especial para distinguir os tipos **HMODULE** e **HINSTANCE** . Mesmo com **Strict** Enabled, eles são definidos como o mesmo tipo base. A maioria das funções de gerenciamento de módulo de kernel usa tipos **HINSTANCE** , mas há algumas funções que retornam ou aceitam apenas tipos **HMODULE** .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Desabilitando estrito](disabling-strict.md)
</dt> <dt>

[Habilitando STRICT](enabling-strict.md)
</dt> </dl>

 

 