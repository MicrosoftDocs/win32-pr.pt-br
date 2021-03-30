---
title: Interface IWMDRMLicenseQuery
description: A interface IWMDRMLicenseQuery permite que os aplicativos consultem os direitos e o estado da licença para um arquivo protegido.
ms.assetid: 4ec8ff9f-0acb-4389-8995-65f24736491b
keywords:
- Formato de mídia do Windows da interface IWMDRMLicenseQuery
- Formato de mídia do Windows da interface IWMDRMLicenseQuery, descrito
topic_type:
- apiref
api_name:
- IWMDRMLicenseQuery
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6463f405bf50d4d4ecb037dc542e3af0e5b7df46
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641453"
---
# <a name="iwmdrmlicensequery-interface"></a>Interface IWMDRMLicenseQuery

A interface **IWMDRMLicenseQuery** permite que os aplicativos consultem os direitos e o estado da licença para um arquivo protegido. Essa interface usa a ID da chave para executar consultas no repositório de licenças local.

Para obter uma instância dessa interface, chame [**IWMDRMProvider:: CreateObject**](iwmdrmprovider-createobject.md). Passe **\_ IWMDRMLicenseQuery IID** como o parâmetro *riid* .

## <a name="members"></a>Membros

A interface **IWMDRMLicenseQuery** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IWMDRMLicenseQuery** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IWMDRMLicenseQuery** tem esses métodos.



| Método                                                                                | Descrição                                                                                      |
|:--------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md)                   | Consulta o repositório de licenças local para obter permissões para executar ações por ID de chave.<br/>         |
| [**QueryLicenseState**](iwmdrmlicensequery-querylicensestate.md)                     | Consulta o repositório de licenças local para dados de estado da licença por ID de chave e direitos específicos.<br/> |
| [**SetActionAllowedQueryParams**](iwmdrmlicensequery-setactionallowedqueryparams.md) | Define os parâmetros ambientais para melhorar a precisão das consultas de licença.<br/>             |



 

## <a name="remarks"></a>Comentários

Os métodos de **IWMDRMLicenseQuery** não fornecem informações sobre licenças individuais. Em vez disso, os dados de licença são agregados pelo subsistema DRM antes que os resultados da consulta sejam retornados.

## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Interfaces**](drm-interfaces.md)
</dt> </dl>

 

