---
title: Regras para usar ponteiros
description: Portar seu código para compilar para o Microsoft Windows de 32 e 64 bits é simples. Você só precisa seguir algumas regras simples sobre ponteiros de conversão e usar os novos tipos de dados em seu código. As regras para manipulação de ponteiros são as seguintes.
ms.assetid: 4c38bee2-fa1c-493f-a12d-e673df4d4895
keywords:
- regras para usar ponteiros de programação do Windows de 64 bits
- manipulação de ponteiros programação do Windows de 64 bits
- ponteiros de conversão de programação de 64 bits do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 318ff5beed6dc90bd49b6b293131e17db6f92f6b
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "103917748"
---
# <a name="rules-for-using-pointers"></a>Regras para usar ponteiros

Portar seu código para compilar para o Microsoft Windows de 32 e 64 bits é simples. Você só precisa seguir algumas regras simples sobre ponteiros de conversão e usar os novos tipos de dados em seu código. As regras para manipulação de ponteiros são as seguintes.

1.  Não converta ponteiros para **int**, **Long**, **ULONG** ou **DWORD**.

    Se você precisar converter um ponteiro para testar alguns bits, definir ou limpar bits, ou então manipular seu conteúdo, use o tipo de PTR **\_ PTR** ou **int \_** . Esses tipos são tipos integrais que são dimensionados para o tamanho de um ponteiro para o Windows de 32 e 64 bits (por exemplo, **ULONG** para windows de 32 bits e \_ Int64 para o Windows de 64 bits). Por exemplo, suponha que você esteja portando o código a seguir:

    `ImageBase = (PVOID)((ULONG)ImageBase | 1);`

    Como parte do processo de portabilidade, você alteraria o código da seguinte maneira:

    `ImageBase = (PVOID)((ULONG_PTR)ImageBase | 1);`

    Use o modo **uint \_** e o **int \_ PTR** quando apropriado (e se você não tiver certeza se eles são obrigatórios, não há nenhum dano em usá-los apenas no caso). Não Converta seus ponteiros para os tipos **ULONG**, **Long**, **int**, **uint** ou **DWORD**.

    Observe que o **identificador** é definido como **void \***, portanto, typecasting um valor de **identificador** para um valor **ULONG** para testar, definir ou limpar os 2 bits de ordem inferior é um erro no Windows de 64 bits.

2.  Use a função **PtrToLong** ou **PtrToUlong** para truncar ponteiros.

    Se você precisar truncar um ponteiro para um valor de 32 bits, use a função **PtrToLong** ou **PtrToUlong** (definida em Basetsd. h). Essas funções desabilitam o aviso de truncamento do ponteiro para a duração da chamada.

    Use essas funções com cuidado. Depois de converter uma variável de ponteiro usando uma dessas funções, nunca a use como um ponteiro novamente. Essas funções truncam os 32 bits superiores de um endereço, que geralmente são necessários para acessar a memória originalmente referenciada pelo ponteiro. O uso dessas funções sem consideração cuidadosa resultará em um código frágil.

3.  Tenha cuidado ao usar \_ valores de ponteiro 32 no código que pode ser compilado como código de 64 bits. O compilador assinará o ponteiro quando ele for atribuído a um ponteiro nativo no código de 64 bits, sem estender o ponteiro.
4.  Tenha cuidado ao usar \_ valores de ponteiro 64 no código que pode ser compilado como código de 32 bits. O compilador assinará o ponteiro no código de 32 bits, sem estender o ponteiro.
5.  Tenha cuidado ao usar parâmetros de saída.

    Por exemplo, suponha que você tenha uma função definida da seguinte maneira:

    `void func( OUT PULONG *PointerToUlong );`

    Não chame essa função da seguinte maneira.

    ``` syntax
    ULONG ul;
    PULONG lp;
    func((PULONG *)&ul);
    lp = (PULONG)ul;
    ```

    Em vez disso, use a chamada a seguir.

    ``` syntax
    PULONG lp;
    func(&lp);
    ```

    Typecasting &UL para **Pulong \*** impede um erro de compilador, mas a função gravará um valor de ponteiro de 64 bits na memória em &UL. Esse código funciona em janelas de 32 bits, mas causará corrupção de dados em janelas de 64 bits e será uma corrupção sutil, difícil de encontrar. O resultado final: não jogue truques com o código C — simples e simples é melhor.

