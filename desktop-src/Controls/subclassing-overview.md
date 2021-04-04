---
title: Controles de subclasses
description: Se um controle faz quase tudo que você deseja, mas você precisa de mais alguns recursos, você pode alterar ou adicionar recursos ao controle original por meio de uma subclasse.
ms.assetid: 7f558674-c8b2-4461-96ba-e139416b7a1c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c013ee317ddeee6ff80dc4a26982d40d7117950
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104008464"
---
# <a name="subclassing-controls"></a>Controles de subclasses

Se um controle faz quase tudo que você deseja, mas você precisa de mais alguns recursos, você pode alterar ou adicionar recursos ao controle original por meio de uma subclasse. Uma subclasse pode ter todos os recursos de uma classe existente, bem como quaisquer recursos adicionais que você queira dar a ela.

Este documento discute como as subclasses são criadas e inclui os tópicos a seguir.

-   [Controles de subclasse antes do ComCtl32.dll versão 6](#subclassing-controls-prior-to-comctl32dll-version-6)
    -   [Armazenando dados do usuário](#storing-user-data)
    -   [Desvantagens da antiga abordagem de subclasse](#disadvantages-of-the-old-subclassing-approach)
-   [Controles de subclasses usando ComCtl32.dll versão 6](#subclassing-controls-using-comctl32dll-version-6)
    -   [SetWindowSubclass](#setwindowsubclass)
    -   [GetWindowSubclass](#getwindowsubclass)
    -   [RemoveWindowSubclass](#removewindowsubclass)
    -   [DefSubclassProc](#defsubclassproc)

## <a name="subclassing-controls-prior-to-comctl32dll-version-6"></a>Controles de subclasse antes do ComCtl32.dll versão 6

Você pode colocar um controle em uma subclasse e armazenar dados de usuário em um controle. Você faz isso ao usar versões do ComCtl32.dll anteriores à versão 6. Há algumas desvantagens na criação de subclasses com versões anteriores do ComCtl32.dll.

Para criar um novo controle, é melhor começar com um dos controles comuns do Windows e estendê-lo para se adequar a uma necessidade específica. Para estender um controle, crie um controle e substitua seu procedimento de janela existente por um novo. O novo procedimento intercepta as mensagens do controle e as atua ou transmite-as para o procedimento original para o processamento padrão. Use a função [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) ou [**SetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-setwindowlongptra) para substituir o WndProc do controle. O exemplo de código a seguir mostra como substituir um WNDPROC.


```
OldWndProc = (WNDPROC)SetWindowLongPtr (hButton,
GWLP_WNDPROC, (LONG_PTR)NewWndProc);
```



### <a name="storing-user-data"></a>Armazenando dados do usuário

Talvez você queira armazenar os dados do usuário com uma janela individual. Esses dados podem ser usados pelo novo procedimento de janela para determinar como desenhar o controle ou para onde enviar determinadas mensagens. Por exemplo, você pode usar dados para armazenar um ponteiro de classe C++ para a classe que representa o controle. O exemplo de código a seguir mostra como usar [**SetProp**](/windows/desktop/api/winuser/nf-winuser-setpropa) para armazenar dados com uma janela.


```
SetProp (hwnd, TEXT("MyData"), (HANDLE)pMyData);
```



### <a name="disadvantages-of-the-old-subclassing-approach"></a>Desvantagens da antiga abordagem de subclasse

A lista a seguir destaca algumas das desvantagens de usar a abordagem descrita anteriormente para subclasse de um controle.

-   O procedimento de janela só pode ser substituído uma vez.
-   É difícil remover uma subclasse após sua criação.
-   A associação de dados privados a uma janela é ineficiente.
-   Para chamar o próximo procedimento em uma cadeia de subclasse, você não pode converter o antigo procedimento de janela e chamá-lo, você deve chamá-lo usando a função [**CallWindowProc**](/windows/desktop/api/winuser/nf-winuser-callwindowproca) .

## <a name="subclassing-controls-using-comctl32dll-version-6"></a>Controles de subclasses usando ComCtl32.dll versão 6

> [!Note]  
> ComCtl32.dll versão 6 é apenas Unicode. Os controles comuns com suporte pelo ComCtl32.dll versão 6 não devem ser subclasses (ou superclasses) com procedimentos de janela ANSI.

 

O ComCtl32.dll versão 6 contém quatro funções que facilitam a criação de subclasses e eliminam as desvantagens discutidas anteriormente. As novas funções encapsulam o gerenciamento envolvido com vários conjuntos de dados de referência, portanto, o desenvolvedor pode se concentrar em recursos de programação e não no gerenciamento de subclasses. As funções de subclasse são:

-   [**SetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass)
-   [**GetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-getwindowsubclass)
-   [**RemoveWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-removewindowsubclass)
-   [**DefSubclassProc**](/windows/desktop/api/commctrl/nf-commctrl-defsubclassproc)

### <a name="setwindowsubclass"></a>SetWindowSubclass

Essa função é usada para inicialmente subclasse de uma janela. Cada subclasse é identificada exclusivamente pelo endereço do *pfnSubclass* e seu *uIdSubclass*. Ambos são parâmetros da função [**SetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass) . Várias subclasses podem compartilhar o mesmo procedimento de subclasse e a ID pode identificar cada chamada. Para alterar os dados de referência, você pode fazer chamadas subsequentes para **SetWindowSubclass**. A vantagem importante é que cada instância de subclasse tem seus próprios dados de referência.

A declaração de um procedimento de subclasse é ligeiramente diferente de um procedimento de janela regular porque ele tem duas partes adicionais de dados: a ID da subclasse e os dados de referência. Os dois últimos parâmetros da declaração de função a seguir mostram isso.


```
LRESULT CALLBACK MyWndProc (HWND hWnd, UINT msg,
WPARAM wParam, LPARAM lParam, UINT_PTR uIdSubclass,
DWORD_PTR dwRefData);
```



Toda vez que uma mensagem é recebida pelo novo procedimento de janela, uma ID de subclasse e dados de referência são incluídos.

> [!Note]  
> Todas as cadeias de caracteres passadas para o procedimento são cadeias de caracteres Unicode, mesmo se o Unicode não for especificado como uma definição de pré-processador.

 

O exemplo a seguir mostra uma implementação de esqueleto de um procedimento de janela para um controle de subclasse.


```
LRESULT CALLBACK OwnerDrawButtonProc(HWND hWnd, UINT uMsg, WPARAM wParam,
                               LPARAM lParam, UINT_PTR uIdSubclass, DWORD_PTR dwRefData)
{
    switch (uMsg)
    {
    case WM_PAINT:
        .
        .
        .
        return TRUE;
    // Other cases...
    } 
    return DefSubclassProc(hWnd, uMsg, wParam, lParam);
}
```



O procedimento de janela pode ser anexado ao controle no manipulador [**\_ INITDIALOG do WM**](/windows/desktop/dlgbox/wm-initdialog) do procedimento da caixa de diálogo, conforme mostrado no exemplo a seguir.


```
case WM_INITDIALOG:
{
    HWND button = GetDlgItem(hDlg, IDC_OWNERDRAWBUTTON);
    SetWindowSubclass(button, OwnerDrawButtonProc, 0, 0);
    return TRUE;
}
```



### <a name="getwindowsubclass"></a>GetWindowSubclass

Essa função recupera informações sobre uma subclasse. Por exemplo, você pode usar [**GetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-getwindowsubclass) para acessar os dados de referência.

### <a name="removewindowsubclass"></a>RemoveWindowSubclass

Essa função remove as subclasses. [**RemoveWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-removewindowsubclass) em combinação com o [**SetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass) permite adicionar e remover subclasses dinamicamente.

### <a name="defsubclassproc"></a>DefSubclassProc

A função [**DefSubclassProc**](/windows/desktop/api/commctrl/nf-commctrl-defsubclassproc) chama o próximo manipulador na cadeia de subclasse. A função também recupera a ID e os dados de referência apropriados e passa as informações para o próximo procedimento da janela.

 

 