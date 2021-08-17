---
title: Windows Convenções de codificação
description: Se você não estiver Windows programação, isso poderá ser desconcertante quando você vir um programa Windows programa.
ms.assetid: 466a66db-7681-4fce-9672-07849cd1b096
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b78c24f38f9f2f410c044637ca3aa59d4baa39e9b671b3485c5b85899b69c2fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118387391"
---
# <a name="windows-coding-conventions"></a>Windows Convenções de codificação

Se você não estiver Windows programação, isso poderá ser desconcertante quando você vir um programa Windows programa. O código é preenchido com definições de tipo estranho, como **DWORD \_ PTR** e **LPRECT,** e as variáveis têm nomes como *hWnd* e *pwsz* (chamada notação Húmcia). Vale a pena dar um tempo para aprender algumas das Windows de codificação.

A grande maioria das WINDOWS apIs consiste em funções ou interfaces COM (Component Object Model). Pouquíssimos Windows APIs são fornecidas como classes C++. (Uma exceção notável é GDI+, uma das APIs gráficas 2D.)

## <a name="typedefs"></a>Typedefs

Os Windows de texto contêm muitos typedefs. Muitos deles são definidos no arquivo de título WinDef.h. Aqui estão alguns que você encontrará com frequência.

### <a name="integer-types"></a>Tipos de inteiro



| Tipo de dados     | Tamanho    | Assinado?  |
|---------------|---------|----------|
| **BYTE**      | 8 bits  | Não assinado |
| **DWORD**     | 32 bits | Não assinado |
| **Int32**     | 32 bits | Com sinal   |
| **INT64**     | 64 bits | Com sinal   |
| **LONG**      | 32 bits | Com sinal   |
| **Longlong**  | 64 bits | Com sinal   |
| **UINT32**    | 32 bits | Não assinado |
| **UINT64**    | 64 bits | Não assinado |
| **ULONG**     | 32 bits | Não assinado |
| **Ulonglong** | 64 bits | Não assinado |
| **WORD**      | 16 bits | Não assinado |



 

Como você pode ver, há uma determinada quantidade de redundância nesses typedefs. Parte dessa sobreposição ocorre simplesmente devido ao histórico das APIs Windows dados. Os tipos listados aqui têm tamanho fixo e os tamanhos são os mesmos em aplicativos de 32 bits e 64. Por exemplo, o **tipo DWORD** tem sempre 32 bits de largura.

### <a name="boolean-type"></a>Tipo booliana

**BOOL** é um typedef para um valor inteiro usado em um contexto booliana. O arquivo de título WinDef.h também define dois valores para uso com **BOOL.**


```C++
#define FALSE    0 
#define TRUE     1
```



Apesar dessa definição de **TRUE,** no entanto, a maioria das funções que retorna um tipo **BOOL** pode retornar qualquer valor diferente de zero para indicar a verdade booliana. Portanto, você sempre deve escrever isso:


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



Esteja ciente de **que BOOL** é um tipo inteiro e não é intercambiável com o tipo **bool** C++.

### <a name="pointer-types"></a>Tipos de ponteiro

Windows define muitos tipos de dados do formato *ponteiro para X.* Normalmente, eles têm o *prefixo P ou* *LP* no nome. Por exemplo, **LPRECT é um** ponteiro para [**um RECT,**](/previous-versions//dd162897(v=vs.85))em que **RECT** é uma estrutura que descreve um retângulo. As declarações de variável a seguir são equivalentes.


```C++
RECT*  rect;  // Pointer to a RECT structure.
LPRECT rect;  // The same
PRECT  rect;  // Also the same.
```



Historicamente, *P* significa "ponteiro" e *LP* significa "ponteiro longo". Ponteiros longos (também chamados de *ponteiros distantes*) são um holdover de 16 bits Windows, quando eles eram necessários para lidar com intervalos de memória fora do segmento atual. O prefixo *LP* foi preservado para facilitar a portabilidade de código de 16 bits para 32 bits Windows. Atualmente, não há distinção – um ponteiro é um ponteiro.

### <a name="pointer-precision-types"></a>Tipos de precisão de ponteiro

Os tipos de dados a seguir são sempre o tamanho de um ponteiro, ou seja, 32 bits de largura em aplicativos de 32 bits e 64 bits de largura em aplicativos de 64 bits. O tamanho é determinado no tempo de compilação. Quando um aplicativo de 32 bits é executado em um Windows de 64 bits, esses tipos de dados ainda têm 4 bytes de largura. (Um aplicativo de 64 bits não pode ser executado em Windows de 32 bits, portanto, a situação inversa não ocorre.)

-   **DWORD \_ PTR**
-   **INT \_ PTR**
-   **\_PTR LONGO**
-   **ULONG \_ PTR**
-   **UINT \_ PTR**

Esses tipos são usados em situações em que um inteiro pode ser lançado em um ponteiro. Eles também são usados para definir variáveis para aritmética de ponteiro e para definir contadores de loop que iteram em todo o intervalo de bytes em buffers de memória. Em geral, eles aparecem em locais em que um valor de 32 bits existente foi expandido para 64 bits em 64 bits Windows.

## <a name="hungarian-notation"></a>Notação Hêrcia

*Notação hórica* é a prática de adicionar prefixos aos nomes de variáveis, para dar informações adicionais sobre a variável. (O inventor da notação, Charles Fernandesyi, era húngaro, portanto, seu nome).

Em sua forma original, a notação hóstica fornece *informações semânticas* sobre uma variável, informando o uso pretendido. Por exemplo, *i* significa um índice, *cb* significa um tamanho em bytes ("contagem de bytes") e *rw* e *col* média de números de linha e coluna. Esses prefixos são projetados para evitar o uso acidental de uma variável no contexto errado. Por exemplo, se você viu a expressão , você sabe que um número de linha está sendo adicionado a um tamanho, o que é quase certamente um `rwPosition +  cbTable` bug no código

Uma forma mais comum de notação  húngaro usa prefixos para dar informações de tipo, por exemplo, *dw* para **DWORD** e *w* para **WORD**.

Se você pesquisar na Web por "notação hóscia", encontrará muitas opiniões sobre se a notação hóscia é boa ou ruim. Alguns programadores têm uma intensa insalação para notação hóscia. Outras pessoas o acham útil. Independentemente disso, muitos dos exemplos de código no MSDN usam notação húngaro, mas você não precisa memorizar os prefixos para entender o código.

## <a name="next"></a>Avançar

[Trabalhando com cadeias de caracteres](working-with-strings.md)

 

 