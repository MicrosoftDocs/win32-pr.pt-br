---
description: O \_ método Put FormatCodes define a lista de códigos de formato de carga de mídia. A variante contém um SAFEARRAY de BSTRs. Cada BSTR dentro dessa matriz é uma cadeia de caracteres de código de formato.
ms.assetid: b76a7fee-0fae-41fb-a8cd-6803458d9182
title: 'ITMedia: método de ut_FormatCodes de:p (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dac8c2d9e102c6a923a535b8141c546885c583668e32fddb1fc607a8c1179a99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012956"
---
# <a name="itmediaput_formatcodes-method"></a>ITMedia: método UT \_ FormatCodes:p

\[os controles e as interfaces de conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **Put \_ FormatCodes** define a lista de códigos de formato de carga de mídia. A variante contém um SAFEARRAY de **BSTR** s. Cada **BSTR** dentro dessa matriz é uma cadeia de caracteres de código de formato.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_FormatCodes(
  [in] VARIANT NewVal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*NEWVAL* \[ no\]
</dt> <dd>

Lista de códigos de formato de carga de mídia.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código de retorno                                                                                   | Descrição                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | O parâmetro *NEWVAL* não é válido.<br/>                 |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/> |
| <dl> <dt>**E \_ falha**</dt> </dl>        | Erro não especificado.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método ainda não foi implementado.<br/>                  |



 

## <a name="remarks"></a>Comentários

Quando uma lista de formatos de carga é fornecida, isso implica que todos esses formatos podem ser usados na sessão, mas o primeiro desses formatos é o formato padrão para a sessão. Quando o protocolo de transporte é RTP, os códigos de formato são tipos de carga RTP.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| Cabeçalho<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITMedia**](itmedia.md)
</dt> <dt>

[**ITMedia:: obter \_ FormatCodes**](itmedia-get-formatcodes.md)
</dt> </dl>

 

 




