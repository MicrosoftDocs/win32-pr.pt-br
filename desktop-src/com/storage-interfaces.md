---
title: Interfaces de armazenamento
description: Interfaces de armazenamento
ms.assetid: bce0fd46-eeba-4a14-be1f-63d16885c28d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab06d8d0920ca7b29619df2173aaa0897c6eef6e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104499165"
---
# <a name="storage-interfaces"></a><span data-ttu-id="babe0-103">Interfaces de armazenamento</span><span class="sxs-lookup"><span data-stu-id="babe0-103">Storage Interfaces</span></span>

<span data-ttu-id="babe0-104">Os contêineres de controle devem ser capazes de dar suporte a controles que implementam [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream)ou [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit).</span><span class="sxs-lookup"><span data-stu-id="babe0-104">Control containers must be able to support controls that implement [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream), or [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit).</span></span> <span data-ttu-id="babe0-105">Opcionalmente, um contêiner pode dar suporte a qualquer outra interface de persistência, como [**IPersistMemory**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85)), [**IPersistPropertyBag**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768205(v=vs.85))e [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)) para esses controles que fornecem suporte.</span><span class="sxs-lookup"><span data-stu-id="babe0-105">Optionally, a container can support any other persistence interfaces such as [**IPersistMemory**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85)), [**IPersistPropertyBag**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768205(v=vs.85)), and [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)) for those controls that provide support.</span></span>

<span data-ttu-id="babe0-106">Depois que um contêiner de controle ActiveX tiver escolhido e inicializado uma interface de armazenamento para usar ([**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream), [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), etc.), essa interface de armazenamento permanecerá na interface de armazenamento primária durante o tempo de vida do controle, ou seja, o controle permanecerá em posse do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="babe0-106">Once an ActiveX control container has chosen and initialized a storage interface to use ([**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream), [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), etc), that storage interface will remain the primary storage interface for the lifetime of the control, i.e. the control will remain in possession of the storage.</span></span> <span data-ttu-id="babe0-107">Isso não impede que o contêiner seja salvo em outras interfaces de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="babe0-107">This does not preclude the container from saving to other storage interfaces.</span></span>

<span data-ttu-id="babe0-108">Os contêineres de controle ActiveX não precisam dar suporte a um mecanismo salvar como texto, portanto, usar [**IPersistPropertyBag**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768205(v=vs.85)) e a interface [**IPropertyBag**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)) associada do lado do contêiner são opcionais.</span><span class="sxs-lookup"><span data-stu-id="babe0-108">ActiveX control containers do not need to support a save as text mechanism, thus using [**IPersistPropertyBag**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768205(v=vs.85)) and the associated container-side interface [**IPropertyBag**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)) are optional.</span></span>

## <a name="related-topics"></a><span data-ttu-id="babe0-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="babe0-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="babe0-110">Contêineres</span><span class="sxs-lookup"><span data-stu-id="babe0-110">Containers</span></span>](containers.md)
</dt> </dl>

 

 