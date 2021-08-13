---
title: Método GetCount IEnumBackgroundCopyFiles (Deliveryoptimization.h)
description: Recupera uma contagem do número de arquivos na enumeração .
ms.assetid: EE27679D-3AC0-49DA-992F-8DEA10C21646
keywords:
- Método GetCount
- Método GetCount, interface IEnumBackgroundCopyFiles
- Interface IEnumBackgroundCopyFiles, método GetCount
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles.GetCount
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f67ee932079a7c67619fe769cbe5d1b6705261655853f1adccb14bf5d12eecf2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119409906"
---
# <a name="ienumbackgroundcopyfilesgetcount-method"></a>Método IEnumBackgroundCopyFiles::GetCount

Recupera uma contagem do número de arquivos na enumeração .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetCount(
  [out] ULONG *pCount
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pCount* \[ out\]
</dt> <dd>

Número de arquivos na enumeração.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna **S_OK** em caso de êxito ou um dos valores padrão do COM **HRESULT** em caso de erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1709 somente para \[ aplicativos da área de trabalho\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Servidor, versão 1709 somente \[ aplicativos da área de trabalho\]<br/>                                       |
| parâmetro<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IEnumBackgroundCopyFiles é definido como CA51E165-C365-424C-8D41-24AAA4FF3C40<br/>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





