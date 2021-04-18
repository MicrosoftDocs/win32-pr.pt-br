---
description: Coloca o formulário original do Word no objeto IWordFormSink.
ms.assetid: 333A3109-6C0A-42AE-9E10-87F53C7F737C
title: 'IWordFormSink: método utWord de:P (Search. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordFormSink.PutWord
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 438cb41e50f264bd373ae2ef8e84598b651b0352
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763279"
---
# <a name="iwordformsinkputword-method"></a>IWordFormSink: método utWord de:P

Coloca o formulário original do Word no objeto [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT PutWord(
  [in] const WCHAR *pwcInBuf ,
  [in]       ULONG cwc
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pwcInBuf* \[ no\]
</dt> <dd>

Um ponteiro para um buffer que contém a forma alternativa final de uma palavra, que é sempre a palavra original.

</dd> <dt>

*CWC* \[ no\]
</dt> <dd>

O número de caracteres em *pwcInBuf*.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código de retorno                                                                          | Description                                           |
|--------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | A operação foi concluída com êxito. <br/> |



 

## <a name="remarks"></a>Comentários

**PutWord** é chamado do método [**GenerateWordForms**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-generatewordforms) da implementação [**IStemmer**](/windows/win32/api/indexsrv/nn-indexsrv-istemmer) . Esse método manipula a forma original de uma palavra e é chamado por último. Todos os formulários alternativos anteriores para uma palavra são colocados no objeto [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) chamando [**IWordFormSink::P utaltword**](iwordformsink-putphrase.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Pesquisar. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink)
</dt> </dl>

 

 
