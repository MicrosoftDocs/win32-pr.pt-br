---
title: Exibir um bitmap fornecido pelo aplicativo na imagem compostada
description: Exibindo um bitmap Application-Supplied na imagem compostada
ms.assetid: c51329d3-e814-4ef9-aad8-a3e60f9fa2a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06ecd8ac931d0a0bb83eafba09d8ca7dc8263f0d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500181"
---
# <a name="display-an-app-supplied-bitmap-on-the-composited-image"></a><span data-ttu-id="5e810-103">Exibir um bitmap fornecido pelo aplicativo na imagem compostada</span><span class="sxs-lookup"><span data-stu-id="5e810-103">Display an app-supplied bitmap on the composited image</span></span>

<span data-ttu-id="5e810-104">Os aplicativos podem usar o modo de mistura do VMR para exibir logotipos de canal com combinação alfabética, uma interface do usuário ou anúncios de forma parcial ou completa dentro do retângulo do vídeo.</span><span class="sxs-lookup"><span data-stu-id="5e810-104">Applications can use the VMR's mixing mode to display alpha-blended channel logos, a user interface, or advertisements either partially or completely within the video rectangle.</span></span> <span data-ttu-id="5e810-105">Como a mesclagem é realizada no hardware pelo processador de gráficos, há um impacto mínimo sobre o desempenho de reprodução do fluxo de vídeo e não há nenhuma cintilação detectável ou artefatos de divisão.</span><span class="sxs-lookup"><span data-stu-id="5e810-105">Because the blending is performed in hardware by the graphics processor, there is minimal impact to the playback performance of the Video Stream, and there are no detectable flicker or tearing artifacts.</span></span> <span data-ttu-id="5e810-106">Os aplicativos podem alterar a imagem exibida com a frequência desejada.</span><span class="sxs-lookup"><span data-stu-id="5e810-106">Applications can change the image displayed as frequently as they wish.</span></span> <span data-ttu-id="5e810-107">Deve-se observar que as alterações só são refletidas na tela quando o grafo de filtro do DirectShow está no estado executando.</span><span class="sxs-lookup"><span data-stu-id="5e810-107">It should be noted that changes are only reflected on the screen when the DirectShow filter graph is in the running state.</span></span>

<span data-ttu-id="5e810-108">O VMR usa seu componente de mixer para sobrepor o bitmap na imagem compostada.</span><span class="sxs-lookup"><span data-stu-id="5e810-108">The VMR uses its mixer component to overlay the bitmap onto the composited image.</span></span> <span data-ttu-id="5e810-109">Com o VMR-7, o aplicativo deve forçar o VMR a carregar seu mixer, mesmo que haja apenas um único fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="5e810-109">With the VMR-7, the application must force the VMR to load its mixer, even if there is only a single video stream.</span></span> <span data-ttu-id="5e810-110">Isso não é necessário com o VMR-9, já que ele carrega seu mixer por padrão.</span><span class="sxs-lookup"><span data-stu-id="5e810-110">This is not necessary with the VMR-9 since it loads its mixer by default.</span></span>

<span data-ttu-id="5e810-111">Para misturar uma imagem de bitmap estática com o fluxo de vídeo, o aplicativo cria o VMR e o adiciona ao grafo e, em seguida, chama [**IVMRFilterConfig:: SetNumberOfStreams**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams).</span><span class="sxs-lookup"><span data-stu-id="5e810-111">To blend a static bitmap image with the video stream, the application creates the VMR and adds it to the graph, and then calls [**IVMRFilterConfig::SetNumberOfStreams**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams).</span></span> <span data-ttu-id="5e810-112">O valor passado para essa função identifica o número de Pins de entrada que o VMR deve criar.</span><span class="sxs-lookup"><span data-stu-id="5e810-112">The value passed to this function identifies the number of input pins that the VMR should create.</span></span> <span data-ttu-id="5e810-113">Os aplicativos podem especificar qualquer valor entre 1 e \_ o máximo de fluxos de mixer \_ ; especificar um valor de 1 será válido se o aplicativo pretender exibir apenas um fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="5e810-113">Applications can specify any value between 1 and MAX\_MIXER\_STREAMS; specifying a value of 1 is valid if the application only intends to display a single video stream.</span></span> <span data-ttu-id="5e810-114">Embora o VMR-7 tenha um único PIN de entrada por padrão, esse método deve ser chamado para forçá-lo a carregar seu componente de mixer.</span><span class="sxs-lookup"><span data-stu-id="5e810-114">Even though the VMR-7 has a single input pin by default, this method must be called in order to force it to load its mixer component.</span></span> <span data-ttu-id="5e810-115">(O VMR-9 carrega seu mixer e configura quatro Pins por padrão.)</span><span class="sxs-lookup"><span data-stu-id="5e810-115">(The VMR-9 loads its mixer and sets up four pins by default.)</span></span>

<span data-ttu-id="5e810-116">Para definir o bitmap, use a interface [**IVMRMixerBitmap**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap) no VMR-7 ou na interface [**IVMRMixerBitmap9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9) no VMR-9.</span><span class="sxs-lookup"><span data-stu-id="5e810-116">To set the bitmap, use the [**IVMRMixerBitmap**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap) interface on the VMR-7 or the [**IVMRMixerBitmap9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9) interface on the VMR-9.</span></span>

