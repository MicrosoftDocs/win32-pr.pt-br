---
title: Método IEnumBackgroundCopyFiles Skip (Deliveryoptimization. h)
description: Ignora o próximo número especificado de elementos na sequência de enumeração. Se houver menos elementos à esquerda na sequência do que o número solicitado de elementos a serem ignorados, ele ignorará o último elemento na sequência.
ms.assetid: B01D4292-6BA5-4171-928B-AB2C555E2C2A
keywords:
- Método Skip
- Método Skip, interface IEnumBackgroundCopyFiles
- Interface IEnumBackgroundCopyFiles, método Skip
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles.Skip
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 174b8ac3e0286a4d2a19e211773969d408c7f7762e8b2dd4fe743f0b4b2aabeb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119567356"
---
# <a name="ienumbackgroundcopyfilesskip-method"></a>Método IEnumBackgroundCopyFiles:: Skip

Ignora o próximo número especificado de elementos na sequência de enumeração. Se houver menos elementos à esquerda na sequência do que o número solicitado de elementos a serem ignorados, ele ignorará o último elemento na sequência.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*celt* \[ no\]
</dt> <dd>

Número de elementos a serem ignorados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna os valores **HRESULT** a seguir, bem como outros.



| Código de retorno                                                                              | Descrição                                                       |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl> | O número de elementos solicitados foi ignorado com êxito.<br/> |
| <dl> <dt>**S_FALSE**</dt> </dl>  | Ignorado menos que o número de elementos solicitados.<br/>    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, \[ somente aplicativos da área de trabalho da versão 1709\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Servidor, versão 1709 \[ aplicativos da área de trabalho\]<br/>                                       |
| Cabeçalho<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IEnumBackgroundCopyFiles é definido como CA51E165-C365-424C-8D41-24AAA4FF3C40<br/>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





