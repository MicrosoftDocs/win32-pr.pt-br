---
title: Método IWMDRMLicenseQuery QueryLicenseState (wmdrmsdk. h)
description: O método QueryLicenseState consulta o repositório de licença local para obter informações de licença que se aplicam a uma ID de chave para um ou mais direitos específicos.
ms.assetid: 17f40c56-2266-4c94-9e95-a33a92ddef74
keywords:
- Formato de mídia do Windows do método QueryLicenseState
- Método QueryLicenseState Windows Media Format, interface IWMDRMLicenseQuery
- Formato de mídia do Windows de interface IWMDRMLicenseQuery, método QueryLicenseState
topic_type:
- apiref
api_name:
- IWMDRMLicenseQuery.QueryLicenseState
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e101d4ad9b5405906d05ba5e5f230326a1a3f13a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760986"
---
# <a name="iwmdrmlicensequeryquerylicensestate-method"></a>Método IWMDRMLicenseQuery:: QueryLicenseState

O método **QueryLicenseState** consulta o repositório de licença local para obter informações de licença que se aplicam a uma ID de chave para um ou mais direitos específicos.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT QueryLicenseState(
  [in]  BSTR                   bstrKID,
  [in]  DWORD                  cActionsToQuery,
  [in]  BSTR                   rgbstrActionsToQuery[],
  [out] DRM_LICENSE_STATE_DATA rgResultStateData[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrKID* \[ no\]
</dt> <dd>

ID de chave para consulta. Somente as licenças que se aplicam a essa ID de chave serão avaliadas.

</dd> <dt>

*cActionsToQuery* \[ no\]
</dt> <dd>

O número de ações para consulta. Esse valor deve ser definido como o número de elementos nas matrizes passadas para os parâmetros *rgbstrActionsToQuery* e *rgResultStateData* .

</dd> <dt>

*\[ rgbstrActionsToQuery \]* \[em\]
</dt> <dd>

Matriz de um ou mais direitos para consulta. Essa matriz deve conter tantos elementos quantos forem especificados por *cActionsToQuery*. Cada elemento deve ser definido como uma das constantes a seguir.



| Constante                                        | Descrição                                                                                                                                        |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Backup do g \_ wszWMDRM \_ licensestate \_               | Inclua para consultar os detalhes sobre o direito de fazer backup e restaurar a licença.                                                               |
| g \_ wszWMDRM \_ licensestate \_ CollaborativePlay    | Inclua para consultar os detalhes sobre o direito de compartilhar o conteúdo com um grupo de usuários como parte de um cenário de reprodução colaborativa.          |
| \_cópia de \_ licença g \_ wszWMDRM                 | Inclua para consultar os detalhes sobre o direito de copiar o conteúdo para dispositivos ou mídias externos.                                                 |
| g \_ wszWMDRM \_ licensestate \_ CopyToCD             | Inclua para consultar os detalhes sobre o direito de copiar o conteúdo para o CD.                                                                        |
| g \_ wszWMDRM \_ licensestate \_ CopyToNonSDMIDevice  | Inclua para consultar os detalhes sobre o direito de copiar o conteúdo para um dispositivo que não dá suporte à SDMI (Secure Digital Media Initiative). |
| g \_ wszWMDRM \_ licensestate \_ CopyToSDMIDevice     | Inclua para consultar os detalhes sobre o direito de copiar o conteúdo para um dispositivo que dá suporte a SDMI.                                           |
| g \_ wszWMDRM \_ licensestate \_ CreateThumbnailImage | Inclua para consultar os detalhes sobre o direito de criar uma imagem em miniatura a partir do conteúdo.                                                     |
| wszWMDRM de licença do g para \_ \_ \_ reprodução             | Inclua para consultar os detalhes sobre o direito de reproduzir o conteúdo.                                                                              |
| g \_ wszWMDRM \_ licensestate \_ PlaylistBurn         | Inclua para consultar os detalhes sobre o direito de copiar o conteúdo para o CD como parte de uma lista de reprodução.                                                  |



 

</dd> <dt>

*\[ rgResultStateData \]* \[out\]
</dt> <dd>

Matriz de uma ou mais estruturas de dados de estado de licença do DRM que recebem as informações de estado da licença que se aplicam à direita no elemento correspondente do parâmetro *rgbstrActionsToQuery* . [**\_ \_ \_**](drmdrm-license-state-data.md)

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Todas as licenças que se aplicam à ID de chave especificada serão pesquisadas e avaliadas. Os resultados são agregados, portanto, cada estrutura de dados de estado de licença do DRM pode conter informações de várias licenças. **\_ \_ \_**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMDRMLicenseQuery**](iwmdrmlicensequery.md)
</dt> </dl>

 

 





