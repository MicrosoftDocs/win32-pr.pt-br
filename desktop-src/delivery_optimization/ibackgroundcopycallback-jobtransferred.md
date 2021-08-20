---
title: Método IBackgroundCopyCallback JobTransferred (Deliveryoptimization. h)
description: A otimização de entrega (DO) chama sua implementação do método JobTransferred quando todos os arquivos no trabalho foram transferidos com êxito.
ms.assetid: D3088279-2D26-4707-9BA2-19D2758EA1CC
keywords:
- Método JobTransferred
- Método JobTransferred, interface IBackgroundCopyCallback
- Interface IBackgroundCopyCallback, método JobTransferred
topic_type:
- apiref
api_name:
- IBackgroundCopyCallback.JobTransferred
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 69cf1a739e15bc7341769bdc01549ad439a1c93877f653f0689e686eb8bac1f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047094"
---
# <a name="ibackgroundcopycallbackjobtransferred-method"></a>Método IBackgroundCopyCallback:: JobTransferred

A otimização de entrega (DO) chama sua implementação do método **JobTransferred** quando todos os arquivos no trabalho foram transferidos com êxito.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT JobTransferred(
  [in] IBackgroundCopyJob *pJob
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pJob* \[ no\]
</dt> <dd>

Contém informações relacionadas ao trabalho, como a hora em que o trabalho foi concluído, o número de bytes transferidos e o número de arquivos transferidos. Não liberar *pJob*; Libera a interface quando o método retorna.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método deve retornar S_OK.

## <a name="remarks"></a>Comentários

Normalmente, sua implementação deve chamar o método [**método ibackgroundcopyjob:: Complete**](ibackgroundcopyjob-complete.md) para confirmar que o transferiu com êxito os arquivos. Baixar arquivos e o arquivo de resposta não estarão disponíveis no cliente até que você chame o método **Complete** .

Se você não chamar o método [**Complete**](ibackgroundcopyjob-complete.md) ou o método [**método ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md) , o cancelará o trabalho após 30 dias e excluirá os arquivos incompletos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, \[ somente aplicativos da área de trabalho da versão 1709\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Servidor, versão 1709 \[ aplicativos da área de trabalho\]<br/>                                       |
| Cabeçalho<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyCallback é definido como 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22<br/>          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IBackgroundCopyCallback**](ibackgroundcopycallback.md)
</dt> <dt>

[**Método ibackgroundcopyjob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**Método ibackgroundcopyjob:: concluir**](ibackgroundcopyjob-complete.md)
</dt> <dt>

[**Método ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md)
</dt> </dl>

 

 