6.  Tenha cuidado com interfaces polimórficas.

    Não crie funções que aceitem parâmetros **DWORD** para dados polimórficos. Se os dados puderem ser um ponteiro ou um valor integral, use o \_ tipo de **pVoid** /PTR uint.

    Por exemplo, não crie uma função que aceite uma matriz de parâmetros de exceção digitados como valores **DWORD** . A matriz deve ser uma matriz de valores de **\_ PTR DWORD** . Portanto, os elementos da matriz podem conter endereços ou valores integrais de 32 bits. (A regra geral é que se o tipo original é **DWORD** e precisa ser a largura do ponteiro, converta-o em um valor de **\_ PTR DWORD** . É por isso que há tipos de precisão de ponteiro correspondentes.) Se você tiver um código que usa **DWORD**, **ULONG** ou outros tipos de 32 bits de uma maneira polimórfica (ou seja, você realmente deseja que o membro do parâmetro ou da estrutura mantenha um endereço), use **um \_ PTR** no lugar do tipo atual.

7.  Use as novas funções de classe de janela.

    Se você tiver dados de janela ou de classe privada que contenham ponteiros, seu código precisará usar as seguintes novas funções:

    -   [**GetClassLongPtr**](/windows/win32/api/winuser/nf-winuser-getclasslongptra)
    -   [**GetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-getwindowlongptra)
    -   [**SetClassLongPtr**](/windows/win32/api/winuser/nf-winuser-setclasslongptra)
    -   [**SetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra)

    Essas funções podem ser usadas em janelas de 32 e 64 bits, mas são necessárias no Windows de 64 bits. Prepare-se para a transição usando essas funções agora.

    Além disso, você deve acessar ponteiros ou identificadores em dados privados de classe usando as novas funções no Windows de 64 bits. Para ajudá-lo a encontrar esses casos, os seguintes índices não são definidos em winuser. h durante uma compilação de 64 bits:

    -   GWL \_ WndProc
    -   GWL \_ HINSTANCE
    -   GWL \_ HWDPARENT
    -   GWL \_ UserData

    Em vez disso, a WinUser. h define os seguintes novos índices:

    -   GWLP \_ WndProc
    -   GWLP \_ HINSTANCE
    -   GWLP \_ HWNDPARENT
    -   GWLP \_ UserData
    -   ID do GWLP \_

    Por exemplo, o código a seguir não compila:

    `SetWindowLong(hWnd, GWL_WNDPROC, (LONG)MyWndProc);`

    Ele deve ser alterado da seguinte maneira:

    `SetWindowLongPtr(hWnd, GWLP_WNDPROC, (LONG_PTR)MyWndProc);`

    Ao definir o membro **cbWndExtra** da estrutura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) , lembre-se de reservar espaço suficiente para ponteiros. Por exemplo, se você estiver reservando, no momento, os bytes sizeof (DWORD) para um valor de ponteiro, Reserve bytes de sizeof (DWORD \_ PTR).

8.  Acessar todos os dados de janela e de classe usando o **\_ deslocamento de campo**.

    É comum acessar os dados do Windows usando deslocamentos embutidos em código. Essa técnica não é portátil para o Windows de 64 bits. Para tornar seu código portátil, acesse seus dados de janela e de classe usando a macro de **\_ deslocamento de campo** . Não assuma que o segundo ponteiro tenha um deslocamento de 4.

9.  Os tipos **lParam**, **wParam** e **LRESULT** mudam de tamanho com a plataforma.

    Ao compilar o código de 64 bits, esses tipos se expandem para 64 bits, porque eles normalmente mantêm ponteiros ou tipos integrais. Não misture esses valores com valores **DWORD**, **ULONG**, **uint**, **int**, **int** ou **Long** . Examine como você usa esses tipos e certifique-se de não truncar os valores inadvertidamente.

 

 