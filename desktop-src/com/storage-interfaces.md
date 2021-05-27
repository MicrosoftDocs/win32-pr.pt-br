---
title: Interfaces de armazenamento
description: Interfaces de armazenamento
ms.assetid: bce0fd46-eeba-4a14-be1f-63d16885c28d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97ad0cc646d45ca0b77a70ecaf47d28eadb4d136
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549261"
---
# <a name="storage-interfaces"></a><span data-ttu-id="b15ba-103">Interfaces de armazenamento</span><span class="sxs-lookup"><span data-stu-id="b15ba-103">Storage Interfaces</span></span>

<span data-ttu-id="b15ba-104">Os contêineres de controle devem ser capazes de dar suporte a controles que implementam [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream)ou [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit).</span><span class="sxs-lookup"><span data-stu-id="b15ba-104">Control containers must be able to support controls that implement [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream), or [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit).</span></span> <span data-ttu-id="b15ba-105">Opcionalmente, um contêiner pode dar suporte a qualquer outra interface de persistência, como [**IPersistMemory**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85)), [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag)e [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)) para esses controles que fornecem suporte.</span><span class="sxs-lookup"><span data-stu-id="b15ba-105">Optionally, a container can support any other persistence interfaces such as [**IPersistMemory**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85)), [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag), and [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)) for those controls that provide support.</span></span>

<span data-ttu-id="b15ba-106">Depois que um contêiner de controle ActiveX tiver escolhido e inicializado uma interface de armazenamento para usar ([**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream), [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), etc.), essa interface de armazenamento permanecerá na interface de armazenamento primária durante o tempo de vida do controle, ou seja, o controle permanecerá em posse do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b15ba-106">Once an ActiveX control container has chosen and initialized a storage interface to use ([**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream), [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), etc), that storage interface will remain the primary storage interface for the lifetime of the control, i.e. the control will remain in possession of the storage.</span></span> <span data-ttu-id="b15ba-107">Isso não impede que o contêiner seja salvo em outras interfaces de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b15ba-107">This does not preclude the container from saving to other storage interfaces.</span></span>

<span data-ttu-id="b15ba-108">Os contêineres de controle ActiveX não precisam dar suporte a um mecanismo salvar como texto, portanto, usar [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag) e a interface [**IPropertyBag**](/windows/win32/api/oaidl/nn-oaidl-ipropertybag) associada do lado do contêiner são opcionais.</span><span class="sxs-lookup"><span data-stu-id="b15ba-108">ActiveX control containers do not need to support a save as text mechanism, thus using [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag) and the associated container-side interface [**IPropertyBag**](/windows/win32/api/oaidl/nn-oaidl-ipropertybag) are optional.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b15ba-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b15ba-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b15ba-110">Contêineres</span><span class="sxs-lookup"><span data-stu-id="b15ba-110">Containers</span></span>](containers.md)
</dt> </dl>

 

 