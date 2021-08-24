---
description: Analisar texto para identificar palavras e fornece os resultados para o objeto WordSink.
ms.assetid: 42bfc961-c095-4380-9b55-b58a0d9f2c00
title: Método IWordInfo::BreakText
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordInfo.BreakText
api_type:
- COM
api_location:
- Msir3jp.dll
ms.openlocfilehash: 4cb4e4b27b52a4fb22a65f382a20c51a43ca5c77feb14828a7ea252e75c3b0f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749736"
---
# <a name="iwordinfobreaktext-method"></a>Método IWordInfo::BreakText

\[Esse método é obsoleto e não tem suporte no Windows Vista.\]

Analisar texto para identificar palavras e fornece os resultados para o [objeto WordSink.](/previous-versions//ms691570(v=vs.85))

## <a name="syntax"></a>Sintaxe


```C++
HRESULT BreakText(
  [in] TEXT_SOURCE *pTextSource,
  [in] IWordSink   *pWordSink,
  [in] DWORD       fBreakMode
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pTextSource* \[ Em\]
</dt> <dd>

Um ponteiro para uma estrutura [TEXT \_ SOURCE](/previous-versions//ms690919(v=vs.85)) que contém o texto Unicode.

</dd> <dt>

*pWordSink* \[ Em\]
</dt> <dd>

Um ponteiro para o [objeto WordSink](/previous-versions//ms691570(v=vs.85)) que recebe e trata as palavras geradas por esse método. Se esse parâmetro for **NULL,** o método não quebrará a cadeia de caracteres em palavras.

</dd> <dt>

*fBreakMode* \[ Em\]
</dt> <dd>

O modo de quebra. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                                                                                                                                   | Significado                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="IWORDINFO_BREAKTEXTMODE_DICTFORM"></span><span id="iwordinfo_breaktextmode_dictform"></span><dl> <dt>**IWORDINFO \_ BREAKTEXTMODE \_ DICTFORM**</dt> <dt>0x00000002</dt> </dl> | Word quebra a cadeia de caracteres de texto e passa a forma de dicionário das palavras para o **objeto WordSink.**<br/> |
| <span id="IWORDINFO_BREAKTEXTMODE_SMARTSEL"></span><span id="iwordinfo_breaktextmode_smartsel"></span><dl> <dt>**IWORDINFO \_ BREAKTEXTMODE \_ SMARTSEL**</dt> <dt>0x00000001</dt> </dl> | Word quebra a cadeia de caracteres de texto e passa as palavras para o **objeto WordSink.**<br/>                        |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna um dos valores a seguir.



| Código de retorno                                                                            | Descrição                                                                                             |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | A operação foi realizada com êxito. Não há mais texto disponível para repor o buffer *pTextSource.*<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | O *parâmetro pTextSource* é **NULL.**<br/>                                                     |



 

## <a name="remarks"></a>Comentários

Use o **membro pfnFillTextBuffer** da estrutura **TEXT \_ SOURCE** para reabastecer o texto de origem. Esse método deve manipular todos os valores de retorno da função de retorno de chamada **pfnFillTextBuffer.** Se ocorrer um erro, termine o processamento do texto no buffer antes de tratar o erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                   |
| Fim do suporte ao cliente<br/>    | Windows XP<br/>                                                                  |
| Fim do suporte ao servidor<br/>    | Windows Server 2003<br/>                                                         |
| DLL<br/>                      | <dl> <dt>Msir3jp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IWordInfo**](iwordinfo.md)
</dt> <dt>

[FONTE DE \_ TEXTO](/previous-versions//ms690919(v=vs.85))
</dt> <dt>

[**Wordinfo**](wordinfo-coclass.md)
</dt> <dt>

[WordSink](/previous-versions//ms691570(v=vs.85))
</dt> </dl>

 

 
