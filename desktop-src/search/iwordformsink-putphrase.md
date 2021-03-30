---
description: Coloca uma forma alternativa de uma palavra no objeto IWordFormSink.
ms.assetid: 4F6A3E88-A17C-4CA3-849D-FF0DC06D5DC3
title: 'IWordFormSink: método utAltWord de:P (Search. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordFormSink.PutAltWord
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 43539bbf67e23bc37ca92f6a961b945ae581e746
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646864"
---
# <a name="iwordformsinkputaltword-method"></a>IWordFormSink: método utAltWord de:P

Coloca uma forma alternativa de uma palavra no objeto [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT PutAltWord(
  [in] const WCHAR *pwcInBuf ,
  [in]       ULONG cwc
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pwcInBuf* \[ no\]
</dt> <dd>

Um ponteiro para um buffer que contém uma forma alternativa de uma palavra.

</dd> <dt>

*CWC* \[ no\]
</dt> <dd>

O número de caracteres em *pwcInBuf*.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código de retorno                                                                                              | Descrição                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                     | A operação foi concluída com êxito. <br/>                                                                                             |
| <dl> <dt>**Idioma \_ do \_ \_ palavra grande**</dt> </dl> | O valor de *CWC* é maior que o valor de *UlMaxTokenSize* especificado em [**IStemmer:: init**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-init). <br/> |



 

## <a name="remarks"></a>Comentários

Esse método é chamado a partir do método [**GenerateWordForms**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-generatewordforms) da implementação [**IStemmer**](/windows/win32/api/indexsrv/nn-indexsrv-istemmer) . Todas as formas alternativas para uma palavra, exceto a última, são colocadas no objeto [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) chamando **IWordFormSink::P utaltword**. A forma alternativa final de uma palavra, que é sempre a forma original da palavra, é tratada chamando [**IWordFormSink::P utword**](iwordformsink-putword.md).

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

 

 
