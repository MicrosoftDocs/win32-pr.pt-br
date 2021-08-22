---
description: Método IEnumMedia::Next – o método Next obtém o próximo número especificado de elementos na sequência de enumeração.
ms.assetid: 39c6d082-415f-4375-8cad-6d4c734d277f
title: Método IEnumMedia::Next (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c526ce608066f8b3e67affb10bd777042d0d2e93cf02887ba5bfd49a744e931a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118865926"
---
# <a name="ienummedianext-method"></a>Método IEnumMedia::Next

\[As interfaces e controles de Conferência de Telefonia IP de reunião não estão disponíveis para uso no Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. A API do Cliente RTC fornece funcionalidade semelhante.\]

O **método Next** obtém o próximo número especificado de elementos na sequência de enumeração.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Next(
  [in]  ULONG   celt,
  [out] ITMedia **pVal,
  [out] ULONG   *pceltFetched
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

Ponteiro para a interface [**ITMedia.**](itmedia.md)

</dd> <dt>

*pceltFetched* \[ out\]
</dt> <dd>

Ponteiro para o número de elementos realmente fornecidos. Pode ser **NULL** *se o valor for* um.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Valor                                                                                     | Significado                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | O método *retornou o número* máximo de elementos.<br/>         |
| <dl> <dt>**S \_ FALSE**</dt> </dl>   | O número de elementos restantes era menor que *o número de*.<br/> |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl> | O *parâmetro pVal* não é um ponteiro válido.<br/>       |



 

## <a name="remarks"></a>Comentários

TAPI chama o **método AddRef** na interface [**ITMedia**](itmedia.md) retornada **por IEnumMedia::Next.** O aplicativo deve chamar **Release** na interface **ITMedia** para liberar recursos associados a ele.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 3.0 ou posterior<br/>                                                 |
| Cabeçalho<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IEnumMedia**](ienummedia.md)
</dt> </dl>

 

 




