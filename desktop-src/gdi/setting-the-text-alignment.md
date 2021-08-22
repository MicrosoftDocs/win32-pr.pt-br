---
description: Você pode consultar e definir o alinhamento de texto para um contexto de dispositivo usando as funções GetTextAlign e SetTextAlign.
ms.assetid: 7fdfbadb-827a-4b42-9b9a-b9e46389e13c
title: Definindo o alinhamento de texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78edffa9febaee0fd624cc97c4a908da349ad65526799e1c4bd3450137b62a47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119468416"
---
# <a name="setting-the-text-alignment"></a>Definindo o alinhamento de texto

Você pode consultar e definir o alinhamento de texto para um contexto de dispositivo usando as funções [**GetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-gettextalign) e [**SetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) . As configurações de alinhamento de texto determinam como o texto é posicionado em relação a um local especificado. O texto pode ser alinhado à direita ou à esquerda da posição ou centralizado sobre ele; Ele também pode ser alinhado acima ou abaixo do ponto.

O exemplo a seguir mostra um método para determinar qual sinalizador de alinhamento horizontal está definido:


```C++
switch ((TA_LEFT | TA_RIGHT | TA_CENTER) & GetTextAlign(hdc)) 
{ 
    case TA_LEFT: 
       . 
       . 
       . 
    case TA_RIGHT: 
       . 
       . 
       . 
    case TA_CENTER: 
       . 
       . 
       . 
} 
```



Você também pode usar a função [**SetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) para atualizar a posição atual quando uma função de texto de saída é chamada. Por exemplo, os exemplos a seguir usam a função [**SetTextAlign**](/windows/win32/api/wingdi/nf-wingdi-settextalign) para atualizar a posição atual quando a função [**TextOut**](/windows/desktop/api/Wingdi/nf-wingdi-textouta) é chamada. Neste exemplo, o parâmetro *cArial* é um inteiro que especifica o número de fontes Arial.


```C++
UINT uAlignPrev; 
char szCount[8];
HRESULT hr;
size_t * pcch; 
 
uAlignPrev = SetTextAlign(hdc, TA_UPDATECP); 
MoveToEx(hdc, 10, 50, (LPPOINT) NULL); 
TextOut(hdc, 0, 0, "Number of Arial fonts: ", 23); 
itoa(cArial, szCount, 10); 

hr = StringCchLength(szCount, 9, pcch);
if (FAILED(hr))
{
// TODO: write error handler 
}
 
TextOut(hdc, 0, 0, (LPSTR) szCount, *pcch); 
SetTextAlign(hdc, uAlignPrev); 
```



> [!Note]  
> Você não deve usar [**SetTextAlign**](/windows/win32/api/wingdi/nf-wingdi-settextalign) com ta \_ UPDATECP quando estiver usando [**ScriptStringOut**](/windows/win32/api/usp10/nf-usp10-scriptstringout), pois o texto selecionado não é renderizado corretamente. Se você precisar usar esse sinalizador, poderá remover a definição e redefini-lo conforme necessário para evitar o problema.

 

 

 
