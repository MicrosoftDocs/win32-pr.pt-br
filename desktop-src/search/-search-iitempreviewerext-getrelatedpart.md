---
description: Obtém uma parte do corpo relacionada para a incorporação no fluxo MHTML de saída.
ms.assetid: 7810568b-5fb7-4814-aa9f-d7ae805c97e1
title: Método IItemPreviewerExt::GetRelatedPart
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt.GetRelatedPart
api_type:
- COM
api_location: ''
ms.openlocfilehash: 9abc4415eef014697376c9df4b89af47037a99df5c9ab5a3c74a3d7825b344c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863969"
---
# <a name="iitempreviewerextgetrelatedpart-method"></a>Método IItemPreviewerExt::GetRelatedPart

Obtém uma parte do corpo relacionada para a incorporação no fluxo MHTML de saída.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetRelatedPart(
  [in]          DWORD     dwContext,
  [in]          LPCOLESTR pwszProp,
  [in]          DWORD     dwIndex,
  [out, retval] LINKINFO  *pInfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwContext* \[ Em\]
</dt> <dd>

Tipo: **DWORD**

O identificador de contexto para a operação. Substitua o **padrão dwContext** para definir o identificador de contexto como um valor de sua escolha.

</dd> <dt>

*pwszProp* \[ Em\]
</dt> <dd>

Tipo: **LPCOLESTR**

Um ponteiro para a propriedade do conteúdo vinculado como uma cadeia de caracteres Unicode.

</dd> <dt>

*dwIndex* \[ Em\]
</dt> <dd>

Tipo: **DWORD**

Um valor inteiro longo sem sinal que contém o índice baseado em zero da parte do corpo relacionada.

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

 

 




