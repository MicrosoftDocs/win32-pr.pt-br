---
description: Obtém o item de pesquisa para os dados especificados. Esse método é chamado uma vez para cada URL processada pelo coletor e recupera um ponteiro para o objeto ISearchItem.
ms.assetid: 35893bc9-8327-44f9-a9fc-7855c5c063e3
title: Método ISearchProtocolUI::GetSearchItemForUrl
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
ms.openlocfilehash: 8636f42026fe44131e149b0e378089b70c7d4f49b9e23b5d48ebe50aa5721d79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119594806"
---
# <a name="isearchprotocoluigetsearchitemforurl-method"></a>Método ISearchProtocolUI::GetSearchItemForUrl

Obtém o item de pesquisa para os dados especificados. Esse método é chamado uma vez para cada URL processada pelo coletor e recupera um ponteiro para o [**objeto ISearchItem.**](-search-isearchitem.md)

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

*pcwszURL* \[ Em\]
</dt> <dd>

Tipo: **LPCOLESTR**

Ponteiro para uma cadeia de caracteres Unicode terminada em dados nulos que contém o item de pesquisa para a URL que está sendo acessada.

</dd> <dt>

*pPropertyBag* \[ Em\]
</dt> <dd>

Tipo: **IItemPropertyBag \***

Ponteiro para um [**objeto IItemPropertyBag**](iitempropertybag.md) que contém informações sobre o item de pesquisa, incluindo as propriedades do item.

</dd> <dt>

*ppSearchItem* \[ out, retval\]
</dt> <dd>

Tipo: **[ **ISearchItem**](-search-isearchitem.md)\*\***

Recebe o endereço de um ponteiro para o [**objeto ISearchItem**](-search-isearchitem.md) criado por esse método. Esse objeto contém informações sobre o item de pesquisa, como o nome do arquivo do item.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

O método **ISearchProtocolUI::GetSearchItemForUrl** tem suporte apenas no Windows XP e no Windows Server 2003 e não deve mais ser usado.

Para visualizar anexos com um manipulador de protocolo de terceiros em computadores que executam o Windows XP ou o Windows Server 2003, pode ser necessário usar a interface [**ISearchProtocolUI**](-search-isearchprotocolui.md) e as seguintes APIs: as interfaces [**IItemPreviewerExt,**](-search-iitempreviewerext.md) [**IItemPropertyBag**](iitempropertybag.md) e [**ISearchItem,**](-search-isearchitem.md) a estrutura [**LINKINFO**](-search-linkinfo.md) e a enumeração [**LINKTYPE.**](-search-linktype.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP somente com \[ aplicativos da área de trabalho SP2\]<br/> |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/> |
| Redistribuível<br/>          | Windows Pesquisa de Área de Trabalho (WDS) 3.0<br/>          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ISearchProtocolUI**](-search-isearchprotocolui.md)
</dt> </dl>

 

 




