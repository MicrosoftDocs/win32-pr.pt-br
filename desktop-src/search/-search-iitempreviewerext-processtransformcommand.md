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
ms.openlocfilehash: f93d4be0bf9491c4fd2f6074c00692d6f634704ec820a34baeb4f1d52343c36a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118969766"
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

Tipo: **variante \***

Um ponteiro para a variante de resultado. *pVarResult* não deve ser um ponteiro **nulo** .

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

 

 




