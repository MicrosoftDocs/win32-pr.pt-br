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
ms.openlocfilehash: fe41cf8d9ec92c0c71be5130aded0b7db539b9b1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757995"
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

## <a name="return-value"></a>Retornar valor

A hora local que corresponde ao tempo universal coordenado especificado.

## <a name="remarks"></a>Comentários

Enquanto o sistema usa o tempo universal coordenado internamente, os aplicativos geralmente exibem a hora local, que é a data e a hora do dia para o fuso horário local do computador.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Utilitários**](utilities.md)
</dt> </dl>

 

 




