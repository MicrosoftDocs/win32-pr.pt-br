---
description: 'Saiba mais sobre: Implementando um decodificador de WIC-Enabled'
ms.assetid: a26a592d-42ef-4690-95b4-48a5324be75a
title: Implementando um decodificador de WIC-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ebd6d56258bf18e6cc914a40efa4cd3a57a92fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829211"
---
# <a name="implementing-a-wic-enabled-decoder"></a><span data-ttu-id="51264-103">Implementando um decodificador de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="51264-103">Implementing a WIC-Enabled Decoder</span></span>


<span data-ttu-id="51264-104">A implementação de um decodificador do Windows Imaging Component (WIC) requer a gravação de duas classes.</span><span class="sxs-lookup"><span data-stu-id="51264-104">Implementing a Windows Imaging Component (WIC) decoder requires writing two classes.</span></span> <span data-ttu-id="51264-105">As interfaces nessas classes correspondem diretamente às responsabilidades do decodificador descritas na seção [decodificação](-wic-howwicworks.md) de [como o Windows Imaging Component funciona](-wic-howwicworks.md).</span><span class="sxs-lookup"><span data-stu-id="51264-105">The interfaces on these classes correspond directly to the decoder responsibilities outlined in the [Decoding](-wic-howwicworks.md) section of [How The Windows Imaging Component Works](-wic-howwicworks.md).</span></span>

<span data-ttu-id="51264-106">Uma das classes fornece serviços de nível de contêiner e implementa a interface [IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md) .</span><span class="sxs-lookup"><span data-stu-id="51264-106">One of the classes provides container-level services and implements the [IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md) interface.</span></span> <span data-ttu-id="51264-107">Se o formato de imagem der suporte a metadados em nível de contêiner, você também deverá implementar a interface [IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md) nessa classe.</span><span class="sxs-lookup"><span data-stu-id="51264-107">If your image format supports container-level metadata, you must also implement the [IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md) interface on this class.</span></span> <span data-ttu-id="51264-108">É recomendável que você dê suporte à interface [IWICBitmapCodecProgressNotification](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md) no decodificador e no codificador para dar suporte a uma melhor experiência do usuário.</span><span class="sxs-lookup"><span data-stu-id="51264-108">It is recommended that you support the [IWICBitmapCodecProgressNotification](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md) interface on both the decoder and encoder to support a better user experience.</span></span>

<span data-ttu-id="51264-109">A outra classe que você implementará fornece serviços de nível de quadro e fará a decodificação real dos bits de imagem para cada quadro no contêiner.</span><span class="sxs-lookup"><span data-stu-id="51264-109">The other class you will implement provides frame-level services and does the actual decoding of the image bits for each frame in the container.</span></span> <span data-ttu-id="51264-110">Essa classe implementa a interface [IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md) e a interface [IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md) .</span><span class="sxs-lookup"><span data-stu-id="51264-110">This class implements the [IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md) interface and the [IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md) interface.</span></span> <span data-ttu-id="51264-111">Se você estiver escrevendo um decodificador para um formato bruto, também implementará a interface [IWICDevelopRaw](-wic-imp-iwicdevelopraw.md) nessa classe.</span><span class="sxs-lookup"><span data-stu-id="51264-111">If you are writing a decoder for a raw format, you also implement the [IWICDevelopRaw](-wic-imp-iwicdevelopraw.md) interface on this class.</span></span> <span data-ttu-id="51264-112">Além das interfaces necessárias, é altamente recomendável que você implemente a interface [IWICBitmapSourceTransform](-wic-imp-iwicmetadatablockreader.md) nessa classe para habilitar o melhor desempenho possível para seu formato de imagem.</span><span class="sxs-lookup"><span data-stu-id="51264-112">In addition to the required interfaces, it is highly recommended that you implement the [IWICBitmapSourceTransform](-wic-imp-iwicmetadatablockreader.md) interface on this class to enable the best possible performance for your image format.</span></span>

<span data-ttu-id="51264-113">Um dos objetos fornecidos pelo WIC é o [**ImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory).</span><span class="sxs-lookup"><span data-stu-id="51264-113">One of the objects provided by WIC is the [**ImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory).</span></span> <span data-ttu-id="51264-114">Você usa frequentemente a interface [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) nesse objeto para criar vários componentes.</span><span class="sxs-lookup"><span data-stu-id="51264-114">You frequently use the [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) interface on this object to create various components.</span></span> <span data-ttu-id="51264-115">Como ele é usado com frequência, você deve manter uma referência a ele como uma propriedade de membro nas classes do decodificador e do codificador.</span><span class="sxs-lookup"><span data-stu-id="51264-115">Because it is used frequently, you should keep a reference to it as a member property on both your decoder and encoder classes.</span></span>


```C++
IWICImagingFactory* m_pImagingFactory = NULL;
IWICComponentFactory* m_pComponentFactory = NULL;
HRESULT hr;
      
hr = CoCreateInstance(CLSID_WICImagingFactory, NULL,
  CLSCTX_INPROC_SERVER, IID_IWICImagingFactory,
  (LPVOID*) m_pImagingFactory);

hr = m_pImagingFactory->QueryInterface(
  IID_IWICComponentFactory, (void**)&m_pComponentFactory);
```



## <a name="related-topics"></a><span data-ttu-id="51264-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="51264-116">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="51264-117">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="51264-117">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="51264-118">Como funciona o Windows Imaging Component</span><span class="sxs-lookup"><span data-stu-id="51264-118">How The Windows Imaging Component Works</span></span>](-wic-howwicworks.md)
</dt> <dt>

[<span data-ttu-id="51264-119">Interfaces do decodificador</span><span class="sxs-lookup"><span data-stu-id="51264-119">Decoder Interfaces</span></span>](-wic-decoderinterfaces.md)
</dt> <dt>

[<span data-ttu-id="51264-120">Como escrever um CODEC de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="51264-120">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="51264-121">Visão geral do Windows Imaging Component</span><span class="sxs-lookup"><span data-stu-id="51264-121">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="51264-122">Visão geral dos metadados do WIC</span><span class="sxs-lookup"><span data-stu-id="51264-122">WIC Metadata Overview</span></span>](-wic-about-metadata.md)
</dt> <dt>

[<span data-ttu-id="51264-123">Visão geral da codificação</span><span class="sxs-lookup"><span data-stu-id="51264-123">Encoding Overview</span></span>](-wic-creating-encoder.md)
</dt> </dl>

 

 



