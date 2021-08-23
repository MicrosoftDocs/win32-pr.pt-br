---
description: Coloca uma palavra e sua posição no objeto IWordSink.
ms.assetid: 3D645BF6-895E-46E2-92A3-3E301CD228D8
title: Método IWordSink::P utWord (Search.h)
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
ms.openlocfilehash: e860aafbef633e226933281aaaa0be5c6429387542e7c3ae2d65d3026fd7fe37
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119597596"
---
# <a name="iwordsinkputword-method"></a>Método IWordSink::P utWord

Coloca uma palavra e sua posição no [**objeto IWordSink.**](iwordsink.md)

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

*cwc* \[ Em\]
</dt> <dd>

O número de caracteres *em pwcInBuf*.

</dd> <dt>

*pwcInBuf* \[ Em\]
</dt> <dd>

Um ponteiro para um buffer que contém uma forma alternativa de uma palavra do texto de origem. Esse parâmetro não é modificado pelo **PutWord.** Você pode passar o *parâmetro pTextSource* de [**IWordBreaker::BreakText conforme**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) apropriado.

</dd> <dt>

*cwcSrcLen* \[ Em\]
</dt> <dd>

O número de caracteres no buffer de texto de origem (indicado pelo parâmetro *pTextSource* para [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)) que correspondem à palavra contida em *pwcInBuf*.

</dd> <dt>

*cwcSrcPos* \[ Em\]
</dt> <dd>

A posição inicial da palavra *em pwcInBuf* no buffer de texto de origem (indicado pelo parâmetro *pTextSource* para [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código de retorno                                                                                              | Descrição                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                     | A operação foi concluída com êxito. Também indica que não há mais texto disponível para repor o buffer.<br/>                                  |
| <dl> <dt>**LANGUAGE \_ S \_ LARGE \_ WORD**</dt> </dl> | O valor *de cwc* é maior que o valor de *ulMaxTokenSize* especificado em [**IWordBreaker::Init**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-init). <br/> |



 

## <a name="remarks"></a>Comentários

Recomendamos que **o método IWordSink::P utWord** sempre contenha a palavra original, conforme encontrado em *pTextSource*. Formas alternativas da palavra são passadas para WordSink usando [**IWordSink::P utAltWord**](iwordsink-putaltword.md). Também recomendamos que as palavras em *pwcInBuf* corresponderem ao texto de origem o mais próximo possível. Por exemplo, mantenha maiúsculas e acentos sempre que possível.

Essa chamada deve ser feita para cada palavra recuperada de *pTextSource,* exceto aquelas para as quais a chamada [**IWordSink::P utAltWord**](iwordsink-putaltword.md) foi feita. A palavra é encerrada com um caractere EOW quando é salva no WordSink.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Search.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IWordSink**](iwordsink.md)
</dt> </dl>

 

 
