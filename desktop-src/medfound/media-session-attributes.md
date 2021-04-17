---
description: Atributos de sessão de mídia
ms.assetid: 7f9cef1c-b419-485f-ac01-afb9f42e5bd6
title: Atributos de sessão de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a58c0ac1f6ccd3132bb83324a4abec333a079d7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105791368"
---
# <a name="media-session-attributes"></a><span data-ttu-id="64592-103">Atributos de sessão de mídia</span><span class="sxs-lookup"><span data-stu-id="64592-103">Media Session Attributes</span></span>

<span data-ttu-id="64592-104">Os atributos a seguir são usados para configurar a sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="64592-104">The following attributes are used to configure the Media Session.</span></span>



| <span data-ttu-id="64592-105">Atributo</span><span class="sxs-lookup"><span data-stu-id="64592-105">Attribute</span></span>                                                                                            | <span data-ttu-id="64592-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="64592-106">Description</span></span>                                                                                                 |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="64592-107">**\_Gerenciador de \_ proteção de conteúdo de sessão MF \_ \_**</span><span class="sxs-lookup"><span data-stu-id="64592-107">**MF\_SESSION\_CONTENT\_PROTECTION\_MANAGER**</span></span>](mf-session-content-protection-manager-attribute.md) | <span data-ttu-id="64592-108">Fornece uma interface de retorno de chamada para que o aplicativo receba um objeto de habilitador de conteúdo da sessão do PMP.</span><span class="sxs-lookup"><span data-stu-id="64592-108">Provides a callback interface for the application to receive a content enabler object from the PMP session.</span></span> |
| [<span data-ttu-id="64592-109">**\_ \_ tempo global da sessão MF \_**</span><span class="sxs-lookup"><span data-stu-id="64592-109">**MF\_SESSION\_GLOBAL\_TIME**</span></span>](mf-session-global-time-attribute.md)                                | <span data-ttu-id="64592-110">Especifica se as topologias terão uma hora de início e de parada global.</span><span class="sxs-lookup"><span data-stu-id="64592-110">Specifies whether topologies will have a global start and stop time.</span></span>                                        |
| [<span data-ttu-id="64592-111">**\_Gerenciador de \_ qualidade de sessão MF \_**</span><span class="sxs-lookup"><span data-stu-id="64592-111">**MF\_SESSION\_QUALITY\_MANAGER**</span></span>](mf-session-quality-manager-attribute.md)                        | <span data-ttu-id="64592-112">Contém o CLSID de um Gerenciador de qualidade para a sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="64592-112">Contains the CLSID of a quality manager for the Media Session.</span></span>                                              |
| [<span data-ttu-id="64592-113">**\_modo de \_ \_ origem remoto da sessão \_ MF**</span><span class="sxs-lookup"><span data-stu-id="64592-113">**MF\_SESSION\_REMOTE\_SOURCE\_MODE**</span></span>](mf-session-remote-source-mode-attribute.md)                 | <span data-ttu-id="64592-114">Especifica que a origem da mídia está sendo executada em um processo remoto.</span><span class="sxs-lookup"><span data-stu-id="64592-114">Specifies that the media source is running in a remote process.</span></span>                                             |
| [<span data-ttu-id="64592-115">**\_ \_ contexto do servidor de sessão MF \_**</span><span class="sxs-lookup"><span data-stu-id="64592-115">**MF\_SESSION\_SERVER\_CONTEXT**</span></span>](mf-session-server-context-attribute.md)                          | <span data-ttu-id="64592-116">Permite que duas instâncias da sessão de mídia compartilhem o mesmo processo de PMP.</span><span class="sxs-lookup"><span data-stu-id="64592-116">Enables two instances of the Media Session to share the same PMP process.</span></span>                                   |
| [<span data-ttu-id="64592-117">**\_TOPOLOADER da sessão MF \_**</span><span class="sxs-lookup"><span data-stu-id="64592-117">**MF\_SESSION\_TOPOLOADER**</span></span>](mf-session-topoloader-attribute.md)                                   | <span data-ttu-id="64592-118">Contém o CLSID de um carregador de topologia para a sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="64592-118">Contains the CLSID of a topology loader for the Media Session.</span></span>                                              |



 

## <a name="related-topics"></a><span data-ttu-id="64592-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="64592-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64592-120">**IMFMediaSession**</span><span class="sxs-lookup"><span data-stu-id="64592-120">**IMFMediaSession**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession)
</dt> <dt>

[<span data-ttu-id="64592-121">Atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="64592-121">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 



