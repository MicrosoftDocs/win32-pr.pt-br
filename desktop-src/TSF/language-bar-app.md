---
title: Barra de idiomas (aplicativos TSF)
description: Um aplicativo não pode adicionar itens à barra de idiomas; somente um serviço de texto pode adicionar itens à barra de idiomas.
ms.assetid: facb0da1-3f80-4745-b021-c026e7e5356c
keywords:
- TSF (estrutura de serviços de texto), barra de idiomas
- TSF (estrutura de serviços de texto), barra de idiomas
- Aplicativos habilitados para TSF, barra de idiomas
- barra de idiomas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef227b29c8b481bfaefc4a218305ba8974fe54e2
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103824132"
---
# <a name="language-bar-tsf-applications"></a><span data-ttu-id="e72ff-107">Barra de idiomas (aplicativos TSF)</span><span class="sxs-lookup"><span data-stu-id="e72ff-107">Language Bar (TSF Applications)</span></span>

<span data-ttu-id="e72ff-108">Um aplicativo não pode adicionar itens à barra de idiomas; somente um serviço de texto pode adicionar itens à barra de idiomas.</span><span class="sxs-lookup"><span data-stu-id="e72ff-108">An application cannot add items to the language bar; only a text service can add items to the language bar.</span></span> <span data-ttu-id="e72ff-109">Um aplicativo pode afetar a aparência de determinados itens na barra de idiomas.</span><span class="sxs-lookup"><span data-stu-id="e72ff-109">An application can affect how certain items on the language bar appear.</span></span>

<span data-ttu-id="e72ff-110">O [compartimento \_ \_ \_ DICTATIONSTAT de fala do compartimento GUID](predefined-compartments.md) é usado para indicar o tipo de entrada de fala que o aplicativo pode aceitar: entrada de texto direto (ditado) e/ou comandos de voz.</span><span class="sxs-lookup"><span data-stu-id="e72ff-110">The [GUID\_COMPARTMENT\_SPEECH\_DICTATIONSTAT](predefined-compartments.md) compartment is used to indicate the type of speech input that the application can accept: direct text input (dictation) and/or voice commands.</span></span> <span data-ttu-id="e72ff-111">Por padrão, o ditado está habilitado e o comando de voz está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="e72ff-111">By default, dictation is enabled and voice command is disabled.</span></span> <span data-ttu-id="e72ff-112">Se o aplicativo puder aceitar comandos de voz, ele deverá definir o valor de [comando do TF \_ \_ habilitado](speech-recognition-constants.md) no \_ compartimento de DICTATIONSTAT de fala do compartimento de GUID \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e72ff-112">If the application can accept voice commands, it should set the [TF\_COMMANDING\_ENABLED](speech-recognition-constants.md) value in the GUID\_COMPARTMENT\_SPEECH\_DICTATIONSTAT compartment.</span></span> <span data-ttu-id="e72ff-113">Se o aplicativo puder aceitar o ditado, ele deverá definir o \_ valor habilitado de ditado TF \_ no compartimento GUID \_ DICTATIONSTAT de \_ fala \_ .</span><span class="sxs-lookup"><span data-stu-id="e72ff-113">If the application can accept dictation, it should set the TF\_DICTATION\_ENABLED value in the GUID\_COMPARTMENT\_SPEECH\_DICTATIONSTAT compartment.</span></span> <span data-ttu-id="e72ff-114">O \_ ditado TF \_ ou o \_ comando TF \_ no valor desse compartimento determina qual modo (ditado ou comando) a entrada de fala está atualmente em.</span><span class="sxs-lookup"><span data-stu-id="e72ff-114">The TF\_DICTATION\_ON or TF\_COMMANDING\_ON value of this compartment determines which mode (dictation or command) speech input is currently in.</span></span>

<span data-ttu-id="e72ff-115">Se o aplicativo oferecer suporte ao armazenamento persistente de dados de propriedade, ele deverá definir o compartimento de [ \_ \_ PERSISTMENUENABLED do compartimento de GUID](predefined-compartments.md) como um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="e72ff-115">If the application supports persistent storage of property data, it should set the [GUID\_COMPARTMENT\_PERSISTMENUENABLED](predefined-compartments.md) compartment to a nonzero value.</span></span> <span data-ttu-id="e72ff-116">Isso faz com que o serviço de texto de fala habilite o item de menu **salvar dados de fala** .</span><span class="sxs-lookup"><span data-stu-id="e72ff-116">This causes the speech text service to enable the **Save Speech Data** menu item.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e72ff-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e72ff-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e72ff-118">Como configurar a estrutura de serviços de texto</span><span class="sxs-lookup"><span data-stu-id="e72ff-118">How To Set Up Text Services Framework</span></span>](how-to-set-up-tsf.md)
</dt> <dt>

[<span data-ttu-id="e72ff-119">Barra de idiomas (serviços de texto)</span><span class="sxs-lookup"><span data-stu-id="e72ff-119">Language Bar (Text Services)</span></span>](language-bar.md)
</dt> </dl>

 

 




