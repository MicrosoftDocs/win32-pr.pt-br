---
description: Usando uma lista de decisões de edição para codificação de voz
ms.assetid: a3d88483-acc9-47cf-8735-f17bd3b4ad57
title: Usando uma lista de decisões de edição para codificação de voz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 970cc40bc5749b9edc1017546020fa3806a9730b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749180"
---
# <a name="using-an-editing-decision-list-for-encoding-voice"></a><span data-ttu-id="7f0c3-103">Usando uma lista de decisões de edição para codificação de voz</span><span class="sxs-lookup"><span data-stu-id="7f0c3-103">Using an Editing Decision List for Encoding Voice</span></span>

<span data-ttu-id="7f0c3-104">Uma EDL (lista de decisões de edição), são dados fornecidos a um codec que fornece informações sobre como partes específicas de conteúdo devem ser codificadas.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-104">An editing decision list (EDL), is data given to a codec that provides information about how specific portions of content should be encoded.</span></span> <span data-ttu-id="7f0c3-105">O codec de voz do Windows Media Audio 9 dá suporte a uma EDL simples na qual você pode especificar as partes do conteúdo que contêm música.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-105">The Windows Media Audio 9 Voice codec supports a simple EDL in which you can specify the portions of content that contain music.</span></span> <span data-ttu-id="7f0c3-106">Por padrão, o codec detecta passagens de música em si quando configurado para codificar conteúdo misto.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-106">By default, the codec detects passages of music itself when configured to encode mixed content.</span></span> <span data-ttu-id="7f0c3-107">Você deve usar um EDL somente se o codec não estiver detectando os tipos de conteúdo corretamente.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-107">You should use an EDL only if the codec is not detecting the content types correctly.</span></span>

<span data-ttu-id="7f0c3-108">Para usar uma EDL, o codificador de voz deve ser definido para codificar conteúdo misto.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-108">To use an EDL, the voice encoder must be set to encode mixed content.</span></span> <span data-ttu-id="7f0c3-109">Configure o modo do codec de voz para "misto" definindo a propriedade [MFPKEY \_ WMAVOICE \_ ENC \_ MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) como 2.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-109">Configure the mode of the voice codec to "mixed" by setting the [MFPKEY\_WMAVOICE\_ENC\_MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) property to 2.</span></span> <span data-ttu-id="7f0c3-110">Defina o EDL usando a propriedade [MFPKEY \_ WMAVOICE \_ ENC \_ EDL](mfpkey-wmavoice-enc-edlproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="7f0c3-110">Set the EDL using the [MFPKEY\_WMAVOICE\_ENC\_EDL](mfpkey-wmavoice-enc-edlproperty.md) property.</span></span> <span data-ttu-id="7f0c3-111">O valor dessa propriedade é uma cadeia de caracteres que contém uma lista delimitada por vírgulas dos intervalos de tempo no conteúdo que deve ser codificado como música.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-111">The value of this property is a string containing a comma-delimited list of the time ranges in the content that should be encoded as music.</span></span> <span data-ttu-id="7f0c3-112">O primeiro item da lista é a versão do EDL, que é sempre 1.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-112">The first item in the list is the version of the EDL, which is always 1.</span></span> <span data-ttu-id="7f0c3-113">O segundo item é o número de seções de música descritas na lista.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-113">The second item is the number of music sections described in the list.</span></span> <span data-ttu-id="7f0c3-114">Seguir o segundo item são um número de pares de valores iguais ao segundo item; cada par de valores descreve o ponto inicial e final de uma passagem de música no conteúdo, em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-114">Following the second item are a number of pairs of values equal to the second item; each pair of values describes the starting and ending point of a music passage in the content, in milliseconds.</span></span>

<span data-ttu-id="7f0c3-115">Por exemplo, a cadeia de caracteres EDL "1, 4, 1000, 2000, 5000, 6000, 9000, 10000, 13000, 14000" especifica quatro passagens musicais, cada uma delas com um segundo.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-115">For example, the EDL string "1, 4, 1000, 2000, 5000, 6000, 9000, 10000, 13000, 14000" specifies four musical passages, each of which is one second long.</span></span> <span data-ttu-id="7f0c3-116">Se as informações na cadeia de caracteres do EDL forem inválidas, elas serão ignoradas.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-116">If the information in the EDL string is invalid, it is ignored.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7f0c3-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7f0c3-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f0c3-118">Usando o codec de voz do Windows Media Audio 9</span><span class="sxs-lookup"><span data-stu-id="7f0c3-118">Using the Windows Media Audio 9 Voice Codec</span></span>](usingthewindowsmediaaudio9voicecodec.md)
</dt> <dt>

[<span data-ttu-id="7f0c3-119">Trabalhando com áudio</span><span class="sxs-lookup"><span data-stu-id="7f0c3-119">Working with Audio</span></span>](workingwithaudio.md)
</dt> </dl>

 

 



