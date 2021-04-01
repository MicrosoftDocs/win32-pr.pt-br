---
description: 'Etapa 2: adicionar um comando de menu para pegar um quadro de cartaz'
ms.assetid: 9a0f807b-5543-41d4-ad2a-030a4346131c
title: 'Etapa 2: adicionar um comando de menu para pegar um quadro de cartaz'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58d049dc4e79197cfbe0a86b065eaf67a5ea567a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091741"
---
# <a name="step-2-add-a-menu-command-to-grab-a-poster-frame"></a>Etapa 2: adicionar um comando de menu para pegar um quadro de cartaz

\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]

Este tópico é a etapa 2 da [captura de um quadro de cartaz](grabbing-a-poster-frame.md).

Em seguida, adicione um comando para que o usuário pegue um quadro de pôster de um arquivo. Crie um item de menu com uma ID de recurso do bitmap de IDM \_ e adicione a seguinte instrução case ao procedimento de janela:


```C++
case WM_COMMAND:
    switch (LOWORD(wparam))
    {
    case IDM_BITMAP:
        {
            HRESULT hr = DoShowBitmap(hwnd, &pbmi);
            if (SUCCEEDED(hr))
            {
                pBuffer = reinterpret_cast<BYTE*>(pbmi) + 
                    sizeof(BITMAPINFOHEADER);
                InvalidateRect(hwnd, NULL, TRUE);
            }
            else
            {
                MessageBox(hwnd, TEXT("Cannot display the image."),
                    TEXT("Error"), MB_OK | MB_ICONERROR);
            }
        }
        break;  // IDM_BITMAP
    }
    break;  // WM_COMMAND
```



A função DoShowBitmap retornará o buffer alocado em *pbmi*. Supondo que a função tenha sucesso, o endereço do bitmap (


```C++
pBuffer
```



) pode ser calculado como um deslocamento de *pbmi*. Na função DoShowBitmap, exiba uma caixa de diálogo **Abrir arquivo** para que o usuário escolha um arquivo e, em seguida, chame a função getbitmap definida pelo aplicativo, que irá recuperar o bitmap:


```C++
HRESULT DoShowBitmap(HWND hwnd, BITMAPINFOHEADER** ppbmih)
{
    OPENFILENAME ofn;       // common dialog box structure
    // Initialize OPENFILENAME (not shown).
    // Display the Open File dialog box.  
    if (GetOpenFileName(&ofn) != TRUE) // failed to open file
    {
        return E_FAIL;
    }
    return GetBitmap(ofn.lpstrFile, ppbmih);
}
```



Em seguida: [etapa 3: implementar a função Frame-Grabbing](step-3--implement-the-frame-grabbing-function.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Capturando um quadro de cartaz](grabbing-a-poster-frame.md)
</dt> </dl>

 

 



