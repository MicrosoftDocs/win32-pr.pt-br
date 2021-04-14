---
title: Configurando fluxos de texto
description: Configurando fluxos de texto
ms.assetid: d99baac5-69e5-4e0a-9cd6-35b288d8181a
keywords:
- fluxos, configurando fluxos de texto
- codecs, configurando fluxos de texto
- fluxos de texto, configurando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 460369eaae02f636f8ddda8bcca4f29ecfc2e1e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453611"
---
# <a name="configuring-text-streams"></a><span data-ttu-id="0b2bb-106">Configurando fluxos de texto</span><span class="sxs-lookup"><span data-stu-id="0b2bb-106">Configuring Text Streams</span></span>

<span data-ttu-id="0b2bb-107">Os fluxos de texto são essencialmente os mesmos que os fluxos arbitrários personalizados.</span><span class="sxs-lookup"><span data-stu-id="0b2bb-107">Text streams are essentially the same as custom arbitrary streams.</span></span> <span data-ttu-id="0b2bb-108">Não há nenhuma informação de configuração associada a um fluxo de texto para identificar o tipo de codificação de texto, portanto, o objeto do gravador não pode verificar exemplos.</span><span class="sxs-lookup"><span data-stu-id="0b2bb-108">There is no configuration information associated with a text stream to identify the type of text encoding, so the writer object cannot verify samples.</span></span>

<span data-ttu-id="0b2bb-109">Para configurar um fluxo de texto, você deve garantir que a estrutura do [**\_ \_ tipo de mídia do WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) contenha um tipo de mídia principal de texto WMMEDIATYPE \_ .</span><span class="sxs-lookup"><span data-stu-id="0b2bb-109">To configure a text stream, you must ensure that the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure contains a major media type of WMMEDIATYPE\_TEXT.</span></span> <span data-ttu-id="0b2bb-110">Você também deve definir uma taxa de bits e uma janela de buffer para o fluxo.</span><span class="sxs-lookup"><span data-stu-id="0b2bb-110">You must also set a bit rate and buffer window for the stream.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0b2bb-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0b2bb-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b2bb-112">**Calculando valores de taxa de bits e de janela de buffer para fluxos arbitrários**</span><span class="sxs-lookup"><span data-stu-id="0b2bb-112">**Calculating Bit Rate and Buffer Window Values for Arbitrary Streams**</span></span>](calculating-bit-rate-and-buffer-window-values-for-arbitrary-streams.md)
</dt> <dt>

[<span data-ttu-id="0b2bb-113">**Configuração comum a todos os fluxos**</span><span class="sxs-lookup"><span data-stu-id="0b2bb-113">**Configuration Common to All Streams**</span></span>](configuration-common-to-all-streams.md)
</dt> <dt>

[<span data-ttu-id="0b2bb-114">**Configurando tipos de fluxo arbitrários**</span><span class="sxs-lookup"><span data-stu-id="0b2bb-114">**Configuring Arbitrary Stream Types**</span></span>](configuring-arbitrary-stream-types.md)
</dt> <dt>

[<span data-ttu-id="0b2bb-115">**Fluxos de texto**</span><span class="sxs-lookup"><span data-stu-id="0b2bb-115">**Text Streams**</span></span>](text-streams.md)
</dt> </dl>

 

 




