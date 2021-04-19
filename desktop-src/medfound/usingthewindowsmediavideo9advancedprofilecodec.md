---
description: Usando o perfil do Windows Media Video 9 avançado
ms.assetid: 2abc0efc-dd11-4921-897c-209a26f8ba1d
title: Usando o perfil do Windows Media Video 9 avançado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 692243117cde3b4b5f1179c5f7324d25842191b6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105784181"
---
# <a name="using-the-windows-media-video-9-advanced-profile"></a><span data-ttu-id="7d952-103">Usando o perfil do Windows Media Video 9 avançado</span><span class="sxs-lookup"><span data-stu-id="7d952-103">Using the Windows Media Video 9 Advanced Profile</span></span>

<span data-ttu-id="7d952-104">Os procedimentos básicos de vídeo descritos na seção [trabalhando com vídeo](workingwithvideo.md) também se aplicam diretamente ao perfil do Windows Media Video 9 avançado.</span><span class="sxs-lookup"><span data-stu-id="7d952-104">The basic video procedures described in the [Working with Video](workingwithvideo.md) section also apply directly to the Windows Media Video 9 Advanced Profile.</span></span> <span data-ttu-id="7d952-105">Nenhum procedimento especial é necessário.</span><span class="sxs-lookup"><span data-stu-id="7d952-105">No special procedures are required.</span></span>

<span data-ttu-id="7d952-106">O perfil do Windows Media Video 9 avançado está associado aos identificadores de classe CLSID \_ CWMV9EncMediaObject e CLSID \_ CWMVDecMediaObject.</span><span class="sxs-lookup"><span data-stu-id="7d952-106">The Windows Media Video 9 Advanced Profile is associated with the class identifiers CLSID\_CWMV9EncMediaObject and CLSID\_CWMVDecMediaObject.</span></span> <span data-ttu-id="7d952-107">O valor FOURCC para os tipos de mídia usando esse codec é "WVC1".</span><span class="sxs-lookup"><span data-stu-id="7d952-107">The FOURCC value for media types using this codec is "WVC1".</span></span>

<span data-ttu-id="7d952-108">O perfil Windows Media Video 9 avançado dá suporte a todos os modos de codificação comuns, bem como codificação entrelaçada, codificação entrelaçada mista e progressiva, resoluções que são diferentes dos recursos de exibição e redução de intervalo.</span><span class="sxs-lookup"><span data-stu-id="7d952-108">The Windows Media Video 9 Advanced Profile supports all common encoding modes as well interlaced encoding, mixed interlaced and progressive encoding, resolutions that are different than the display, and range reduction features.</span></span> <span data-ttu-id="7d952-109">Outro recurso é a capacidade de armazenar metadados de sequência e de quadro no próprio fluxo de bits; anteriormente, isso tinha exigido o uso do ASF e da API de extensões de unidade de dados.</span><span class="sxs-lookup"><span data-stu-id="7d952-109">Another feature is the ability to store sequence and frame metadata in the bit-stream itself; previously this had required use of the ASF and Data Unit Extensions API.</span></span>

<span data-ttu-id="7d952-110">As propriedades a seguir do perfil avançado do Windows Media Video 9, que podem ser controladas usando as configurações do registro, não têm as cadeias de caracteres **IPropertyBag** ou **IPropertyStore** correspondentes:</span><span class="sxs-lookup"><span data-stu-id="7d952-110">The following properties of the Windows Media Video 9 Advanced Profile, which can be controlled using registry settings, do not have corresponding **IPropertyBag** or **IPropertyStore** strings:</span></span>

-   <span data-ttu-id="7d952-111">Opção Dquant.</span><span class="sxs-lookup"><span data-stu-id="7d952-111">Dquant Option.</span></span>
-   <span data-ttu-id="7d952-112">Intensidade de Dquant.</span><span class="sxs-lookup"><span data-stu-id="7d952-112">Dquant Strength.</span></span>
-   <span data-ttu-id="7d952-113">Forçar sobreposição.</span><span class="sxs-lookup"><span data-stu-id="7d952-113">Force Overlap.</span></span>
-   <span data-ttu-id="7d952-114">Método de custo de vetor de movimento.</span><span class="sxs-lookup"><span data-stu-id="7d952-114">Motion Vector Cost Method.</span></span>

## <a name="achieving-optimal-visual-quality"></a><span data-ttu-id="7d952-115">Obtendo qualidade visual ideal</span><span class="sxs-lookup"><span data-stu-id="7d952-115">Achieving Optimal Visual Quality</span></span>

<span data-ttu-id="7d952-116">Para a maioria dos dados de vídeo, para obter a qualidade visual ideal usando o perfil do Windows Media Video 9 avançado, você pode definir a propriedade [MFPKEY \_ COMPRESSIONOPTIMIZATIONTYPE](mfpkey-compressionoptimizationtypeproperty.md) como 1.</span><span class="sxs-lookup"><span data-stu-id="7d952-116">For most video data, to achieve optimal visual quality using the Windows Media Video 9 Advanced Profile, you can set the [MFPKEY\_COMPRESSIONOPTIMIZATIONTYPE](mfpkey-compressionoptimizationtypeproperty.md) property to 1.</span></span>

## <a name="about-the-previous-windows-media-video-9-advanced-profile-codecs"></a><span data-ttu-id="7d952-117">Sobre os codecs de perfil avançado do Windows Media monitor 9 Advanced</span><span class="sxs-lookup"><span data-stu-id="7d952-117">About the Previous Windows Media Video 9 Advanced Profile Codecs</span></span>

<span data-ttu-id="7d952-118">A versão atual do codec de perfil avançado do Windows Media Video 9 é baseada no perfil da sociedade de imagem do Motion (421M) para VC-1 (SMPTE) (padrão de engenharia de vídeo) e avançado.</span><span class="sxs-lookup"><span data-stu-id="7d952-118">The current version of the Windows Media Video 9 Advanced Profile codec is based on the Society of Motion Picture and Television Engineers (SMPTE) standard for VC-1 (SMPTE 421M) Advanced Profile.</span></span> <span data-ttu-id="7d952-119">Esse codec substitui o codec anterior do Windows também chamado de codec de perfil avançado do Windows Media Video 9, que foi identificado pelo código FOURCC "WMVA".</span><span class="sxs-lookup"><span data-stu-id="7d952-119">This codec replaces the earlier codec from Windows also called the Windows Media Video 9 Advanced Profile codec which was identified by the FOURCC code "WMVA".</span></span> <span data-ttu-id="7d952-120">A versão anterior do codec VC-1 foi implementada antes de o padrão de perfil avançado VC-1 ter sido finalizado e não é mais suportado.</span><span class="sxs-lookup"><span data-stu-id="7d952-120">The previous version of the VC-1 codec was implemented before the VC-1 advanced profile standard was finalized, and is no longer supported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7d952-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7d952-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d952-122">Trabalhando com vídeo</span><span class="sxs-lookup"><span data-stu-id="7d952-122">Working with Video</span></span>](workingwithvideo.md)
</dt> 
<dt>

[<span data-ttu-id="7d952-123">Usando as configurações avançadas do codec de perfil avançado do Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="7d952-123">Using the Advanced Settings of the Windows Media Video 9 Advanced Profile Codec</span></span>](https://www.microsoft.com/windows/windowsmedia/howto/articles/codecadvancedsettings.aspx)
</dt> </dl>

 

 



