---
title: Exibir um bitmap fornecido pelo aplicativo na imagem composta
description: Exibindo um Application-Supplied bitmap na imagem composta
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
# <a name="display-an-app-supplied-bitmap-on-the-composited-image"></a>Exibir um bitmap fornecido pelo aplicativo na imagem composta

Os aplicativos podem usar o modo de combinação da VMR para exibir logotipos de canal alfa-blended, uma interface do usuário ou anúncios parcial ou completamente dentro do retângulo de vídeo. Como a combinação é executada em hardware pelo processador de gráficos, há um impacto mínimo no desempenho de reprodução do Fluxo de Vídeo e não há nenhuma cintilação detectável ou artefatos de desmantelhamento. Os aplicativos podem alterar a imagem exibida com a frequência que desejar. Deve-se lembrar que as alterações só são refletidas na tela quando o DirectShow de filtro está no estado de execução.

A VMR usa seu componente de mixer para sobrepor o bitmap à imagem composta. Com a VMR-7, o aplicativo deve forçar a VMR a carregar seu mixer, mesmo que haja apenas um único fluxo de vídeo. Isso não é necessário com a VMR-9, pois ele carrega seu mixer por padrão.

Para combinar uma imagem de bitmap estático com o fluxo de vídeo, o aplicativo cria a VMR e a adiciona ao grafo e, em seguida, chama [**IVMRFilterConfig::SetNumberOfStreams**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams). O valor passado para essa função identifica o número de pinos de entrada que a VMR deve criar. Os aplicativos podem especificar qualquer valor entre 1 e MAX MIXER STREAMS; especificar um valor de 1 é válido se o aplicativo pretende exibir apenas um único fluxo \_ \_ de vídeo. Embora a VMR-7 tenha um único pino de entrada por padrão, esse método deve ser chamado para forçá-lo a carregar seu componente de mixer. (A VMR-9 carrega seu mixer e configura quatro pinos por padrão.)

Para definir o bitmap, use a interface [**IVMRMixerBitmap**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap) na interface VMR-7 ou [**IVMRMixerBitmap9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9) na VMR-9.

O bitmap pode ser especificado por um handle para um hDC (Contexto de Dispositivo GDI) ou por uma interface do DirectDraw Surface. Se o aplicativo quiser que a imagem contenha informações alfa inseridas (também conhecidas como alfa por pixel), ele deverá colocar os dados de imagem em uma interface do DirectDraw Surface. Isso ocorre porque, no momento, não é possível colocar informações alfa por pixel com um contexto de dispositivo GDI. A superfície do DirectDraw deve ser RGB32 ou ARGB32 e, preferencialmente, ser uma superfície de memória do sistema. Não é necessário que as dimensões da superfície sejam uma potência de 2.

A VMR permite que os aplicativos especifiquem o local e um valor de transparência geral para a imagem. O código a seguir mostra como passar dados de imagem para a VMR para mesclagem subsequente:


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



Os conceitos discutidos neste tópico são demonstrados no aplicativo de exemplo [de exemplo VMRPlayer.](vmrplayer-sample.md)

**Criando animações simples com a imagem bitmap**

Para criar um logotipo de bitmap animado simples, coloque todos os "quadros" de bitmap em uma única imagem, conforme mostrado na ilustração a seguir.

![faixa de imagem vmr](images/vmr-image-strip.png)

Quando você definir o bitmap inicialmente usando [**IVMRMixerBitmap::SetAlphaBitmap**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixerbitmap-setalphabitmap), se o bitmap estiver em um HDC, de definido o **campo rSrc** da estrutura **VMRALPHABITMAP** para especificar o tamanho de todo o bitmap dentro do HDC. Os **membros** superior **e** esquerdo da estrutura são  definidos  como 0 e os membros direito e inferior são a largura e a altura do bitmap. Se o bitmap estiver em uma superfície directDraw, o tamanho da superfície será conhecido, portanto, não há necessidade de especificar rSrc nesse método.

Ao chamar [**IVMRMixerBitmap::UpdateAlphaBitmapParameters**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixerbitmap-updatealphabitmapparameters), use o membro **rSrc** para bitmaps HDC e DirectDraw, para especificar o quadro ou retângulo específico dentro da imagem que você deseja exibir e definir o sinalizador **\_ SRCRECT VMRBITMAP** no membro **dwFlags.**

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o modo de combinação de VMR](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



