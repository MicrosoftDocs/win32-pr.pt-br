---
description: Analisa o texto para identificar palavras e fornece os resultados para o objeto WordSink.
ms.assetid: 42bfc961-c095-4380-9b55-b58a0d9f2c00
title: 'Método IWordInfo:: BreakText'
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
ms.openlocfilehash: f6f71e92137490d56c93d9443506c2d7ffa2688a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010107"
---
# <a name="iwordinfobreaktext-method"></a>Método IWordInfo:: BreakText

\[Esse método é obsoleto e não tem suporte no Windows Vista.\]

Analisa o texto para identificar palavras e fornece os resultados para o objeto [WordSink](/previous-versions//ms691570(v=vs.85)) .

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

*pTextSource* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura de [ \_ fonte de texto](/previous-versions//ms690919(v=vs.85)) que contém o texto Unicode.

</dd> <dt>

*pWordSink* \[ no\]
</dt> <dd>

Um ponteiro para o objeto [WordSink](/previous-versions//ms691570(v=vs.85)) que recebe e manipula as palavras geradas por esse método. Se esse parâmetro for **nulo**, o método não quebrará a cadeia de caracteres em palavras.

</dd> <dt>

*fBreakMode* \[ no\]
</dt> <dd>

O modo de interrupção. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                                                                                                                                   | Significado                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="IWORDINFO_BREAKTEXTMODE_DICTFORM"></span><span id="iwordinfo_breaktextmode_dictform"></span><dl> <dt>**IWORDINFO \_ BREAKTEXTMODE \_ DICTFORM**</dt> <dt>0x00000002</dt> </dl> | O Word quebra a cadeia de texto e passa o formulário de dicionário das palavras para o objeto **WordSink** .<br/> |
| <span id="IWORDINFO_BREAKTEXTMODE_SMARTSEL"></span><span id="iwordinfo_breaktextmode_smartsel"></span><dl> <dt>**IWORDINFO \_ BREAKTEXTMODE \_ SMARTSEL**</dt> <dt>0x00000001</dt> </dl> | O Word quebra a cadeia de texto e passa as palavras para o objeto **WordSink** .<br/>                        |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna um dos valores a seguir.



| Código de retorno                                                                            | Descrição                                                                                             |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | A operação foi realizada com êxito. Não há mais texto disponível para reabastecer o buffer *pTextSource* .<br/> |
| <dl> <dt>**E \_ falha**</dt> </dl> | O parâmetro *pTextSource* é **nulo**.<br/>                                                     |



 

## <a name="remarks"></a>Comentários

Use o membro **pfnFillTextBuffer** da estrutura **de \_ fonte de texto** para reabastecer o texto de origem. Esse método deve lidar com todos os valores de retorno da função de retorno de chamada **pfnFillTextBuffer** . Se ocorrer um erro, conclua o processamento do texto no buffer antes de manipular o erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                   |
| Fim do suporte do cliente<br/>    | Windows XP<br/>                                                                  |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                                                         |
| DLL<br/>                      | <dl> <dt>Msir3jp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IWordInfo**](iwordinfo.md)
</dt> <dt>

[fonte de texto \_](/previous-versions//ms690919(v=vs.85))
</dt> <dt>

[**WordInfo**](wordinfo-coclass.md)
</dt> <dt>

[WordSink](/previous-versions//ms691570(v=vs.85))
</dt> </dl>

 

 
