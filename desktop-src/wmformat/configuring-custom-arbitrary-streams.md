---
title: Configurando fluxos arbitrários personalizados
description: Configurando fluxos arbitrários personalizados
ms.assetid: 09b28fd3-a0a3-44d9-b664-7421290abf02
keywords:
- fluxos, configurando fluxos arbitrários personalizados
- codecs, configurando fluxos arbitrários personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29d5cf3e95a5514ddeede9eb3c25df01ed4cd2ae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635789"
---
# <a name="configuring-custom-arbitrary-streams"></a><span data-ttu-id="6d29f-105">Configurando fluxos arbitrários personalizados</span><span class="sxs-lookup"><span data-stu-id="6d29f-105">Configuring Custom Arbitrary Streams</span></span>

<span data-ttu-id="6d29f-106">Ao usar seu próprio tipo de dados arbitrário, você deve criar um valor de GUID para servir como o identificador de tipo de mídia principal para ele.</span><span class="sxs-lookup"><span data-stu-id="6d29f-106">When using your own arbitrary data type, you must create a GUID value to serve as the major media type identifier for it.</span></span> <span data-ttu-id="6d29f-107">Quando o gravador encontra um fluxo em um perfil com um tipo principal que ele não reconhece, ele pressupõe que o fluxo é dados arbitrários personalizados.</span><span class="sxs-lookup"><span data-stu-id="6d29f-107">When the writer encounters a stream in a profile with a major type it does not recognize, it assumes that the stream is custom arbitrary data.</span></span> <span data-ttu-id="6d29f-108">Ele aceitará seus exemplos, os atualizará e os combinará com exemplos de outros fluxos no arquivo sem verificar os dados de qualquer forma.</span><span class="sxs-lookup"><span data-stu-id="6d29f-108">It will accept your samples, packetize them, and combine them with samples from the other streams in the file without verifying the data in any way.</span></span>

<span data-ttu-id="6d29f-109">Você também pode criar seus próprios identificadores GUID de subtipo para definir subcategorias de dados personalizados.</span><span class="sxs-lookup"><span data-stu-id="6d29f-109">You can also create your own subtype GUID identifiers to define subcategories of your custom data.</span></span> <span data-ttu-id="6d29f-110">O gravador irá ignorar esses subtipos completamente, mas eles serão preservados na seção de cabeçalho do arquivo ASF, para que seu aplicativo de leitura possa recuperá-los e tomar decisões com base neles.</span><span class="sxs-lookup"><span data-stu-id="6d29f-110">The writer will ignore these subtypes completely, but they will be preserved in the header section of the ASF file, so your reading application can retrieve them and make decisions based on them.</span></span>

<span data-ttu-id="6d29f-111">Um fluxo arbitrário requer uma taxa de bits e uma janela de buffer e deve ter uma estrutura de [**\_ \_ tipo de mídia do WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) com os valores limpos, exceto o tipo de mídia principal e subtipo (se estiver usando um).</span><span class="sxs-lookup"><span data-stu-id="6d29f-111">An arbitrary stream requires a bit rate and buffer window, and must have a [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure with the values cleared except for the major media type and subtype(if using one).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6d29f-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6d29f-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d29f-113">**Configuração comum a todos os fluxos**</span><span class="sxs-lookup"><span data-stu-id="6d29f-113">**Configuration Common to All Streams**</span></span>](configuration-common-to-all-streams.md)
</dt> <dt>

[<span data-ttu-id="6d29f-114">**Configurando tipos de fluxo arbitrários**</span><span class="sxs-lookup"><span data-stu-id="6d29f-114">**Configuring Arbitrary Stream Types**</span></span>](configuring-arbitrary-stream-types.md)
</dt> <dt>

[<span data-ttu-id="6d29f-115">**Fluxos de dados arbitrários personalizados**</span><span class="sxs-lookup"><span data-stu-id="6d29f-115">**Custom Arbitrary Data Streams**</span></span>](custom-arbitrary-data-streams.md)
</dt> </dl>

 

 




