---
description: Método IEnumTime::Next – o método Next obtém o próximo número especificado de elementos na sequência de enumeração.
ms.assetid: e8ca77b8-0322-43b4-9996-26f584cf878a
title: Método IEnumTime::Next (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6068d23fae96d5623ced72f44e6e8d185f861b6c49ff085f1b6e9e58bc489b89
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905956"
---
# <a name="ienumtimenext-method"></a>Método IEnumTime::Next

\[As interfaces e controles de Conferência de Telefonia IP de reunião não estão disponíveis para uso no Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. A API do Cliente RTC fornece funcionalidade semelhante.\]

O **método Next** obtém o próximo número especificado de elementos na sequência de enumeração.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Next(
  [in]  ULONG  celt,
  [out] ITTime **pVal,
  [out] ULONG  *pceltFetched
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ao mesmo tempo* \[ Em\]
</dt> <dd>

Número de elementos solicitados.

</dd> <dt>

*pVal* \[ out\]
</dt> <dd>

Ponteiro para a interface [**ITTime.**](ittime.md)

</dd> <dt>

*pceltFetched* \[ out\]
</dt> <dd>

Ponteiro para o número de elementos realmente fornecidos. Pode ser **NULL** *se o valor for* 1.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Valor                                                                                     | Significado                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | O método *retornou o número* máximo de elementos.<br/>         |
| <dl> <dt>**S \_ FALSE**</dt> </dl>   | O número de elementos restantes era menor que *o número de*.<br/> |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl> | O *parâmetro pVal* não é um ponteiro válido.<br/>       |



 

## <a name="remarks"></a>Comentários

TAPI chama o **método AddRef** na interface [**ITTime**](ittime.md) retornada por **IEnumTime::Next.** O aplicativo deve chamar **Release** na interface **ITTime** para liberar recursos associados a ele.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 3.0 ou posterior<br/>                                                 |
| Cabeçalho<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IEnumTime**](ienumtime.md)
</dt> </dl>

 

 




