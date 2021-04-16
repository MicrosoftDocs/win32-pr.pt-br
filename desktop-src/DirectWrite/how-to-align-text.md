---
title: Como alinhar texto
description: Você pode alinhar o texto DirectWrite usando o método SetTextAlign da interface IDWriteTextFormat.
ms.assetid: 7f79dcff-11f6-4e74-b5bd-98bfebe6e393
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb765860f2fbaac94409aa9ec20c2269beb45cbb
ms.sourcegitcommit: 3b9424e1dcd951b2a73e47de3c7f4d734de4263b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/31/2021
ms.locfileid: "106103867"
---
# <a name="how-to-align-text"></a><span data-ttu-id="46610-103">Como alinhar texto</span><span class="sxs-lookup"><span data-stu-id="46610-103">How to Align Text</span></span>

<span data-ttu-id="46610-104">Você pode alinhar o texto [DirectWrite](direct-write-portal.md) usando o método [**SetTextAlign**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) da interface [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) , conforme mostrado no código a seguir que centraliza o texto.</span><span class="sxs-lookup"><span data-stu-id="46610-104">You can align [DirectWrite](direct-write-portal.md) text by using the [**SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) method of the [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface, as shown in the following code that centers the text.</span></span>


```C++
HRESULT hr = pTextFormat_->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER);

if (FAILED(hr))
{
    // Report the error
}
```



<span data-ttu-id="46610-105">O texto pode ser alinhado à borda esquerda ou à direita da caixa de layout ou pode ser centralizado.</span><span class="sxs-lookup"><span data-stu-id="46610-105">The text can be aligned to the leading or trailing edge of the layout box, or it can be centered.</span></span> <span data-ttu-id="46610-106">A ilustração a seguir mostra o texto com o alinhamento definido como [**DWRITE de \_ alinhamento de texto à \_ \_ esquerda**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment), [**centro de \_ alinhamento de texto \_ \_ DWRITE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment)e [**alinhamento de \_ texto DWRITE \_ \_ à direita**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment), respectivamente.</span><span class="sxs-lookup"><span data-stu-id="46610-106">The following illustration shows text with the alignment set to [**DWRITE\_TEXT\_ALIGNMENT\_LEADING**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment), [**DWRITE\_TEXT\_ALIGNMENT\_CENTER**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment), and [**DWRITE\_TEXT\_ALIGNMENT\_TRAILING**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment), respectively.</span></span>

![ilustração de parágrafos de texto com alinhamento à esquerda, centralizado e à direita](images/textalignment.png)

> [!Note]  
> <span data-ttu-id="46610-108">O alinhamento é dependente da direção de leitura, o acima é para a direção de leitura da esquerda para a direita.</span><span class="sxs-lookup"><span data-stu-id="46610-108">The alignment is dependent on reading direction, the above is for left-to-right reading direction.</span></span> <span data-ttu-id="46610-109">Para a direção de leitura da direita para a esquerda, seria o oposto.</span><span class="sxs-lookup"><span data-stu-id="46610-109">For right-to-left reading direction it would be the opposite.</span></span>

 

<span data-ttu-id="46610-110">Um objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) usará o alinhamento que foi designado para o [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) fornecido por você ao criar o layout.</span><span class="sxs-lookup"><span data-stu-id="46610-110">An [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object will use the alignment that has been designated for the [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) provided by you when creating the layout.</span></span> <span data-ttu-id="46610-111">Para alterar o alinhamento do texto, use [**IDWriteTextLayout:: SetTextAlign**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment).</span><span class="sxs-lookup"><span data-stu-id="46610-111">To change the text alignment, use [**IDWriteTextLayout::SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment).</span></span>

 

 
