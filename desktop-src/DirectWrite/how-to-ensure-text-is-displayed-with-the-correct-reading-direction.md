---
title: Verifique se o texto é exibido com a direção de leitura correta
description: Algumas linguagens, como árabe e Hebraico, exigem uma direção de leitura da direita para a esquerda.
ms.assetid: fa9a3dd6-575a-4877-a488-22845c6726c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3774e4d237863a218cadf5206e4dc4921bceaeaa06c00ab81057f80dd8ee6549
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982166"
---
# <a name="ensure-text-is-displayed-with-the-correct-reading-direction"></a>Verifique se o texto é exibido com a direção de leitura correta

Algumas linguagens, como árabe e Hebraico, exigem uma direção de leitura da direita para a esquerda. para um objeto de formato de texto [DirectWrite](direct-write-portal.md) , a direção de leitura padrão é da esquerda para a direita. DirectWrite não infere automaticamente a direção de leitura da localidade, portanto, você deve fazer isso por conta própria.

Primeiro, obtenha os sinalizadores de estilo estendidos para a janela para a qual o texto será renderizado usando a macro GetWindowStyleEx definida em windowsx. h.


```C++
// Get the window extended style flagsfor the current window.
DWORD dwStyle = GetWindowExStyle(hwnd_);
```



A macro retorna um valor DWORD constituído de vários sinalizadores combinados com operações or bits. Você deve determinar se os sinalizadores específicos que afetam a direção de leitura estão lá.

Há dois sinalizadores diferentes relacionados à direção de leitura: WS \_ ex \_ LAYOUTRTL e WS \_ ex \_ RTLREADING.

Use o operador AND de bit e a (&) com a variável dwStyle e a \_ macro WS ex \_ LAYOUTRTL para armazenar um valor bool que indica se o layout é espelhado.


```C++
// Is the WS_EX_LAYOUTRTL flag present?
BOOL bWSLayout = dwStyle & WS_EX_LAYOUTRTL;
```



Faça a mesma coisa para o \_ sinalizador WS ex \_ RTLREADING.


```C++
// Is the WS_EX_RLTREADING flag present?
BOOL bWSReading = dwStyle & WS_EX_RTLREADING;
```



Defina a direção de leitura usando o método [**IDWriteTextFormat:: SetReadingDirection**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setreadingdirection) . O padrão é da esquerda para a direita, portanto, você só precisa definir a direção de leitura se ela for da direita para a esquerda.

> [!Note]  
> \_O WS ex \_ LAYOUTRTL espelha todo o layout e implica a direção de leitura da direita para a esquerda, portanto, defina a direção de leitura somente se um desses sinalizadores estiver presente. Se ambos estiverem presentes, eles cancelarão um ao outro e a direção de leitura do formato de texto deverá ser da esquerda para a direita.

 


```C++
// If either the WS_EX_LAYOUTRTL flag or the WS_EX_RLTREADING flag is present,
// but NOT BOTH, set the reading direction to right to left.
if ((bWSLayout && !bWSReading)
||  (!bWSLayout && bWSReading))
{
    pTextFormat_->SetReadingDirection(DWRITE_READING_DIRECTION_RIGHT_TO_LEFT);
}
```



 

 
