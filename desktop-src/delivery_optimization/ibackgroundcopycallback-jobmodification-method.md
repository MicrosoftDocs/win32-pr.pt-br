---
title: Método IBackgroundCopyCallback JobModification (Deliveryoptimization. h)
description: A otimização de entrega (DO) chama sua implementação do método JobModification quando o trabalho foi modificado.
ms.assetid: 4AC2575F-57FB-45E6-B29C-12DF615237F3
keywords:
- Método JobModification
- Método JobModification, interface IBackgroundCopyCallback
- Interface IBackgroundCopyCallback, método JobModification
topic_type:
- apiref
api_name:
- IBackgroundCopyCallback.JobModification
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ceeb390fc8592c1e8e1d03efdb432056bd131a6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105812092"
---
# <a name="ibackgroundcopycallbackjobmodification-method"></a>Método IBackgroundCopyCallback:: JobModification

A otimização de entrega (DO) chama sua implementação do método [**JobModification**](https://www.bing.com/search?q=**JobModification**) quando o trabalho foi modificado. O serviço gera esse evento quando bytes são transferidos, os arquivos foram adicionados ao trabalho, as propriedades foram modificadas ou o estado do trabalho foi alterado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT JobModification(
  [in] IBackgroundCopyJob *pJob,
  [in] DWORD              dwReserved
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pJob* \[ no\]
</dt> <dd>

Contém os métodos para acessar informações de propriedade, progresso e estado do trabalho. Não liberar *pJob*; Libera a interface quando o método [**JobModification**](https://www.bing.com/search?q=**JobModification**) retorna.

</dd> <dt>

*dwReserved* \[ no\]
</dt> <dd>

Reservado para uso futuro.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método deve retornar S_OK.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]<br/>                                       |
| parâmetro<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyCallback é definido como 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22<br/>          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IBackgroundCopyCallback**](ibackgroundcopycallback.md)
</dt> <dt>

[**Método ibackgroundcopyjob**](ibackgroundcopyjob-.md)
</dt> </dl>

 

 





