---
title: Método IWMDRMLicenseQuery QueryActionAllowed (wmdrmsdk. h)
description: O método QueryActionAllowed executa uma consulta no repositório de licenças local para recuperar o status da licença para uma ou mais ações de DRM que se aplicam a uma ID de chave especificada.
ms.assetid: 814c2850-c036-4c44-a64e-861e88f16fb1
keywords:
- Formato de mídia do Windows do método QueryActionAllowed
- Método QueryActionAllowed Windows Media Format, interface IWMDRMLicenseQuery
- Formato de mídia do Windows de interface IWMDRMLicenseQuery, método QueryActionAllowed
topic_type:
- apiref
api_name:
- IWMDRMLicenseQuery.QueryActionAllowed
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6564062fc9f76a840b37f6e134e960480d67a2ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105775573"
---
# <a name="iwmdrmlicensequeryqueryactionallowed-method"></a>Método IWMDRMLicenseQuery:: QueryActionAllowed

O método **QueryActionAllowed** executa uma consulta no repositório de licenças local para recuperar o status da licença para uma ou mais ações de DRM que se aplicam a uma ID de chave especificada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT QueryActionAllowed(
  [in]  BSTR  bstrKID,
  [in]  BSTR  bstrMinReqIndivVersion,
  [in]  DWORD cActionsToQuery,
  [in]  BSTR  rgbstrActionsToQuery[],
  [out] DWORD rgdwQueryResult[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrKID* \[ no\]
</dt> <dd>

ID de chave para consulta. Somente as licenças que se aplicam a essa ID de chave serão avaliadas.

</dd> <dt>

*bstrMinReqIndivVersion* \[ no\]
</dt> <dd>

A versão de segurança mínima especificada no cabeçalho do arquivo ASF. Esse parâmetro é opcional. Passe **NULL** para executar a consulta sem essas informações.

</dd> <dt>

*cActionsToQuery* \[ no\]
</dt> <dd>

O número de ações para consulta. Esse valor deve ser definido como o número de elementos nas matrizes passadas para os parâmetros *rgbstrActionsToQuery* e *rgdwQueryResult* .

</dd> <dt>

*\[ rgbstrActionsToQuery \]* \[em\]
</dt> <dd>

Matriz de um ou mais direitos para consulta. Essa matriz deve conter tantos elementos quantos forem especificados por *cActionsToQuery*. Cada elemento deve ser definido como uma das seguintes constantes:



| Constante                                         | Descrição                                                                      |
|--------------------------------------------------|----------------------------------------------------------------------------------|
| reprodução do g \_ wszWMDRM \_ ActionAllowed \_             | Inclua para consultar o direito de reproduzir o conteúdo.                              |
| cópia do g \_ wszWMDRM \_ ActionAllowed \_                 | Inclua para consultar o direito de copiar o conteúdo para dispositivos externos ou mídia. |
| g \_ wszWMDRM \_ ActionAllowed \_ PlaylistBurn         | Inclua para consultar o direito de copiar o conteúdo para o CD como parte de uma lista de reprodução.  |
| g \_ wszWMDRM \_ ActionAllowed \_ CreateThumbnailImage | Inclua para consultar o direito de criar uma imagem em miniatura a partir do conteúdo.     |
| g \_ wszWMDRM \_ ActionAllowed \_ CopyToCD             | Inclua para consultar o direito de copiar o conteúdo para o CD.                        |



 

</dd> <dt>

*\[ rgdwQueryResult \]* \[out\]
</dt> <dd>

Matriz de uma ou mais variáveis DWORD que recebem os resultados da consulta para os direitos especificados por *rgbstrActionsToQuery*. Se uma ação for permitida, o elemento correspondente será definido como zero. Se uma ação não for permitida, o elemento será definido como um ou mais valores da enumeração [**de \_ \_ resultados de \_ consulta \_ permitida da ação DRM**](drm-action-allowed-query-results.md) combinadas com o uso da operação OR. Essa matriz deve conter tantos elementos quantos forem especificados por *cActionsToQuery*.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Ao consultar direitos de reprodução e cópia, você obterá resultados mais precisos primeiro definindo parâmetros ambientais. Use o método [**SetActionAllowedQueryParams**](iwmdrmlicensequery-setactionallowedqueryparams.md) para definir os parâmetros ambientais. Os resultados das consultas para o direito de gravação não são afetados pelos parâmetros ambientais; Você pode usar os padrões com segurança.

Os resultados retornados pelo método **QueryActionAllowed** são agregados de zero ou mais licenças no repositório de licenças local. O método pode não Pesquisar todas as licenças que se aplicam à ID da chave se encontrar um resultado habilitado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMDRMLicenseQuery**](iwmdrmlicensequery.md)
</dt> <dt>

[**Consultando informações de direitos simples**](querying-for-simple-rights-information.md)
</dt> </dl>

 

 





