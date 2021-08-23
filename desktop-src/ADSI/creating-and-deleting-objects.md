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
ms.openlocfilehash: 36bf2e351fb9bae919e8c40b0682b456b793f2e4419a66c64242791fad1d6cae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023644"
---
# <a name="creating-and-deleting-objects"></a>Criando e excluindo objetos

Com a ADSI, os objetos são criados e excluídos usando a interface [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) [**ou IDirectoryObject.**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)

## <a name="creating-an-object-with-iadscontainer"></a>Criando um objeto com IADsContainer

**Para criar um objeto com a interface IADsContainer**

1.  A bind ao contêiner que conterá o objeto a ser criado e obterá a interface [**IADsContainer.**](/windows/desktop/api/Iads/nn-iads-iadscontainer)
2.  Use o [**método IADsContainer.Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) para criar um novo objeto no contêiner.
3.  De definir os valores para todos os atributos necessários para o objeto usando o [**método IADs.Put**](/windows/desktop/api/Iads/nf-iads-iads-put) ou [**IADs.PutEx.**](/windows/desktop/api/Iads/nf-iads-iads-putex) Os atributos necessários para criar um objeto dependerão do serviço de diretório e do tipo de objeto criado. Para obter mais informações sobre como criar objetos do Active Directory, consulte [Criando e excluindo objetos do Active Directory.](/windows/desktop/AD/creating-and-deleting-objects-in-active-directory-domain-services)
4.  De definir os valores para todos os atributos opcionais desejados para o objeto usando o [**método IADs.Put**](/windows/desktop/api/Iads/nf-iads-iads-put) ou [**IADs.PutEx.**](/windows/desktop/api/Iads/nf-iads-iads-putex)
5.  Chame o [**método IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) para fazer commit do objeto e de seus atributos. O novo objeto não é realmente criado no serviço de diretório subjacente até que o método **IADs.SetInfo** seja chamado para fazer commit dos atributos.

## <a name="creating-an-object-with-idirectoryobject"></a>Criando um objeto com IDirectoryObject

**Para criar um objeto com a interface IDirectoryObject**

1.  A bind ao contêiner que conterá o objeto a ser criado e obterá a interface [**IDirectoryObject.**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)
2.  Aloce uma matriz de [**estruturas ADS \_ ATTR \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) que contém uma estrutura para cada atributo a ser definido quando o objeto é criado.
3.  Preencha uma estrutura [**ADS \_ ATTR \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) para cada atributo necessário para o objeto . Os atributos necessários para criar um objeto dependerão do serviço de diretório e do tipo de objeto criado. Para obter mais informações sobre como criar objetos do Active Directory, consulte [Criando e excluindo objetos do Active Directory.](/windows/desktop/AD/creating-and-deleting-objects-in-active-directory-domain-services)
4.  Preencha uma estrutura [**ADS \_ ATTR \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) para cada atributo opcional para o objeto .
5.  Use o [**método IDirectoryObject::CreateDSObject**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-createdsobject) para criar o objeto no contêiner. Esse método também confirma o objeto para o serviço de diretório subjacente. Se a [**matriz ADS \_ ATTR \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) não contém todos os atributos necessários para o objeto, **IDirectoryObject::CreateDSObject** falhará.

## <a name="deleting-an-object"></a>Excluindo um objeto

Para excluir um objeto, use [**o método IADsContainer::D elete**](/windows/desktop/api/Iads/nf-iads-iadscontainer-delete) ou [**IDirectoryObject::D eleteDSObject.**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-deletedsobject) Esses métodos falharão se o objeto excluído contiver objetos filho. Use o [**método IADsDeleteOps::D eleteObject**](/windows/desktop/api/Iads/nf-iads-iadsdeleteops-deleteobject) para excluir um contêiner e todos os objetos filho do contêiner.

O que acontece com um objeto excluído depende do serviço de diretório subjacente. Para obter mais informações sobre como excluir objetos do Active Directory, consulte [Criando e excluindo objetos do Active Directory](/windows/desktop/AD/creating-and-deleting-objects-in-active-directory-domain-services).

 

 