---
description: Converte o tempo universal coordenado (hora de Greenwich) na hora local do computador.
ms.assetid: 4085d7cb-d346-477d-a043-e96fb951c35a
title: Método Utilities. UTCTimeToLocalTime
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.UTCTimeToLocalTime
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c1ad7236564fff2f9a3814beda9bedacbf96fbc9ca2678546304ee108891bea1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005144"
---
# <a name="utilitiesutctimetolocaltime-method"></a>Método Utilities. UTCTimeToLocalTime

\[O método **UTCTimeToLocalTime** está disponível para uso nos sistemas operacionais especificados na seção requisitos.\]

O método **UTCTimeToLocalTime** converte o tempo universal coordenado (hora de Greenwich) na hora local do computador.

## <a name="syntax"></a>Sintaxe


```VB
Utilities.UTCTimeToLocalTime( _
  ByVal UTCTime _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*UTCTime* \[ no\]
</dt> <dd>

O tempo universal coordenado a ser convertido na hora local do computador.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

A hora local que corresponde ao tempo universal coordenado especificado.

## <a name="remarks"></a>Comentários

Enquanto o sistema usa o tempo universal coordenado internamente, os aplicativos geralmente exibem a hora local, que é a data e a hora do dia para o fuso horário local do computador.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | capicom 2,0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Utilitários**](utilities.md)
</dt> </dl>

 

 




