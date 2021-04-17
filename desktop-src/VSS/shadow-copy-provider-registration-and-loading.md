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
# <a name="shadow-copy-provider-registration-and-loading"></a>Registro e carregamento do provedor de cópia de sombra

## <a name="provider-registration"></a>Registro do provedor

Somente os provedores de chamadas do VSS. O provedor registra para chamadas invocando [**IVssAdmin:: RegisterProvider**](/windows/desktop/api/VsAdmin/nf-vsadmin-ivssadmin-registerprovider), passando o **\_ \_ hardware de Prov do VSS** para o parâmetro *eProviderType* . Depois de registrado, o provedor estará envolvido no gerenciamento de cópia de sombra até o cancelamento do registro usando [**IVssAdmin:: UnregisterProvider**](/windows/desktop/api/VsAdmin/nf-vsadmin-ivssadmin-unregisterprovider).

## <a name="provider-loading-and-unloading"></a>Carregamento e descarregamento do provedor

Os provedores podem ser carregados e descarregados com frequência. Os provedores podem implementar [**IVssProviderNotifications**](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidernotifications) para determinar quando o VSS está carregando ou descarregando o provedor.

 

 



