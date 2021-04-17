---
description: Registro e carregamento do provedor de cópia de sombra
ms.assetid: f9bb72ce-9a2b-43cd-9697-1f6598a46e3e
title: Registro e carregamento do provedor de cópia de sombra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 725613ff37450075c964b3c66fce3ffba1a70529
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296649"
---
# <a name="shadow-copy-provider-registration-and-loading"></a><span data-ttu-id="55a66-103">Registro e carregamento do provedor de cópia de sombra</span><span class="sxs-lookup"><span data-stu-id="55a66-103">Shadow Copy Provider Registration and Loading</span></span>

## <a name="provider-registration"></a><span data-ttu-id="55a66-104">Registro do provedor</span><span class="sxs-lookup"><span data-stu-id="55a66-104">Provider Registration</span></span>

<span data-ttu-id="55a66-105">Somente os provedores de chamadas do VSS.</span><span class="sxs-lookup"><span data-stu-id="55a66-105">Only VSS calls providers.</span></span> <span data-ttu-id="55a66-106">O provedor registra para chamadas invocando [**IVssAdmin:: RegisterProvider**](/windows/desktop/api/VsAdmin/nf-vsadmin-ivssadmin-registerprovider), passando o **\_ \_ hardware de Prov do VSS** para o parâmetro *eProviderType* .</span><span class="sxs-lookup"><span data-stu-id="55a66-106">The provider registers for calls by invoking [**IVssAdmin::RegisterProvider**](/windows/desktop/api/VsAdmin/nf-vsadmin-ivssadmin-registerprovider), passing **VSS\_PROV\_HARDWARE** for the *eProviderType* parameter.</span></span> <span data-ttu-id="55a66-107">Depois de registrado, o provedor estará envolvido no gerenciamento de cópia de sombra até o cancelamento do registro usando [**IVssAdmin:: UnregisterProvider**](/windows/desktop/api/VsAdmin/nf-vsadmin-ivssadmin-unregisterprovider).</span><span class="sxs-lookup"><span data-stu-id="55a66-107">Once registered, the provider will be involved in shadow copy management until unregistering using [**IVssAdmin::UnregisterProvider**](/windows/desktop/api/VsAdmin/nf-vsadmin-ivssadmin-unregisterprovider).</span></span>

## <a name="provider-loading-and-unloading"></a><span data-ttu-id="55a66-108">Carregamento e descarregamento do provedor</span><span class="sxs-lookup"><span data-stu-id="55a66-108">Provider Loading and Unloading</span></span>

<span data-ttu-id="55a66-109">Os provedores podem ser carregados e descarregados com frequência.</span><span class="sxs-lookup"><span data-stu-id="55a66-109">Providers can be frequently loaded and unloaded.</span></span> <span data-ttu-id="55a66-110">Os provedores podem implementar [**IVssProviderNotifications**](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidernotifications) para determinar quando o VSS está carregando ou descarregando o provedor.</span><span class="sxs-lookup"><span data-stu-id="55a66-110">Providers can implement [**IVssProviderNotifications**](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidernotifications) to determine when VSS is loading or unloading the provider.</span></span>

 

 



