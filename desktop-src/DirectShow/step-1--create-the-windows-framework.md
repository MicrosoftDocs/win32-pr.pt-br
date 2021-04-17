---
description: 'Etapa 1: criar o Windows Framework'
ms.assetid: 678c6261-cbd0-4865-a1dd-03de55eca996
title: 'Etapa 1: criar o Windows Framework'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ff1712f631db520ff30065e8943d13b280f3d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768625"
---
# <a name="step-1-create-the-windows-framework"></a>Etapa 1: criar o Windows Framework

\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]

Comece criando a estrutura básica de um aplicativo do Windows, incluindo WinMain e um procedimento de janela. A função WinMain não é mostrada aqui; Chame o [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) antes do loop de mensagem para inicializar a biblioteca com e [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) depois que o loop de mensagem for encerrado. Comece com o seguinte procedimento mínimo de janela:


```C++
LRESULT CALLBACK MainWndProc(HWND hwnd, UINT msg, WPARAM wparam, LPARAM lparam)
{
    static BITMAPINFOHEADER *pbmi = NULL;
    static BYTE *pBuffer = NULL;
    switch (msg)
    {
    case WM_CLOSE:
        DestroyWindow(hwnd);
        break;
    case WM_DESTROY:
        if (pbmi) delete [] pbmi;
        PostQuitMessage(0);
        break;
    default:
        return DefWindowProc(hwnd, msg, wparam, lparam);
    }
    return 0;
}
```



Quando você recupera um quadro de pôster do detector de mídia, ele retorna um buffer que contém uma estrutura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) seguida pelos bits de imagem. Portanto, defina duas variáveis estáticas no procedimento de janela: *pbmi* manterá um ponteiro para a estrutura **BITMAPINFOHEADER** e *pBuffer* manterá um ponteiro para o bitmap. O aplicativo irá alocar o buffer no *pbmi* usando `new` , portanto, ele deve excluir o buffer antes que a janela seja destruída. O ponteiro *pBuffer* é calculado como um deslocamento de *pbmi*, portanto, não é necessário excluí-lo.

Próximo: [etapa 2: adicionar um comando de menu para pegar um quadro de cartaz](step-2--add-a-menu-command-to-grab-a-poster-frame.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Capturando um quadro de cartaz](grabbing-a-poster-frame.md)
</dt> </dl>

 

 
