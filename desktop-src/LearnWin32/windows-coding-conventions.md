---
title: Convenções de codificação do Windows
description: Se você for novo na programação do Windows, ele poderá ser desconcerto quando você vir um programa do Windows pela primeira vez.
ms.assetid: 466a66db-7681-4fce-9672-07849cd1b096
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 365a9c8509d7cb799bafdfa70c326f1074b64d93
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105766259"
---
# <a name="windows-coding-conventions"></a>Convenções de codificação do Windows

Se você for novo na programação do Windows, ele poderá ser desconcerto quando você vir um programa do Windows pela primeira vez. O código é preenchido com definições de tipo estranhas, como **DWORD \_ PTR** e **lpRect**, e variáveis têm nomes como *HWND* e *PWSZ* (chamado de notação húngara). Vale a pena dedicar um momento para aprender algumas das convenções de codificação do Windows.

A grande maioria das APIs do Windows consiste em funções ou em interfaces de Component Object Model (COM). Muito poucas APIs do Windows são fornecidas como classes do C++. (Uma exceção notável é GDI+, uma das APIs de gráficos 2-D.)

## <a name="typedefs"></a>Typedefs

Os cabeçalhos do Windows contêm muitos TYPEDEFs. Muitos deles são definidos no arquivo de cabeçalho WinDef. h. Aqui estão alguns que você encontrará com frequência.

### <a name="integer-types"></a>Tipos de inteiro



| Tipo de dados     | Tamanho    | Inteiro?  |
|---------------|---------|----------|
| **BYTE**      | 8 bits  | Não assinado |
| **DWORD**     | 32 bits | Não assinado |
| **INT32**     | 32 bits | Com sinal   |
| **INT64**     | 64 bits | Com sinal   |
| **LONG**      | 32 bits | Com sinal   |
| **LONGLONG**  | 64 bits | Com sinal   |
| **UINT32**    | 32 bits | Não assinado |
| **UINT64**    | 64 bits | Não assinado |
| **ULONG**     | 32 bits | Não assinado |
| **ULONGLONG** | 64 bits | Não assinado |
| **WORD**      | 16 bits | Não assinado |



 

Como você pode ver, há uma certa quantidade de redundância nesses TYPEDEFs. Parte dessa sobreposição é simplesmente devido ao histórico das APIs do Windows. Os tipos listados aqui têm tamanho fixo e os tamanhos são os mesmos nos aplicativos de 32 bits e 64. Por exemplo, o tipo **DWORD** é sempre de 32 bits de largura.

### <a name="boolean-type"></a>Tipo booliano

**Bool** é um typedef para um valor inteiro que é usado em um contexto booliano. O arquivo de cabeçalho WinDef. h também define dois valores para uso com **bool**.


```C++
#define FALSE    0 
#define TRUE     1
```



Apesar dessa definição de **true**, no entanto, a maioria das funções que retornam um tipo **bool** pode retornar qualquer valor diferente de zero para indicar a verdade booliana. Portanto, você deve sempre escrever isto:


```C++
// Right way.
BOOL result = SomeFunctionThatReturnsBoolean();
if (result) 
{ 
    ...
}
```



e não isso:


```C++
// Wrong!
if (result == TRUE) 
{
    ... 
}
```



Lembre-se de que **bool** é um tipo inteiro e não é intercambiável com o tipo **booliano** de C++.

### <a name="pointer-types"></a>Tipos de ponteiro

O Windows define vários tipos de dados do formato *ponteiro-para-X*. Normalmente, eles têm o prefixo *P-* ou *LP-* no nome. Por exemplo, **lpRect** é um ponteiro para um [**Rect**](/previous-versions//dd162897(v=vs.85)), onde **Rect** é uma estrutura que descreve um retângulo. As seguintes declarações de variável são equivalentes.


```C++
RECT*  rect;  // Pointer to a RECT structure.
LPRECT rect;  // The same
PRECT  rect;  // Also the same.
```



Historicamente, *P* significa "ponteiro" e *LP* significa "ponteiro longo". Ponteiros longos (também chamados de *ponteiros distantes*) são um remanescente do Windows de 16 bits, quando eles eram necessários para endereçar os intervalos de memória fora do segmento atual. O prefixo *LP* foi preservado para tornar mais fácil a porta de código de 16 bits para o Windows de 32 bits. Atualmente, não há distinção — um ponteiro é um ponteiro.

### <a name="pointer-precision-types"></a>Tipos de precisão de ponteiro

Os seguintes tipos de dados são sempre o tamanho de um ponteiro — ou seja, 32 bits de largura em aplicativos de 32 bits e 64 bits de largura em aplicativos de 64 bits. O tamanho é determinado no momento da compilação. Quando um aplicativo de 32 bits é executado em janelas de 64 bits, esses tipos de dados ainda têm 4 bytes de largura. (Um aplicativo de 64 bits não pode ser executado em janelas de 32 bits, portanto, a situação inversa não ocorre.)

-   **PTR de DWORD \_**
-   **INT \_ PTR**
-   **\_PTR longo**
-   **\_ponteiro ULONG**
-   **PTR-UINT \_**

Esses tipos são usados em situações em que um inteiro pode ser convertido em um ponteiro. Eles também são usados para definir variáveis para aritmética de ponteiro e para definir contadores de loop que iteram em todo o intervalo de bytes em buffers de memória. Em geral, eles aparecem em locais onde um valor de 32 bits existente foi expandido para 64 bits no Windows de 64 bits.

## <a name="hungarian-notation"></a>Notação húngaro

A *notação húngara* é a prática de adicionar prefixos aos nomes de variáveis, para fornecer informações adicionais sobre a variável. (O inventário da notação, Charles Simonyi, foi o húngaro, portanto seu nome).

Em sua forma original, a notação húngara fornece informações *semânticas* sobre uma variável, informando o uso pretendido. Por exemplo, *eu* significa um índice, *CB* significa um tamanho em bytes ("contagem de bytes") e números de linha e coluna médias de *RW* e *Col* . Esses prefixos são projetados para evitar o uso acidental de uma variável no contexto errado. Por exemplo, se você viu a expressão `rwPosition +  cbTable` , saberia que um número de linha está sendo adicionado a um tamanho, o que é quase certamente um bug no código

Uma forma mais comum de notação húngara usa prefixos para fornecer informações de *tipo* , por exemplo, *DW* para **DWORD** e *w* para **Word**.

Se você pesquisar na Web "notação húngara", encontrará muitas opiniões sobre se a notação húngara é boa ou ruim. Alguns programadores têm uma aparência intensa para a notação húngara. Outras pessoas acham útil. Independentemente disso, muitos dos exemplos de código no MSDN usam a notação húngara, mas você não precisa memorizar os prefixos para entender o código.

## <a name="next"></a>Avançar

[Trabalhando com cadeias de caracteres](working-with-strings.md)

 

 