---
description: Obtém o item de pesquisa para os dados especificados. Esse método é chamado uma vez para cada URL processada pelo gatherer e recupera um ponteiro para o objeto ISearchItem.
ms.assetid: 35893bc9-8327-44f9-a9fc-7855c5c063e3
title: 'Método ISearchProtocolUI:: GetSearchItemForUrl'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchProtocolUI.GetSearchItemForUrl
api_type:
- COM
api_location: ''
ms.openlocfilehash: f8a9bbe3459109946b7a4789d9b9f0fb7473ff05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646874"
---
# <a name="isearchprotocoluigetsearchitemforurl-method"></a>Método ISearchProtocolUI:: GetSearchItemForUrl

Obtém o item de pesquisa para os dados especificados. Esse método é chamado uma vez para cada URL processada pelo gatherer e recupera um ponteiro para o objeto [**ISearchItem**](-search-isearchitem.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetSearchItemForUrl(
  [in]          LPCOLESTR        pcwszURL,
  [in]          IItemPropertyBag *pPropertyBag,
  [out, retval] ISearchItem      **ppSearchItem
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pcwszURL* \[ no\]
</dt> <dd>

Tipo: **LPCOLESTR**

Ponteiro para uma cadeia de caracteres Unicode terminada em dados nulos contendo o item de pesquisa para a URL que está sendo acessada.

</dd> <dt>

*pPropertyBag* \[ no\]
</dt> <dd>

Tipo: **IItemPropertyBag \** _

Ponteiro para um objeto [_ *IItemPropertyBag* *](iitempropertybag.md) que contém informações sobre o item de pesquisa, incluindo as propriedades do item.

</dd> <dt>

*ppSearchItem* \[ out, retval\]
</dt> <dd>

Tipo: **[ **ISearchItem**](-search-isearchitem.md)\*\***

Recebe o endereço de um ponteiro para o objeto [**ISearchItem**](-search-isearchitem.md) criado por esse método. Esse objeto contém informações sobre o item de pesquisa, como o nome do arquivo do item.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

O método **ISearchProtocolUI:: GetSearchItemForUrl** tem suporte apenas no Windows XP e no windows Server 2003 e não deve mais ser usado.

Para visualizar os anexos com um manipulador de protocolo de terceiros em computadores que executam o Windows XP ou o Windows Server 2003, pode ser necessário usar a interface [**ISearchProtocolUI**](-search-isearchprotocolui.md) e as seguintes APIs: as interfaces [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md) e [**ISearchItem**](-search-isearchitem.md) , a estrutura [**LINKINFO**](-search-linkinfo.md) e a enumeração [**LinkId**](-search-linktype.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows XP com SP2\]<br/> |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/> |
| Redistribuível<br/>          | Windows Desktop Search (WDS) 3,0<br/>          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ISearchProtocolUI**](-search-isearchprotocolui.md)
</dt> </dl>

 

 




