---
description: Coloca uma quebra após a palavra anterior.
ms.assetid: C8622067-D8CE-4099-8B9F-941720F4706B
title: 'IWordSink: método utBreak de:P (Search. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.PutBreak
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: c6407f1307b4860960c5202af13de736c7921139
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296235"
---
# <a name="iwordsinkputbreak-method"></a>IWordSink: método utBreak de:P

Coloca uma quebra após a palavra anterior.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT PutBreak(
  [in] WORDREP_BREAK_TYPE breakType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*breaktype* \[ no\]
</dt> <dd>

Um valor de [**\_ \_ tipo de quebra de WORDREP**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85)) que indica o tipo de quebra que o WordSink insere após a palavra anterior. Cada quebra ocupa uma posição exclusiva no índice. Portanto, inserir quebras entre palavras altera a distância relativa entre palavras.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código de retorno                                                                          | Descrição                                          |
|--------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | A operação foi concluída com êxito.<br/> |



 

## <a name="remarks"></a>Comentários

Os métodos [**IWordSinkPutWord**](iwordsink-putword.md) e [**IWordSink::P utaltword**](iwordsink-putaltword.md) inserem automaticamente uma quebra de fim de palavra (EOW, indicada pelo \_ elemento WORDREP Break EOW \_ do tipo enumerado [**de \_ \_ tipo de interrupção WORDREP**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85)) ) após cada palavra. Chame o método **PutBreak** para inserir um tipo de quebra diferente do fim da palavra. Esse método não altera o buffer de texto de origem (*pSourceText*) ou incrementa a contagem de caracteres (*CWC*). No entanto, ele incrementa a posição atual no índice e afeta os resultados da consulta.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Pesquisar. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IWordSink**](iwordsink.md)
</dt> </dl>

 

 
