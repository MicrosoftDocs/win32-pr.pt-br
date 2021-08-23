---
description: 'etapa 1: criar a estrutura de Windows'
ms.assetid: 678c6261-cbd0-4865-a1dd-03de55eca996
title: 'etapa 1: criar a estrutura de Windows'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: feba710c8df948e34c0da0ca9e7a1de85622bfae462290cbce3f36777854cb6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072510"
---
# <a name="step-1-create-the-windows-framework"></a>etapa 1: criar a estrutura de Windows

\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]

comece criando a estrutura básica de um aplicativo Windows, incluindo o WinMain e um procedimento de janela. A função WinMain não é mostrada aqui; Chame o [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) antes do loop de mensagem para inicializar a biblioteca com e [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) depois que o loop de mensagem for encerrado. Comece com o seguinte procedimento mínimo de janela:


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

 

 
