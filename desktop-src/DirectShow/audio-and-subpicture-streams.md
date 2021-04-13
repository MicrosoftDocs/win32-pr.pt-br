---
description: Fluxos de áudio e subimagem
ms.assetid: 8d361da3-a33a-401c-a750-f9b952022cf6
title: Fluxos de áudio e subimagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2f5c8c74f7507557f374d690a671b62e8b43343
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456828"
---
# <a name="audio-and-subpicture-streams"></a><span data-ttu-id="5f3c9-103">Fluxos de áudio e subimagem</span><span class="sxs-lookup"><span data-stu-id="5f3c9-103">Audio and Subpicture Streams</span></span>

<span data-ttu-id="5f3c9-104">Um disco DVD-Video pode ter até oito fluxos de áudio, numerados de zero a sete, cada um com até seis canais discretos.</span><span class="sxs-lookup"><span data-stu-id="5f3c9-104">A DVD-Video disc can have up to eight audio streams, numbered zero through seven, each with up to six discrete channels.</span></span> <span data-ttu-id="5f3c9-105">(Observe que os fluxos de áudio e subimagem são numerados de zero, enquanto os títulos, ângulos e níveis de pais são numerados de um.) Somente um desses fluxos pode ser selecionado em um determinado momento.</span><span class="sxs-lookup"><span data-stu-id="5f3c9-105">(Note that audio and subpicture streams are numbered from zero, whereas titles, angles, and parental levels are numbered from one.) Only one of these streams can be selected at any given time.</span></span> <span data-ttu-id="5f3c9-106">Para subfiguras, até 32 fluxos estão disponíveis, embora apenas um fluxo possa ser ativado em um determinado momento.</span><span class="sxs-lookup"><span data-stu-id="5f3c9-106">For subpictures, up to 32 streams are available, although only one stream can be activated at any given time.</span></span> <span data-ttu-id="5f3c9-107">Os discos geralmente são criados com fluxos de áudio e subimagem padrão, mas um aplicativo pode permitir que os usuários exibam uma lista de todos os fluxos disponíveis e selecione aquele no idioma que preferirem.</span><span class="sxs-lookup"><span data-stu-id="5f3c9-107">Discs are generally authored with default audio and subpicture streams, but an application can enable users to view a list of all the available streams, and select the one in the language they prefer.</span></span> <span data-ttu-id="5f3c9-108">As etapas básicas nesse processo são as mesmas para os fluxos de áudio e subimagem.</span><span class="sxs-lookup"><span data-stu-id="5f3c9-108">The basic steps in this process are the same for both audio and subpicture streams.</span></span>

1.  <span data-ttu-id="5f3c9-109">Determine o número de fluxos disponíveis para um título.</span><span class="sxs-lookup"><span data-stu-id="5f3c9-109">Determine the number of streams available for a title.</span></span>
2.  <span data-ttu-id="5f3c9-110">Itere pelos fluxos e recupere os atributos de fluxo para cada um.</span><span class="sxs-lookup"><span data-stu-id="5f3c9-110">Iterate through the streams and retrieve the stream attributes for each.</span></span>
3.  <span data-ttu-id="5f3c9-111">Recupere o código de idioma do LCID (identificador de localidade) retornado e crie uma cadeia de caracteres legível.</span><span class="sxs-lookup"><span data-stu-id="5f3c9-111">Retrieve the language code from the returned locale identifier (LCID) and create a human-readable string.</span></span>
4.  <span data-ttu-id="5f3c9-112">Preencha uma caixa de listagem ou outro controle de interface do usuário (IU) para permitir que o usuário selecione um fluxo preferencial.</span><span class="sxs-lookup"><span data-stu-id="5f3c9-112">Populate a list box or other user interface (UI) control to enable the user to select a preferred stream.</span></span>

<span data-ttu-id="5f3c9-113">No aplicativo de exemplo de DVD, o método CAudioLangDlg:: MakeAudioStreamList em Dialogs. cpp demonstra as etapas básicas.</span><span class="sxs-lookup"><span data-stu-id="5f3c9-113">In the DVD sample application, the CAudioLangDlg::MakeAudioStreamList method in Dialogs.cpp demonstrates the basic steps.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5f3c9-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5f3c9-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f3c9-115">Aplicativos de DVD</span><span class="sxs-lookup"><span data-stu-id="5f3c9-115">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



