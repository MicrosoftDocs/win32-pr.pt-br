---
description: O método setalias configura um alias H. 323 padrão para o endereço. Esse alias será usado no intercâmbio de configuração de chamada H. 323 para que a outra parte saiba o nome dessa entidade.
ms.assetid: 09608214-7346-4ee8-bbfd-0877d3ad0766
title: 'Método IH323LineEx:: setalias (H323priv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7341d177297cf95f46d07e503244f06b2c4dea71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105800033"
---
# <a name="ih323lineexsetalias-method"></a>Método IH323LineEx:: setalias

\[**Setalias** não está disponível para uso no Windows Vista, no windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **setalias** configura um alias H. 323 padrão para o endereço. Esse alias será usado no intercâmbio de configuração de chamada H. 323 para que a outra parte saiba o nome dessa entidade.

Chamar esse método uma segunda vez substituirá o alias anterior.

O alias definido nessa interface será usado somente quando não houver outra maneira para o TSP encontrar um alias adequado. No futuro, quando o suporte do gatekeeper for adicionado ao TSP, o alias registrado no gatekeeper ou atribuído pelo gatekeeper substituirá o que for definido por meio desse método.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetAlias(
  [in] WCHAR *strAlias,
  [in] DWORD dwLength
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*strAlias* \[ no\]
</dt> <dd>

O alias a ser usado, em Unicode. Terminação **nula** não é necessária.

</dd> <dt>

*dwLength* \[ no\]
</dt> <dd>

O comprimento do nome do alias em número de caracteres, incluindo o terminador **nulo** .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código de retorno                                                                               | Descrição                                                                                                                      |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | O método foi bem-sucedido.<br/>                                                                                                     |
| <dl> <dt>**\_ponteiro E**</dt> </dl> | O número de caracteres indicado em *dwLength* excede o número real de caracteres no parâmetro *strAlias* .<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| parâmetro<br/>       | <dl> <dt>H323priv. h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



 

 




