---
description: O \_ método Put FormatCodes define a lista de códigos de formato de carga de mídia. A variante contém um SAFEARRAY de BSTRs. Cada BSTR dentro dessa matriz é uma cadeia de caracteres de código de formato.
ms.assetid: b76a7fee-0fae-41fb-a8cd-6803458d9182
title: 'ITMedia: método de ut_FormatCodes de:p (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9131f946635c2bb066e704f1d6245c1c30d1372
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760342"
---
# <a name="itmediaput_formatcodes-method"></a>ITMedia: método UT \_ FormatCodes:p

\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

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

## <a name="return-value"></a>Retornar valor

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
| parâmetro<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITMedia**](itmedia.md)
</dt> <dt>

[**ITMedia:: obter \_ FormatCodes**](itmedia-get-formatcodes.md)
</dt> </dl>

 

 




