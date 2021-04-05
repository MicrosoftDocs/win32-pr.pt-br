---
description: Permite o processamento de um comando de transformação encontrado em um modelo de visualização.
ms.assetid: 0b81b780-8bd1-4667-a0a1-65319f209603
title: 'IItemPreviewerExt: método rocessTransformCommand de:P'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt.ProcessTransformCommand
api_type:
- COM
api_location: ''
ms.openlocfilehash: 384294aac177679ea7445edb880198d250310625
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826916"
---
# <a name="iitempreviewerextprocesstransformcommand-method"></a>IItemPreviewerExt: método rocessTransformCommand de:P

Permite o processamento de um comando de transformação encontrado em um modelo de visualização.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ProcessTransformCommand(
  [in]          DWORD     dwContext,
  [in]          LPCOLESTR pwszName,
  [in]          LPCOLESTR pwszArg,
  [out, retval] VARIANT   *pvarResult
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwContext* \[ no\]
</dt> <dd>

Tipo: **DWORD**

O identificador de contexto para a operação. Substitua o padrão *dwContext* para definir o identificador de contexto como um valor de sua escolha.

</dd> <dt>

*pwszName* \[ no\]
</dt> <dd>

Tipo: **LPCOLESTR**

Um ponteiro para o nome do comando de transformação como uma cadeia de caracteres Unicode.

</dd> <dt>

*pwszArg* \[ no\]
</dt> <dd>

Tipo: **LPCOLESTR**

Um ponteiro para o argumento como uma cadeia de caracteres Unicode.

</dd> <dt>

*pVarResult* \[ out, retval\]
</dt> <dd>

Tipo: **Variant \** _

Um ponteiro para a variante de resultado. _pvarResult * não deve ser um ponteiro **nulo** .

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

 

 




