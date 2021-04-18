---
description: Coloca uma palavra e sua posição no objeto IWordSink.
ms.assetid: 3D645BF6-895E-46E2-92A3-3E301CD228D8
title: 'IWordSink: método utWord de:P (Search. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.PutWord
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 5f622e09c2b82bc8de986dafcc83247617caec75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813574"
---
# <a name="iwordsinkputword-method"></a>IWordSink: método utWord de:P

Coloca uma palavra e sua posição no objeto [**IWordSink**](iwordsink.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT PutWord(
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

Um ponteiro para um buffer que contém uma forma alternativa de uma palavra do texto de origem. Esse parâmetro não é modificado por **PutWord**. Você pode passar o parâmetro *pTextSource* de [**IWordBreaker:: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) conforme apropriado.

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
| <dl> <dt>**S \_ OK**</dt> </dl>                     | A operação foi concluída com êxito. Também indica que não há mais texto disponível para reabastecer o buffer.<br/>                                  |
| <dl> <dt>**Idioma \_ do \_ \_ palavra grande**</dt> </dl> | O valor de *CWC* é maior que o valor de *UlMaxTokenSize* especificado em [**IWordBreaker:: init**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-init). <br/> |



 

## <a name="remarks"></a>Comentários

Recomendamos que o método **IWordSink::P utword** sempre contenha a palavra original como encontrada em *pTextSource*. Formas alternativas da palavra são passadas para WordSink usando [**IWordSink::P utaltword**](iwordsink-putaltword.md). Também recomendamos que as palavras em *pwcInBuf* correspondam ao texto de origem o mais próximo possível. Por exemplo, mantenha a capitalização e os acentos sempre que possível.

Essa chamada deve ser feita para cada palavra recuperada de *pTextSource* , exceto aquelas para as quais a chamada [**IWordSink::P utaltword**](iwordsink-putaltword.md) foi feita. A palavra é terminada com um caractere EOW quando é salva no WordSink.

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

 

 
