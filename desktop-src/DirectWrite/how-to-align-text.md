---
title: Como alinhar texto
description: Você pode alinhar DirectWrite texto usando o método SetTextAlignment da interface IDWriteTextFormat.
ms.assetid: 7f79dcff-11f6-4e74-b5bd-98bfebe6e393
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3a9d73443577468d794e43dc62d19e7dd24a86227ba6b5e5d8c3542cdded8ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118650357"
---
# <a name="how-to-align-text"></a>Como alinhar texto

Você pode alinhar [DirectWrite](direct-write-portal.md) texto usando o método [**SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) da interface [**IDWriteTextFormat,**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) conforme mostrado no código a seguir que centraliza o texto.


```C++
HRESULT hr = pTextFormat_->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER);

if (FAILED(hr))
{
    // Report the error
}
```



O texto pode ser alinhado à borda à esquerda ou à direita da caixa de layout ou pode ser centralizado. A ilustração a seguir mostra o texto com o alinhamento definido como [**DWRITE \_ TEXT \_ ALIGNMENT \_ LEADING**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment), [**DWRITE \_ TEXT ALIGNMENT \_ \_ CENTER**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment)e [**DWRITE \_ TEXT ALIGNMENT \_ \_ TRAILING**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment), respectivamente.

![ilustração de parágrafos de texto com alinhamento à frente, centralizado e à frente](images/textalignment.png)

> [!Note]  
> O alinhamento depende da direção de leitura; o acima é para a direção de leitura da esquerda para a direita. Para a direção de leitura da direita para a esquerda, seria o oposto.

 

Um [**objeto IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) usará o alinhamento que foi designado para [**o IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) fornecido por você ao criar o layout. Para alterar o alinhamento do texto, use [**IDWriteTextLayout::SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment).

 

 
