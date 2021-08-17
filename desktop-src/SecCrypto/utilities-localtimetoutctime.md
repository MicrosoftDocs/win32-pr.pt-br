---
description: Converte a hora local do computador em Tempo Universal Coordenado (Hora média de Greenwich).
ms.assetid: ff5d40ba-7d94-4f11-9c18-e41752d1d7b9
title: Método Utilities.LocalTimeToUTCTime
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
ms.openlocfilehash: 03efb6cdfbea712f2fbca194073b89bcee66975481c1a7c0fdc2d7bd385eb652
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117971017"
---
# <a name="utilitieslocaltimetoutctime-method"></a>Método Utilities.LocalTimeToUTCTime

\[O **método LocalTimeToUTCTime** está disponível para uso nos sistemas operacionais especificados na seção Requisitos.\]

O **método LocalTimeToUTCTime** converte a hora local do computador em Tempo Universal Coordenado (Hora de Greenwich).

## <a name="syntax"></a>Sintaxe


```VB
Utilities.LocalTimeToUTCTime( _
  ByVal LocalTime _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*LocalTime* \[ Em\]
</dt> <dd>

A hora local a ser convertida em Tempo Universal Coordenado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O Tempo Universal Coordenado que corresponde à hora local especificada.

## <a name="remarks"></a>Comentários

Embora o sistema use Tempo Universal Coordenado internamente, os aplicativos geralmente exibem a hora local, que é a data e a hora do dia para o fuso horário local do computador.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2.0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Utilitários**](utilities.md)
</dt> </dl>

 

 




