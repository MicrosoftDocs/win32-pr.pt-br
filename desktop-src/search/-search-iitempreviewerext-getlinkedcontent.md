---
description: Permite a extensão para o conteúdo avançado de uma propriedade.
ms.assetid: d1b09ea0-7263-4b7c-8c59-25251bb6b285
title: 'Método IItemPreviewerExt:: GetLinkedContent'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt.GetLinkedContent
api_type:
- COM
api_location: ''
ms.openlocfilehash: 7d450bbda2ac7c24b49d1ca5032fd1c59754652e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764286"
---
# <a name="iitempreviewerextgetlinkedcontent-method"></a>Método IItemPreviewerExt:: GetLinkedContent

Permite a extensão para o conteúdo avançado de uma propriedade.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetLinkedContent(
  [in]          DWORD     dwContext,
  [in]          LPCOLESTR pwszProp,
  [out, retval] LINKINFO  *pInfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwContext* \[ no\]
</dt> <dd>

Tipo: **DWORD**

O identificador de contexto para a operação. Substitua o padrão *dwContext* para definir o identificador de contexto como um valor de sua escolha.

</dd> <dt>

*pwszProp* \[ no\]
</dt> <dd>

Tipo: **LPCOLESTR**

Um ponteiro para a propriedade do conteúdo vinculado como uma cadeia de caracteres Unicode.

</dd> <dt>

*pInfo* \[ out, retval\]
</dt> <dd>

Tipo: **[**LINKINFO**](-search-linkinfo.md) \** _

Recebe um ponteiro para a estrutura [_ *LINKINFO* *](-search-linkinfo.md) na qual o método retorna informações sobre a transação. *pInfo* não deve ser um ponteiro **nulo** .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

A interface [**IItemPreviewerExt**](-search-iitempreviewerext.md) tem suporte apenas no Windows XP e no windows Server 2003 e não deve mais ser usada.

Para visualizar os anexos com um manipulador de protocolo de terceiros em computadores que executam o Windows XP ou o Windows Server 2003, pode ser necessário usar a interface [**IItemPreviewerExt**](-search-iitempreviewerext.md) e as seguintes APIs: as interfaces [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) e [**ISearchItem**](-search-isearchitem.md) , a estrutura [**LINKINFO**](-search-linkinfo.md) e a enumeração [**LinkId**](-search-linktype.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows XP com SP2\]<br/> |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/> |
| Redistribuível<br/>          | Windows Desktop Search (WDS) 3,0<br/>          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IItemPreviewerExt**](-search-iitempreviewerext.md)
</dt> </dl>

 

 




