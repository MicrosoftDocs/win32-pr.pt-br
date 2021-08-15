---
title: Método IWMDRMLicenseQueryActionAllowed (Wmdrmsdk.h)
description: O método QueryActionAllowed executa uma consulta no armazenamento de licenças local para recuperar o status da licença para uma ou mais ações drm que se aplicam a uma ID de chave especificada.
ms.assetid: 814c2850-c036-4c44-a64e-861e88f16fb1
keywords:
- Formato de mídia do windows do método QueryActionAllowed
- Formato de mídia do windows do método QueryActionAllowed, interface IWMDRMLicenseQuery
- Formato de mídia da interface IWMDRMLicenseQuery , Método QueryActionAllowed
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
ms.openlocfilehash: 9f6974a04f92852ef9e56b473126eb8e0cc2d92a9bdcf5192e10abe800978bcd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117846870"
---
# <a name="iwmdrmlicensequeryqueryactionallowed-method"></a>Método IWMDRMLicenseQuery::QueryActionAllowed

O **método QueryActionAllowed** executa uma consulta no armazenamento de licenças local para recuperar o status da licença para uma ou mais ações drm que se aplicam a uma ID de chave especificada.

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

*bstrKID* \[ Em\]
</dt> <dd>

ID da chave para a qual consultar. Somente as licenças que se aplicam a essa ID de chave serão avaliadas.

</dd> <dt>

*bstrMinReqIndivVersion* \[ Em\]
</dt> <dd>

A versão de segurança mínima especificada no título do arquivo ASF. Esse parâmetro é opcional. Passe **NULL** para executar a consulta sem essas informações.

</dd> <dt>

*cActionsToQuery* \[ Em\]
</dt> <dd>

O número de ações para as quais consultar. Esse valor deve ser definido como o número de elementos nas matrizes passadas para os parâmetros *rgbstrActionsToQuery* e *rgdwQueryResult.*

</dd> <dt>

*rgbstrActionsToQuery \[ \]* \[em\]
</dt> <dd>

Matriz de um ou mais direitos para os quais consultar. Essa matriz deve conter tantos elementos quanto especificado por *cActionsToQuery.* Cada elemento deve ser definido como uma das seguintes constantes:



| Constante                                         | Descrição                                                                      |
|--------------------------------------------------|----------------------------------------------------------------------------------|
| g \_ wszWMDRM \_ ActionAllowed \_ Playback             | Inclua para consultar o direito de reproduzir o conteúdo.                              |
| g \_ wszWMDRM \_ ActionAllowed \_ Copy                 | Inclua para consultar o direito de copiar o conteúdo para dispositivos externos ou mídia. |
| g \_ wszWMDRM \_ ActionAllowed \_ Playlist Lean         | Inclua para consultar o direito de copiar o conteúdo para CD como parte de uma playlist.  |
| g \_ wszWMDRM \_ ActionAllowed \_ CreateThumbnailImage | Inclua para consultar o direito de criar uma imagem em miniatura do conteúdo.     |
| g \_ wszWMDRM \_ ActionAllowed \_ CopyToCD             | Inclua para consultar o direito de copiar o conteúdo para CD.                        |



 

</dd> <dt>

*rgdwQueryResult \[ \]* \[out\]
</dt> <dd>

Matriz de uma ou mais variáveis DWORD que recebem os resultados da consulta para os direitos especificados por *rgbstrActionsToQuery*. Se uma ação for permitida, o elemento correspondente será definido como zero. Se uma ação não for permitida, o elemento será definido como um ou mais valores da enumeração [**DRM \_ ACTION ALLOWED \_ \_ QUERY \_ RESULTS**](drm-action-allowed-query-results.md) combinados usando a operação OR bit a bit. Essa matriz deve conter tantos elementos quanto especificado por *cActionsToQuery.*

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT.** Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Ao consultar direitos de reprodução e cópia, você obterá resultados mais precisos definindo primeiro parâmetros ambientais. Use o [**método SetActionAllowedQueryParams**](iwmdrmlicensequery-setactionallowedqueryparams.md) para definir os parâmetros ambientais. Os resultados das consultas para o direito de gravar não são afetados pelos parâmetros ambientais; você pode usar os padrões com segurança.

Os resultados retornados pelo **método QueryActionAllowed** são agregados de zero ou mais licenças no armazenamento de licenças local. O método pode não pesquisar todas as licenças que se aplicam à ID da Chave se encontrar um resultado habilitado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IWMDRMLicenseQuery Interface**](iwmdrmlicensequery.md)
</dt> <dt>

[**Consultando informações de direitos simples**](querying-for-simple-rights-information.md)
</dt> </dl>

 

 





