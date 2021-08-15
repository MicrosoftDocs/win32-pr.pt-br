---
description: Obtém uma parte do corpo relacionado para inserir no fluxo de saída de MHTML.
ms.assetid: 7810568b-5fb7-4814-aa9f-d7ae805c97e1
title: 'Método IItemPreviewerExt:: GetRelatedPart'
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
# <a name="iitempreviewerextgetrelatedpart-method"></a>Método IItemPreviewerExt:: GetRelatedPart

Obtém uma parte do corpo relacionado para inserir no fluxo de saída de MHTML.

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

*dwContext* \[ no\]
</dt> <dd>

Tipo: **DWORD**

O identificador de contexto para a operação. Substitua o padrão **dwContext** para definir o identificador de contexto como um valor de sua escolha.

</dd> <dt>

*pwszProp* \[ no\]
</dt> <dd>

Tipo: **LPCOLESTR**

Um ponteiro para a propriedade do conteúdo vinculado como uma cadeia de caracteres Unicode.

</dd> <dt>

*dwIndex* \[ no\]
</dt> <dd>

Tipo: **DWORD**

Um valor inteiro longo sem sinal que contém o índice de base zero da parte do corpo relacionado.

</dd> <dt>

*pInfo* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LINKINFO**](-search-linkinfo.md)\***

Recebe um ponteiro para a estrutura [**LINKINFO**](-search-linkinfo.md) na qual o método retorna informações sobre a transação. *pInfo* não deve ser um ponteiro **nulo** .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

a interface [**IItemPreviewerExt**](-search-iitempreviewerext.md) tem suporte apenas no Windows XP e no Windows Server 2003 e não deve mais ser usada.

para visualizar os anexos com um manipulador de protocolo de terceiros em computadores que executam o Windows XP ou o Windows Server 2003, pode ser necessário usar a interface [**IItemPreviewerExt**](-search-iitempreviewerext.md) e as seguintes APIs: as interfaces [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) e [**ISearchItem**](-search-isearchitem.md) , a estrutura [**LINKINFO**](-search-linkinfo.md) e a enumeração [**linkid**](-search-linktype.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP somente com \[ aplicativos de área de trabalho do SP2\]<br/> |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/> |
| Redistribuível<br/>          | Windows Pesquisa de desktop (WDS) 3,0<br/>          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IItemPreviewerExt**](-search-iitempreviewerext.md)
</dt> </dl>

 

 




