---
description: A codificação de duas passagens pode ser usada para a taxa de bits constante (CBR) e para a codificação de taxa de bits variável (VBR) com alguns dos codecs de mídia do Windows.
ms.assetid: eec5085c-9441-496a-8127-cf5d2686d917
title: Usando a codificação Two-Pass (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 993af0015452db410b5a9f2c13233566fc17a3a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782971"
---
# <a name="using-two-pass-encoding-microsoft-media-foundation"></a><span data-ttu-id="9fa7e-103">Usando a codificação Two-Pass (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="9fa7e-103">Using Two-Pass Encoding (Microsoft Media Foundation)</span></span>

<span data-ttu-id="9fa7e-104">A codificação de duas passagens pode ser usada para a taxa de bits constante (CBR) e para a codificação de taxa de bits variável (VBR) com alguns dos codecs de mídia do Windows.</span><span class="sxs-lookup"><span data-stu-id="9fa7e-104">Two-pass encoding can be used for constant bit rate (CBR) and for variable bit rate (VBR) encoding with some of the Windows Media codecs.</span></span> <span data-ttu-id="9fa7e-105">Você pode encontrar o número máximo de passagens de codificação com suporte por um codec recuperando a propriedade [MFPKEY \_ PASSESRECOMMENDED](mfpkey-passesrecommendedproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="9fa7e-105">You can find the maximum number of encoding passes supported by a codec by retrieving the [MFPKEY\_PASSESRECOMMENDED](mfpkey-passesrecommendedproperty.md) property.</span></span> <span data-ttu-id="9fa7e-106">Nenhum dos codecs dá suporte a mais de duas passagens.</span><span class="sxs-lookup"><span data-stu-id="9fa7e-106">None of the codecs supports more than two passes.</span></span> <span data-ttu-id="9fa7e-107">Configure o DMO para usar duas passagens definindo a propriedade [MFPKEY \_ PASSESUSED](mfpkey-passesusedproperty.md) como 2.</span><span class="sxs-lookup"><span data-stu-id="9fa7e-107">Configure the DMO to use two passes by setting the [MFPKEY\_PASSESUSED](mfpkey-passesusedproperty.md) property to 2.</span></span>

<span data-ttu-id="9fa7e-108">Entregue os exemplos ao codificador DMO, um de cada vez, como você faria em um modo de passagem única.</span><span class="sxs-lookup"><span data-stu-id="9fa7e-108">Deliver the samples to the encoder DMO one at a time, as you would in a one-pass mode.</span></span> <span data-ttu-id="9fa7e-109">Quando você processa os exemplos de entrada para sua passagem de pré-processamento, as chamadas para [**IMediaObject::P rocessinput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput) ou [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) retornará **S \_ false**, para indicar que nenhuma saída é produzida.</span><span class="sxs-lookup"><span data-stu-id="9fa7e-109">When you process the input samples for your preprocessing pass, the calls to [**IMediaObject::ProcessInput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput) or [**IMFTransform::ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) will return **S\_FALSE**, to indicate that no output is produced.</span></span>

<span data-ttu-id="9fa7e-110">No final da primeira passagem (após a última entrada ser processada pela primeira vez), você deve definir a propriedade [MFPKEY \_ ENDOFPASS](mfpkey-endofpassproperty.md) para notificar o codec de que a próxima entrada processada é a primeira entrada da segunda passagem.</span><span class="sxs-lookup"><span data-stu-id="9fa7e-110">At the end of the first pass (after the last input is processed for the first time), you then must set the [MFPKEY\_ENDOFPASS](mfpkey-endofpassproperty.md) property to notify the codec that the next input processed is the first input of the second pass.</span></span> <span data-ttu-id="9fa7e-111">Nenhum valor é necessário para essa propriedade, portanto, você deve usar uma estrutura **Variant** vazia.</span><span class="sxs-lookup"><span data-stu-id="9fa7e-111">No value is required for this property, so you should use an empty **VARIANT** structure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9fa7e-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9fa7e-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9fa7e-113">Codificações de mídia do Windows</span><span class="sxs-lookup"><span data-stu-id="9fa7e-113">Windows Media Codecs</span></span>](windows-media-codecs.md)
</dt> </dl>

 

 
