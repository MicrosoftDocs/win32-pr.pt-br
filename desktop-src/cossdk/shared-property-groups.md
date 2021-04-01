---
description: Para evitar colisões de nomes entre as propriedades criadas por objetos diferentes, o SPM (Shared Property Manager) usa grupos de propriedades compartilhadas.
ms.assetid: f73d631e-2552-4358-903a-739e2df3657d
title: Grupos de propriedades compartilhadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 776dafe5c7e9752ce3ed1c88b01fd909b4b145de
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2021
ms.locfileid: "103663693"
---
# <a name="shared-property-groups"></a>Grupos de propriedades compartilhadas

Para evitar colisões de nomes entre as propriedades criadas por objetos diferentes, o SPM (Shared Property Manager) usa grupos de propriedades compartilhadas. Um grupo de propriedades compartilhado é simplesmente um namespace para um conjunto de propriedades compartilhadas. Cada propriedade dentro de um grupo de propriedades compartilhado consiste em um nome, um valor e uma posição dentro do grupo de propriedades compartilhado. O nome ou a posição pode ser usado para recuperar o valor da propriedade. Você pode acessar e criar grupos de propriedades compartilhadas por meio do Gerenciador do grupo de propriedades compartilhado.

O modelo de objeto SPM é mostrado na ilustração a seguir.

![Diagrama que mostra o modelo de objeto SPM: ISharedPropertyGroupManager, ISharedPropertyGroup, para ISharedProperty.](images/1df31cd9-2fc4-48d3-ae68-cae38afb75a6.png)

A seguir estão as interfaces do Gerenciador de propriedades compartilhado:

-   [**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager) é usado para criar grupos de propriedades compartilhadas e para obter acesso a grupos de propriedades compartilhadas existentes. Você pode acessar a interface **ISharedPropertyGroupManager** criando uma instância do objeto [**SharedPropertyGroupManager**](sharedpropertygroupmanager.md) usando [**IObjectContext:: CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance) ou [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).

-   [**ISharedPropertyGroup**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup) é usado para criar e acessar as propriedades compartilhadas em um grupo de propriedades compartilhado. Você pode acessar a interface **ISharedPropertyGroup** criando um objeto [**SharedPropertyGroup**](sharedpropertygroup.md) com o método [**ISharedPropertyGroupManager:: CreateProperty**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroupmanager-createpropertygroup) . Assim como ocorre com qualquer objeto COM, você deve liberar um objeto **SharedPropertyGroup** quando terminar de usá-lo.

-   [**ISharedProperty**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedproperty) é usado para definir ou recuperar o valor de uma propriedade compartilhada. Uma propriedade compartilhada pode conter qualquer tipo de dados que possa ser representado por uma variante. Você pode acessar a interface **ISharedProperty** criando um objeto [**SharedProperty**](sharedproperty.md) com o método [**ISharedPropertyGroup:: CreateProperty**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createproperty) ou o método [**ISharedPropertyGroup:: CreatePropertyByPosition**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createpropertybyposition) . Um objeto **SharedProperty** pode ser criado ou acessado somente de dentro de um objeto [**SharedPropertyGroup**](sharedpropertygroup.md) . Novamente, você deve liberar um objeto **SharedProperty** quando terminar de usá-lo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gerenciador de Propriedades COM+ compartilhados](com--shared-property-manager.md)
</dt> </dl>

 

 
