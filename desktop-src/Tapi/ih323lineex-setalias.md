---
description: O método SetAlias configura um alias H.323 padrão para o endereço. Esse alias será usado na troca de configuração de chamada H.323 para que a outra parte saiba o nome dessa parte.
ms.assetid: 09608214-7346-4ee8-bbfd-0877d3ad0766
title: Método IH323LineEx::SetAlias (H323priv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 464c6707c3221fda1ef245e0302731ee7c6a1cf274c7ecac537c55f7f48437a0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992186"
---
# <a name="ih323lineexsetalias-method"></a>Método IH323LineEx::SetAlias

\[**SetAlias** não está disponível para uso no Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. A API do Cliente RTC fornece funcionalidade semelhante.\]

O **método SetAlias** configura um alias H.323 padrão para o endereço. Esse alias será usado na troca de configuração de chamada H.323 para que a outra parte saiba o nome dessa parte.

Chamar esse método uma segunda vez substituirá o alias anterior.

O alias definido nessa interface será usado somente quando não houver outra maneira para o TSP encontrar um alias adequado. No futuro, quando o suporte ao gatekeeper for adicionado ao TSP, o alias registrado no gatekeeper ou atribuído pelo gatekeeper substituirá o que estiver definido por meio desse método.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetAlias(
  [in] WCHAR *strAlias,
  [in] DWORD dwLength
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*strAlias* \[ Em\]
</dt> <dd>

O alias a ser usado, em Unicode. **A** terminação nula não é necessária.

</dd> <dt>

*dwLength* \[ Em\]
</dt> <dd>

O comprimento do nome do alias em número de caracteres, incluindo o **terminador** nulo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código de retorno                                                                               | Descrição                                                                                                                      |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | O método foi bem-sucedido.<br/>                                                                                                     |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl> | O número de caracteres indicados *em dwLength* excede o número real de caracteres no *parâmetro strAlias.*<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 3.0 ou posterior<br/>                                                 |
| Cabeçalho<br/>       | <dl> <dt>H323priv.h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



 

 




