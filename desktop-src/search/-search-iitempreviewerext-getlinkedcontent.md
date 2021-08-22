---
description: Permite a extensão para conteúdo rico para uma propriedade.
ms.assetid: d1b09ea0-7263-4b7c-8c59-25251bb6b285
title: Método IItemPreviewerExt::GetLinkedContent
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
ms.openlocfilehash: e9b99d46d33ba66a9669d47021661b0a359fb2ca98d418735238e2baf3dc9e89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094917"
---
# <a name="iitempreviewerextgetlinkedcontent-method"></a>Método IItemPreviewerExt::GetLinkedContent

Permite a extensão para conteúdo rico para uma propriedade.

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

*dwContext* \[ Em\]
</dt> <dd>

Tipo: **DWORD**

O identificador de contexto para a operação. Substitua o *padrão dwContext* para definir o identificador de contexto como um valor de sua escolha.

</dd> <dt>

*pwszProp* \[ Em\]
</dt> <dd>

Tipo: **LPCOLESTR**

Um ponteiro para a propriedade do conteúdo vinculado como uma cadeia de caracteres Unicode.

</dd> <dt>

*pInfo* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LINKINFO**](-search-linkinfo.md)\***

Recebe um ponteiro para a estrutura [**LINKINFO**](-search-linkinfo.md) na qual o método retorna informações sobre a transação. *pInfo* não deve ser um **ponteiro NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

A interface [**IItemPreviewerExt**](-search-iitempreviewerext.md) tem suporte apenas no Windows XP e Windows Server 2003 e não deve mais ser usada.

Para visualizar anexos com um manipulador de protocolo de terceiros em computadores que executam o Windows XP ou o Windows Server 2003, pode ser necessário usar a interface [**IItemPreviewerExt**](-search-iitempreviewerext.md) e as seguintes APIs: as interfaces [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) e [**ISearchItem,**](-search-isearchitem.md) a estrutura [**LINKINFO**](-search-linkinfo.md) e a enumeração [**LINKTYPE.**](-search-linktype.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP somente com \[ aplicativos da área de trabalho SP2\]<br/> |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/> |
| Redistribuível<br/>          | Windows Pesquisa de Área de Trabalho (WDS) 3.0<br/>          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IItemPreviewerExt**](-search-iitempreviewerext.md)
</dt> </dl>

 

 




