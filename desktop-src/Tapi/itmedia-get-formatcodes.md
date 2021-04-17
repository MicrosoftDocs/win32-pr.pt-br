---
description: O \_ método Get FormatCodes Obtém a lista de códigos de formato de carga de mídia. A variante retorna um SAFEARRAY de BSTRs. Cada BSTR dentro dessa matriz é uma cadeia de caracteres de código de formato.
ms.assetid: 8663d7e8-d46f-44d1-93db-9b5142bb28dd
title: 'Método ITMedia:: get_FormatCodes (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce9e28a0323ac001c948a3b19b8dae2cfe9daf5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757226"
---
# <a name="itmediaget_formatcodes-method"></a>Método ITMedia:: get \_ FormatCodes

\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **Get \_ FormatCodes** Obtém a lista de códigos de formato de carga de mídia. A variante retorna um SAFEARRAY de **BSTR** s. Cada **BSTR** dentro dessa matriz é uma cadeia de caracteres de código de formato.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_FormatCodes(
  [out] VARIANT *pVal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PVal* \[ fora\]
</dt> <dd>

Matriz de códigos de formato de carga de mídia.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código de retorno                                                                                   | Descrição                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                    |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | O parâmetro *PVal* não é um ponteiro válido.<br/>         |
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

[**ITMedia::p UT \_ FormatCodes**](itmedia-put-formatcodes.md)
</dt> </dl>

 

 




