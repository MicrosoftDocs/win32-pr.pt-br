---
title: Propriedades de ambiente para controles
description: Propriedades de ambiente para controles
ms.assetid: 19aa3bc2-1605-43e1-acf4-ab782d012539
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e166a7186021b53798150968c9998fed243de00
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364121"
---
# <a name="ambient-properties-for-controls"></a><span data-ttu-id="a1c33-103">Propriedades de ambiente para controles</span><span class="sxs-lookup"><span data-stu-id="a1c33-103">Ambient Properties for Controls</span></span>

<span data-ttu-id="a1c33-104">Se um controle oferecer suporte a todas as propriedades de ambiente, ele deverá pelo menos respeitar os valores das seguintes propriedades de ambiente nas condições indicadas na tabela a seguir usando os DISPIDs padrão.</span><span class="sxs-lookup"><span data-stu-id="a1c33-104">If a control supports any ambient properties at all, it must at least respect the values of the following ambient properties under the conditions stated in the following table using the standard dispids.</span></span>



| <span data-ttu-id="a1c33-105">Propriedade de ambiente</span><span class="sxs-lookup"><span data-stu-id="a1c33-105">Ambient Property</span></span>            | <span data-ttu-id="a1c33-106">DISPID</span><span class="sxs-lookup"><span data-stu-id="a1c33-106">Dispid</span></span>          | <span data-ttu-id="a1c33-107">Comentário/condições para uso</span><span class="sxs-lookup"><span data-stu-id="a1c33-107">Comment/Conditions for Use</span></span>                                                                                                                                                                                                                                                                |
|-----------------------------|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1c33-108">LocaleID</span><span class="sxs-lookup"><span data-stu-id="a1c33-108">LocaleID</span></span><br/>         | <span data-ttu-id="a1c33-109">-705</span><span class="sxs-lookup"><span data-stu-id="a1c33-109">-705</span></span><br/> | <span data-ttu-id="a1c33-110">Se a localidade for significativa para o controle, por exemplo, para saída de texto</span><span class="sxs-lookup"><span data-stu-id="a1c33-110">If Locale is significant to the control, e.g. for text output</span></span><br/>                                                                                                                                                                                                                  |
| <span data-ttu-id="a1c33-111">Modo</span><span class="sxs-lookup"><span data-stu-id="a1c33-111">UserMode</span></span> <br/>        | <span data-ttu-id="a1c33-112">-709</span><span class="sxs-lookup"><span data-stu-id="a1c33-112">-709</span></span><br/> | <span data-ttu-id="a1c33-113">Se o controle se comporta de forma diferente no modo de usuário (Design) e no modo de execução</span><span class="sxs-lookup"><span data-stu-id="a1c33-113">If the control behaves differently in user (design) mode and run mode</span></span><br/>                                                                                                                                                                                                          |
| <span data-ttu-id="a1c33-114">UIDead</span><span class="sxs-lookup"><span data-stu-id="a1c33-114">UIDead</span></span><br/>           | <span data-ttu-id="a1c33-115">-710</span><span class="sxs-lookup"><span data-stu-id="a1c33-115">-710</span></span><br/> | <span data-ttu-id="a1c33-116">Se o controle reage a eventos de interface do usuário, ele deve honrar essa propriedade de ambiente</span><span class="sxs-lookup"><span data-stu-id="a1c33-116">If the control reacts to UI events, then it should honor this ambient property</span></span><br/>                                                                                                                                                                                                 |
| <span data-ttu-id="a1c33-117">ShowGrabHandles</span><span class="sxs-lookup"><span data-stu-id="a1c33-117">ShowGrabHandles</span></span><br/>  | <span data-ttu-id="a1c33-118">-711</span><span class="sxs-lookup"><span data-stu-id="a1c33-118">-711</span></span><br/> | <span data-ttu-id="a1c33-119">Se o controle suportar o redimensionamento in-loco de si mesmo</span><span class="sxs-lookup"><span data-stu-id="a1c33-119">If the control support in-place resizing of itself</span></span><br/>                                                                                                                                                                                                                             |
| <span data-ttu-id="a1c33-120">Deshachurando</span><span class="sxs-lookup"><span data-stu-id="a1c33-120">ShowHatching</span></span><br/>     | <span data-ttu-id="a1c33-121">-712</span><span class="sxs-lookup"><span data-stu-id="a1c33-121">-712</span></span><br/> | <span data-ttu-id="a1c33-122">Se o controle oferecer suporte à ativação in-loco e à ativação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="a1c33-122">If the control support in-place activation and UI activation</span></span><br/>                                                                                                                                                                                                                   |
| <span data-ttu-id="a1c33-123">DisplayAsDefault</span><span class="sxs-lookup"><span data-stu-id="a1c33-123">DisplayAsDefault</span></span><br/> | <span data-ttu-id="a1c33-124">-713</span><span class="sxs-lookup"><span data-stu-id="a1c33-124">-713</span></span><br/> | <span data-ttu-id="a1c33-125">Somente se o controle estiver marcado como OLEMISC \_ ACTSLIKEBUTTON (o que significa que o suporte para mnemônicos de teclado é fornecido, portanto, [**IOleControl:: GetControlInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-getcontrolinfo) e [**IOleControl:: onmnemônico**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onmnemonic) deve ser implementado).</span><span class="sxs-lookup"><span data-stu-id="a1c33-125">Only if the control is marked OLEMISC\_ACTSLIKEBUTTON (which means that support for keyboard mnemonics is provided, thus [**IOleControl::GetControlInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-getcontrolinfo) and [**IOleControl::OnMnemonic**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onmnemonic) must be implemented).</span></span><br/> |



 

<span data-ttu-id="a1c33-126">Conforme descrito anteriormente, o uso de ambientes requer [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) (para [**OnAmbientPropertyChange**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onambientpropertychange) como um mínimo), bem como [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject) (para [**SetClientSite**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-setclientsite) e [**GetClientSite**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getclientsite)).</span><span class="sxs-lookup"><span data-stu-id="a1c33-126">As described previously, use of ambients requires both [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) (for [**OnAmbientPropertyChange**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onambientpropertychange) as a minimum) as well as [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject) (for [**SetClientSite**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-setclientsite) and [**GetClientSite**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getclientsite)).</span></span>

<span data-ttu-id="a1c33-127">O OLEMISC \_ SETCLIENTSITEFIRST bit pode não ser necessariamente suportado por um contêiner.</span><span class="sxs-lookup"><span data-stu-id="a1c33-127">The OLEMISC\_SETCLIENTSITEFIRST bit may not necessarily be supported by a container.</span></span> <span data-ttu-id="a1c33-128">Nessas circunstâncias, um controle deve recorrer aos valores padrão para as propriedades de ambiente que ele requer.</span><span class="sxs-lookup"><span data-stu-id="a1c33-128">In these circumstances, a control must resort to default values for the ambient properties that it requires.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a1c33-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a1c33-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1c33-130">Controles</span><span class="sxs-lookup"><span data-stu-id="a1c33-130">Controls</span></span>](controls.md)
</dt> </dl>

 

 





