---
title: Conformidade ESTRITA
description: Algum código-fonte compilado com êxito pode produzir mensagens de erro quando você habilita a verificação de tipo STRICT.
ms.assetid: 88368fec-b375-4ad0-aa13-ffadf0338a44
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29baee071bd8d7c236ec5f2f99d1dff11aeac37deb44b0d8a6254325c9a75df0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117928141"
---
# <a name="strict-compliance"></a>Conformidade ESTRITA

Algum código-fonte compilado com êxito pode produzir mensagens de erro quando você habilita a **verificação de tipo STRICT.** As seções a seguir descrevem os requisitos mínimos para fazer com que seu código seja compilado **quando STRICT** estiver habilitado. Etapas adicionais são recomendadas, especialmente para produzir código portátil.

## <a name="general-requirements"></a>Requisitos gerais

O principal requisito é que você deve declarar tipos de alça corretos e ponteiros de função em vez de depender de tipos mais gerais. Não é possível usar um tipo de identificador em que outro é esperado. Isso também significa que você pode ter que alterar declarações de função e usar mais casts de tipo.

Para melhores resultados, o tipo **HANDLE genérico** deve ser usado somente quando necessário.

## <a name="declaring-functions-within-your-application"></a>Declarando funções em seu aplicativo

Certifique-se de que todas as funções de aplicativo sejam declaradas. É recomendável colocar todas as declarações de função em um arquivo de inclusão porque você pode facilmente verificar suas declarações e procurar os tipos de parâmetro e retorno que devem ser alterados.

Se você usar a opção do compilador **/Zg** para criar arquivos de header para suas funções, lembre-se de que você obterá resultados diferentes dependendo se habilitar a verificação de tipo **STRICT.** Com **STRICT** desabilitado, todos os tipos de identificador geram o mesmo tipo base. Com **STRICT** habilitado, eles geram tipos base diferentes. Para evitar conflitos, você precisa criar o arquivo de header sempre que habilitar ou desabilitar **STRICT** ou editar o arquivo de header para usar os tipos **HWND,** **HDC,** **HANDLE** e assim por diante, em vez dos tipos base.

As declarações de função que você copiou de Windows.h em seu código-fonte podem ter sido alteradas e sua declaração local pode estar des date. Remova sua declaração local.

## <a name="types-that-require-casts"></a>Tipos que exigem casts

Algumas funções têm tipos de retorno genéricos ou parâmetros. Por exemplo, a [**função SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) retorna dados que podem ser qualquer número de tipos, dependendo do contexto. Quando você vir qualquer uma dessas funções em seu código-fonte, certifique-se de usar a cast de tipo correta e se ela é o mais específica possível. A lista a seguir é um exemplo dessas funções.

-   [**LocalLock**](/windows/desktop/api/winbase/nf-winbase-locallock)
-   [**GlobalLock**](/windows/desktop/api/winbase/nf-winbase-globallock)
-   [**Getwindowlong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga)
-   [**Setwindowlong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga)
-   [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage)
-   [**Defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
-   [**Senddlgitemmessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea)

Ao chamar [**SendMessage,**](/windows/win32/api/winuser/nf-winuser-sendmessage) [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)ou [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea), você deve primeiro lançar o resultado para o tipo **UINT \_ PTR**. Você precisa seguir etapas semelhantes para qualquer função que retorne um **valor LRESULT** ou **LONG \_ PTR,** em que o resultado contém um handle. Isso é necessário para escrever código portátil porque o tamanho de um alça varia, dependendo da versão do Windows. A conversão (**UINT \_ PTR**) garante a conversão adequada. O código a seguir mostra um exemplo no **qual SendMessage** retorna um alça para um pincel:


```C++
HBRUSH hbr;

hbr = (HBRUSH)(UINT_PTR)SendMessage(hwnd, WM_CTLCOLOR, ..., ...);
```



Às vezes, o parâmetro **CreateWindow** e **CreateWindowEx** *é* usado para passar um ID (identificador de controle inteiro). Nesse caso, você deve passar a ID para um **tipo HMENU:**


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

Para obter o maior benefício da **verificação de tipo STRICT,** há diretrizes adicionais que você deve seguir. Seu código será mais portátil em versões futuras Windows se você fizer as alterações a seguir.

Os tipos **WPARAM,** **LPARAM,** **LRESULT** e **LPVOID** são *tipos de dados polimórficos*. Eles têm diferentes tipos de dados em momentos diferentes, mesmo quando **a verificação de** tipo STRICT está habilitada. Para obter o benefício da verificação de tipo, você deve castar valores desses tipos assim que possível. (Observe que a mensagem é automaticamente recast *wParam* e *lParam* para você de maneira portátil.)

Tome cuidado especial para distinguir **os tipos HMODULE** e **HINSTANCE.** Mesmo com **STRICT** habilitado, eles são definidos como o mesmo tipo base. A maioria das funções de gerenciamento de módulo de kernel usa tipos **HINSTANCE,** mas há algumas funções que retornam ou aceitam apenas tipos **HMODULE.**

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Desabilitando STRICT](disabling-strict.md)
</dt> <dt>

[Habilitando STRICT](enabling-strict.md)
</dt> </dl>

 

 