<span data-ttu-id="5e810-117">O bitmap pode ser especificado por um identificador para um contexto de dispositivo GDI (hDC) ou por uma interface de superfície do DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="5e810-117">The bitmap can be specified by either a handle to a GDI Device Context (hDC) or by a DirectDraw Surface interface.</span></span> <span data-ttu-id="5e810-118">Se o aplicativo quiser que a imagem contenha informações alfa incorporadas (também conhecidas por pixel alfa), ele deverá posicionar os dados da imagem em uma interface de superfície do DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="5e810-118">If the application wants the image to contain embedded alpha information (also known as per pixel alpha) it must place the image data in a DirectDraw Surface interface.</span></span> <span data-ttu-id="5e810-119">Isso ocorre porque atualmente não é possível inserir informações alfa por pixel com um contexto de dispositivo GDI.</span><span class="sxs-lookup"><span data-stu-id="5e810-119">This is because it is not currently possible to place per-pixel alpha information with a GDI Device Context.</span></span> <span data-ttu-id="5e810-120">A superfície do DirectDraw deve ser RGB32 ou ARGB32, e, preferencialmente, ser uma superfície de memória do sistema.</span><span class="sxs-lookup"><span data-stu-id="5e810-120">The DirectDraw surface must be either RGB32 or ARGB32, and should preferably be a system memory surface.</span></span> <span data-ttu-id="5e810-121">Não é necessário que as dimensões da superfície sejam uma potência de 2.</span><span class="sxs-lookup"><span data-stu-id="5e810-121">It is not necessary for the surface dimensions to be a power of 2.</span></span>

<span data-ttu-id="5e810-122">O VMR permite que os aplicativos especifiquem o local e um valor de transparência geral para a imagem.</span><span class="sxs-lookup"><span data-stu-id="5e810-122">The VMR allows applications to specify the location and an overall transparency value for the image.</span></span> <span data-ttu-id="5e810-123">O código a seguir mostra como transmitir dados de imagem para o VMR para mesclagem subsequente:</span><span class="sxs-lookup"><span data-stu-id="5e810-123">The following code shows how to pass image data down to the VMR for subsequent blending:</span></span>


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



<span data-ttu-id="5e810-124">Os conceitos abordados neste tópico são demonstrados no [exemplo](vmrplayer-sample.md) de aplicativo de exemplo VMRPlayer.</span><span class="sxs-lookup"><span data-stu-id="5e810-124">The concepts discussed in this topic are demonstrated in the [VMRPlayer Sample](vmrplayer-sample.md) sample application.</span></span>

<span data-ttu-id="5e810-125">**Criando animações simples com a imagem de bitmap**</span><span class="sxs-lookup"><span data-stu-id="5e810-125">**Creating Simple Animations with the Bitmap Image**</span></span>

<span data-ttu-id="5e810-126">Para criar um logotipo de bitmap animado simples, coloque todos os "quadros" de bitmap em uma única imagem, conforme mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="5e810-126">To create a simple animated bitmap logo, put all of the bitmap "frames" into a single image, as shown in the following illustration.</span></span>

![faixa de imagem do VMR](images/vmr-image-strip.png)

<span data-ttu-id="5e810-128">Quando você definir o bitmap inicialmente usando [**IVMRMixerBitmap:: SetAlphaBitmap**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixerbitmap-setalphabitmap), se o bitmap estiver em um HDC, defina o campo **RSrc** da estrutura **VMRALPHABITMAP** para especificar o tamanho do bitmap inteiro dentro do HDC.</span><span class="sxs-lookup"><span data-stu-id="5e810-128">When you set the bitmap initially using [**IVMRMixerBitmap::SetAlphaBitmap**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixerbitmap-setalphabitmap), if the bitmap is in an HDC, set the **rSrc** field of the **VMRALPHABITMAP** structure to specify the size of the entire bitmap within the HDC.</span></span> <span data-ttu-id="5e810-129">Os membros **superior** e **esquerdo** da estrutura são definidos como 0 e os membros **direito** e **inferior** são a largura e a altura do bitmap.</span><span class="sxs-lookup"><span data-stu-id="5e810-129">The **top** and **left** members of the structure are set to 0, and the **right** and **bottom** members are the width and height of the bitmap.</span></span> <span data-ttu-id="5e810-130">Se o bitmap estiver em uma superfície do DirectDraw, o tamanho da superfície será conhecido e, portanto, não será necessário especificar rSrc nesse método.</span><span class="sxs-lookup"><span data-stu-id="5e810-130">If the bitmap is in a DirectDraw surface, then the size of the surface is known, so there is no need to specify rSrc in this method.</span></span>

<span data-ttu-id="5e810-131">Ao chamar [**IVMRMixerBitmap:: UpdateAlphaBitmapParameters**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixerbitmap-updatealphabitmapparameters), use o membro **rsrc** para os bitmaps hDC e DirectDraw, para especificar o quadro ou retângulo específico dentro da imagem que você deseja exibir e defina o sinalizador **VMRBITMAP \_ SRCRECT** no membro **dwFlags** .</span><span class="sxs-lookup"><span data-stu-id="5e810-131">When you call [**IVMRMixerBitmap::UpdateAlphaBitmapParameters**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixerbitmap-updatealphabitmapparameters), use the **rSrc** member for both HDC and DirectDraw bitmaps, to specify the particular frame or rectangle within the image that you wish to display, and set the **VMRBITMAP\_SRCRECT** flag in the **dwFlags** member.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5e810-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5e810-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e810-133">Usando o modo de mixagem do VMR</span><span class="sxs-lookup"><span data-stu-id="5e810-133">Using VMR Mixing Mode</span></span>](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



