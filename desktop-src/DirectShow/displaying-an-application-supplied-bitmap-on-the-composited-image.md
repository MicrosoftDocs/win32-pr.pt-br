---
title: Exibir um bitmap fornecido pelo aplicativo na imagem compostada
description: Exibindo um bitmap Application-Supplied na imagem compostada
ms.assetid: c51329d3-e814-4ef9-aad8-a3e60f9fa2a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90768cc9ba9ed3a7f53336c63b0112f297e1844ba9638799e8badf28588775eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118653508"
---
# <a name="display-an-app-supplied-bitmap-on-the-composited-image"></a>Exibir um bitmap fornecido pelo aplicativo na imagem compostada

Os aplicativos podem usar o modo de mistura do VMR para exibir logotipos de canal com combinação alfabética, uma interface do usuário ou anúncios de forma parcial ou completa dentro do retângulo do vídeo. Como a mesclagem é realizada no hardware pelo processador de gráficos, há um impacto mínimo sobre o desempenho de reprodução do fluxo de vídeo e não há nenhuma cintilação detectável ou artefatos de divisão. Os aplicativos podem alterar a imagem exibida com a frequência desejada. deve-se observar que as alterações só são refletidas na tela quando o grafo de filtro de DirectShow está no estado executando.

O VMR usa seu componente de mixer para sobrepor o bitmap na imagem compostada. Com o VMR-7, o aplicativo deve forçar o VMR a carregar seu mixer, mesmo que haja apenas um único fluxo de vídeo. Isso não é necessário com o VMR-9, já que ele carrega seu mixer por padrão.

Para misturar uma imagem de bitmap estática com o fluxo de vídeo, o aplicativo cria o VMR e o adiciona ao grafo e, em seguida, chama [**IVMRFilterConfig:: SetNumberOfStreams**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams). O valor passado para essa função identifica o número de Pins de entrada que o VMR deve criar. Os aplicativos podem especificar qualquer valor entre 1 e \_ o máximo de fluxos de mixer \_ ; especificar um valor de 1 será válido se o aplicativo pretender exibir apenas um fluxo de vídeo. Embora o VMR-7 tenha um único PIN de entrada por padrão, esse método deve ser chamado para forçá-lo a carregar seu componente de mixer. (O VMR-9 carrega seu mixer e configura quatro Pins por padrão.)

Para definir o bitmap, use a interface [**IVMRMixerBitmap**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap) no VMR-7 ou na interface [**IVMRMixerBitmap9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9) no VMR-9.

O bitmap pode ser especificado por um identificador para um contexto de dispositivo GDI (hDC) ou por uma interface de superfície do DirectDraw. Se o aplicativo quiser que a imagem contenha informações alfa incorporadas (também conhecidas por pixel alfa), ele deverá posicionar os dados da imagem em uma interface de superfície do DirectDraw. Isso ocorre porque atualmente não é possível inserir informações alfa por pixel com um contexto de dispositivo GDI. A superfície do DirectDraw deve ser RGB32 ou ARGB32, e, preferencialmente, ser uma superfície de memória do sistema. Não é necessário que as dimensões da superfície sejam uma potência de 2.

O VMR permite que os aplicativos especifiquem o local e um valor de transparência geral para a imagem. O código a seguir mostra como transmitir dados de imagem para o VMR para mesclagem subsequente:


```C++
HRESULT BlendApplicationImage( 
  HWND hwndApp,
  IVMRWindowlessControl* pWc,
  HBITMAP hbm
)
{
    LONG cx, cy;
    HRESULT hr;
    hr = pWc->GetNativeVideoSize(&cx, &cy, NULL, NULL);
    if (FAILED(hr))
        return hr;
    
    HDC hdc = GetDC(hwndApp);
    if (hdc == NULL)
    {
        return E_FAIL;
    }
    
    HDC hdcBmp = CreateCompatibleDC(hdc);
    ReleaseDC(hwndApp, hdc);
    
    if (hdcBmp == NULL)
    {
        return E_FAIL;
    }
    
    BITMAP bm;
    if (0 == GetObject(hbm, sizeof(bm), &bm))
    {
        DeleteDC(hdcBmp);
        return E_FAIL;
    }
    
    HBITMAP hbmOld = (HBITMAP)SelectObject(hdcBmp, hbm);
    if (hbmOld == 0)
    {
        DeleteDC(hdcBmp);
        return E_FAIL;
    }
    
    VMRALPHABITMAP bmpInfo;
    ZeroMemory(&bmpInfo, sizeof(bmpInfo) );
    bmpInfo.dwFlags = VMRBITMAP_HDC;
    bmpInfo.hdc = hdcBmp;
    
    // Show the entire bitmap in the top-left corner of the video image.
    SetRect(&bmpInfo.rSrc, 0, 0, bm.bmWidth, bm.bmHeight);
    bmpInfo.rDest.left = 0.f;
    bmpInfo.rDest.top = 0.f;
    bmpInfo.rDest.right = (float)bm.bmWidth / (float)cx;
    bmpInfo.rDest.bottom = (float)bm.bmHeight / (float)cy;
    
    // Set the transparency value (1.0 is opaque, 0.0 is transparent).
    bmpInfo.fAlpha = 0.2f;
    
    IVMRMixerBitmap* pBmp;
    hr = pWc->QueryInterface(IID_IVMRMixerBitmap, (LPVOID *)&pBmp);
    if (SUCCEEDED(hr)) 
    {
        pBmp->SetAlphaBitmap(&bmpInfo);
        pBmp->Release();
    }
    
    DeleteObject(SelectObject(hdcBmp, hbmOld));
    DeleteDC(hdcBmp);
    return hr;
}
```



Os conceitos abordados neste tópico são demonstrados no [exemplo](vmrplayer-sample.md) de aplicativo de exemplo VMRPlayer.

**Criando animações simples com a imagem de bitmap**

Para criar um logotipo de bitmap animado simples, coloque todos os "quadros" de bitmap em uma única imagem, conforme mostrado na ilustração a seguir.

![faixa de imagem do VMR](images/vmr-image-strip.png)

Quando você definir o bitmap inicialmente usando [**IVMRMixerBitmap:: SetAlphaBitmap**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixerbitmap-setalphabitmap), se o bitmap estiver em um HDC, defina o campo **RSrc** da estrutura **VMRALPHABITMAP** para especificar o tamanho do bitmap inteiro dentro do HDC. Os membros **superior** e **esquerdo** da estrutura são definidos como 0 e os membros **direito** e **inferior** são a largura e a altura do bitmap. Se o bitmap estiver em uma superfície do DirectDraw, o tamanho da superfície será conhecido e, portanto, não será necessário especificar rSrc nesse método.

Ao chamar [**IVMRMixerBitmap:: UpdateAlphaBitmapParameters**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixerbitmap-updatealphabitmapparameters), use o membro **rsrc** para os bitmaps hDC e DirectDraw, para especificar o quadro ou retângulo específico dentro da imagem que você deseja exibir e defina o sinalizador **VMRBITMAP \_ SRCRECT** no membro **dwFlags** .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o modo de mixagem do VMR](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



