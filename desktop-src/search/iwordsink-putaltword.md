---
description: Coloca uma palavra alternativa e sua posição no objeto IWordSink.
ms.assetid: 5C8A9B30-F9B5-42E9-ADAC-A11230F0C2FA
title: 'IWordSink: método utAltWord de:P (Search. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.PutAltWord
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 21fd9eb9ac5a1bf0f52d6574595dc495432d7ec9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761251"
---
# <a name="iwordsinkputaltword-method"></a>IWordSink: método utAltWord de:P

Coloca uma palavra alternativa e sua posição no objeto [**IWordSink**](iwordsink.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT PutAltWord(
  [in]       ULONG cwc,
  [in] const WCHAR *pwcInBuf,
  [in]       ULONG cwcSrcLen,
  [in]       ULONG cwcSrcPos
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*CWC* \[ no\]
</dt> <dd>

O número de caracteres em *pwcInBuf*.

</dd> <dt>

*pwcInBuf* \[ no\]
</dt> <dd>

Um ponteiro para um buffer que contém uma forma alternativa de uma palavra do texto de origem. Esse parâmetro não é modificado por **PutAltWord**. Você pode passar o parâmetro *pTextSource* de [**IWordBreaker:: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) conforme apropriado.

</dd> <dt>

*cwcSrcLen* \[ no\]
</dt> <dd>

O número de caracteres no buffer de texto de origem (indicado pelo parâmetro *pTextSource* para [**IWordBreaker:: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)) que correspondem à palavra contida em *pwcInBuf*.

</dd> <dt>

*cwcSrcPos* \[ no\]
</dt> <dd>

A posição inicial da palavra em *pwcInBuf* no buffer de texto de origem (indicado pelo parâmetro *pTextSource* como [**IWordBreaker:: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código de retorno                                                                                              | Description                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                     | A operação foi concluída com êxito. Também indica que não há mais texto a ser processado.<br/>                                            |
| <dl> <dt>**Idioma \_ do \_ \_ palavra grande**</dt> </dl> | O valor de *CWC* é maior que o valor de *UlMaxTokenSize* especificado em [**IWordBreaker:: init**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-init). <br/> |



 

## <a name="remarks"></a>Comentários

**PutAltWord** coloca uma forma alternativa de uma palavra no [**IWordSink**](iwordsink.md). A palavra é colocada na mesma posição que a palavra original na fonte de texto (*pTextSource* em [**IWordBreaker:: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)). Por padrão, o **PutAltWord** encerra palavras com um tipo de quebra de WORDREP de interrupção de **\_ \_ EOW** do tipo enumerado de [**\_ quebra \_ de WORDREP**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85)) .

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

 

 
