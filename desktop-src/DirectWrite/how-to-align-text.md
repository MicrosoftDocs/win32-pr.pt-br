---
title: Como alinhar texto
description: Você pode alinhar o texto DirectWrite usando o método SetTextAlign da interface IDWriteTextFormat.
ms.assetid: 7f79dcff-11f6-4e74-b5bd-98bfebe6e393
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cfd7a025769dea34444236805ebb8e5530ea06c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641446"
---
# <a name="how-to-align-text"></a>Como alinhar texto

Você pode alinhar o texto [DirectWrite](direct-write-portal.md) usando o método [**SetTextAlign**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) da interface [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) , conforme mostrado no código a seguir que centraliza o texto.


```C++
if (SUCCEEDED(hr))
{
    hr = pTextFormat_->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER);
}
```



O texto pode ser alinhado à borda esquerda ou à direita da caixa de layout ou pode ser centralizado. A ilustração a seguir mostra o texto com o alinhamento definido como [**DWRITE de \_ alinhamento de texto à \_ \_ esquerda**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment), [**centro de \_ alinhamento de texto \_ \_ DWRITE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment)e [**alinhamento de \_ texto DWRITE \_ \_ à direita**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment), respectivamente.

![ilustração de parágrafos de texto com alinhamento à esquerda, centralizado e à direita](images/textalignment.png)

> [!Note]  
> O alinhamento é dependente da direção de leitura, o acima é para a direção de leitura da esquerda para a direita. Para a direção de leitura da direita para a esquerda, seria o oposto.

 

Um objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) usará o alinhamento que foi designado para o [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) fornecido por você ao criar o layout. Para alterar o alinhamento do texto, use [**IDWriteTextLayout:: SetTextAlign**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment).

 

 