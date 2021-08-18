---
description: Registro e carregamento do provedor de cópia de sombra
ms.assetid: f9bb72ce-9a2b-43cd-9697-1f6598a46e3e
title: Registro e carregamento do provedor de cópia de sombra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbb239303884314375ec865e3862d6a65af7de27bd7351a74e92604d06876bb2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998106"
---
# <a name="shadow-copy-provider-registration-and-loading"></a>Registro e carregamento do provedor de cópia de sombra

## <a name="provider-registration"></a>Registro do provedor

Somente o VSS chama provedores. O provedor se registra para chamadas invocando [**IVssAdmin::RegisterProvider**](/windows/desktop/api/VsAdmin/nf-vsadmin-ivssadmin-registerprovider), passando **o HARDWARE DO VSS \_ PROV \_** para o parâmetro *eProviderType.* Depois de registrado, o provedor estará envolvido no gerenciamento de cópia de sombra até o registro ser feito usando [**IVssAdmin::UnregisterProvider**](/windows/desktop/api/VsAdmin/nf-vsadmin-ivssadmin-unregisterprovider).

## <a name="provider-loading-and-unloading"></a>Carregamento e descarregamento do provedor

Os provedores podem ser carregados e descarregados com frequência. Os provedores podem implementar [**IVssProviderNotifications**](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidernotifications) para determinar quando o VSS está carregando ou descarregando o provedor.

 

 



