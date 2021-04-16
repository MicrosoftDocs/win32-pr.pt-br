---
title: Criando e excluindo objetos
description: Com a ADSI, os objetos são criados e excluídos usando a interface IADsContainer ou IDirectoryObject.
ms.assetid: 4d1f7ac5-48d3-4ea9-91e4-0cd4bb2ec9f8
ms.tgt_platform: multiple
keywords:
- Criando e excluindo objetos ADSI
- ADSI, criando e excluindo objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4730c4cc6a95ad37bfd3953474d3d488fcf05abb
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104454344"
---
# <a name="creating-and-deleting-objects"></a>Criando e excluindo objetos

Com a ADSI, os objetos são criados e excluídos usando a interface [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) ou [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) .

## <a name="creating-an-object-with-iadscontainer"></a>Criando um objeto com IADsContainer

**Para criar um objeto com a interface IADsContainer**

1.  Associe ao contêiner que conterá o objeto a ser criado e obtenha a interface [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) .
2.  Use o método [**IADsContainer. Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) para criar um novo objeto no contêiner.
3.  Defina os valores para todos os atributos necessários para o objeto usando o método [**IADs. put**](/windows/desktop/api/Iads/nf-iads-iads-put) ou [**IADs. PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) . Os atributos necessários para criar um objeto dependerão do serviço de diretório e do tipo de objeto criado. Para obter mais informações sobre como criar Active Directory objetos, consulte [criando e excluindo objetos Active Directory](/windows/desktop/AD/creating-and-deleting-objects-in-active-directory-domain-services).
4.  Defina os valores para todos os atributos opcionais desejados para o objeto usando o método [**IADs. put**](/windows/desktop/api/Iads/nf-iads-iads-put) ou [**IADs. PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) .
5.  Chame o método [**IADs. setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) para confirmar o objeto e seus atributos. O novo objeto não é realmente criado no serviço de diretório subjacente até que o método **IADs. setinfo** seja chamado para confirmar os atributos.

## <a name="creating-an-object-with-idirectoryobject"></a>Criando um objeto com IDirectoryObject

**Para criar um objeto com a interface IDirectoryObject**

1.  Associe ao contêiner que conterá o objeto a ser criado e obtenha a interface [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) .
2.  Aloque uma matriz de estruturas de [**\_ \_ informações attr de anúncios**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) que contenham uma estrutura para cada atributo a ser definido quando o objeto for criado.
3.  Preencha uma estrutura [**de \_ \_ informações attr de anúncios**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) para cada atributo necessário para o objeto. Os atributos necessários para criar um objeto dependerão do serviço de diretório e do tipo de objeto criado. Para obter mais informações sobre como criar Active Directory objetos, consulte [criando e excluindo objetos Active Directory](/windows/desktop/AD/creating-and-deleting-objects-in-active-directory-domain-services).
4.  Preencha uma estrutura [**de \_ \_ informações attr de anúncios**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) para cada atributo opcional para o objeto.
5.  Use o método [**IDirectoryObject:: CreateDSObject**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-createdsobject) para criar o objeto no contêiner. Esse método também confirma o objeto para o serviço de diretório subjacente. Se a matriz de [**\_ \_ informações attr do ADS**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) não contiver todos os atributos necessários para o objeto, **IDirectoryObject:: CreateDSObject** falhará.

## <a name="deleting-an-object"></a>Excluindo um objeto

Para excluir um objeto, use o método [**IADsContainer::D xcluir**](/windows/desktop/api/Iads/nf-iads-iadscontainer-delete) ou [**IDirectoryObject::D eletedsobject**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-deletedsobject) . Esses métodos falharão se o objeto excluído contiver objetos filho. Use o método [**IADsDeleteOps::D eleteobject**](/windows/desktop/api/Iads/nf-iads-iadsdeleteops-deleteobject) para excluir um contêiner e todos os objetos filho do contêiner.

O que acontece com um objeto excluído depende do serviço de diretório subjacente. Para obter mais informações sobre como excluir objetos Active Directory, consulte [criando e excluindo objetos Active Directory](/windows/desktop/AD/creating-and-deleting-objects-in-active-directory-domain-services).

 

 