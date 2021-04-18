---
description: Converte a hora local do computador em tempo universal coordenado (Greenwich Mean Time).
ms.assetid: ff5d40ba-7d94-4f11-9c18-e41752d1d7b9
title: Método Utilities. LocalTimeToUTCTime
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.LocalTimeToUTCTime
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2691e3306a84ce4eff3d73df4b070ba4b65671f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105767815"
---
# <a name="utilitieslocaltimetoutctime-method"></a>Método Utilities. LocalTimeToUTCTime

\[O método **LocalTimeToUTCTime** está disponível para uso nos sistemas operacionais especificados na seção requisitos.\]

O método **LocalTimeToUTCTime** converte a hora local do computador em tempo universal coordenado (Greenwich Mean Time).

## <a name="syntax"></a>Sintaxe


```VB
Utilities.LocalTimeToUTCTime( _
  ByVal LocalTime _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Localtime* \[ no\]
</dt> <dd>

A hora local a ser convertida em tempo universal coordenado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O tempo universal coordenado que corresponde à hora local especificada.

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

 

 




