---
title: Método de redefinição de IEnumBackgroundCopyFiles (Deliveryoptimization. h)
description: 'Método IEnumBackgroundCopyFiles:: Reset – redefine a sequência de enumeração para o início.'
ms.assetid: 6A303069-105C-4053-A8C5-2ECF60E789DE
keywords:
- Método Reset
- Método Reset, interface IEnumBackgroundCopyFiles
- Interface IEnumBackgroundCopyFiles, Método Reset
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles.Reset
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bcd0fc46d1106feb553c77727f979da1e3002dc2530f1bb37d8c345220c264b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118542003"
---
# <a name="ienumbackgroundcopyfilesreset-method"></a>Método IEnumBackgroundCopyFiles:: Reset

Redefine a sequência de enumeração para o início.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Reset();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método retorna **S_OK** em caso de êxito ou um dos valores padrão com **HRESULT** em erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, \[ somente aplicativos da área de trabalho da versão 1709\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Servidor, versão 1709 \[ aplicativos da área de trabalho\]<br/>                                       |
| parâmetro<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IEnumBackgroundCopyFiles é definido como CA51E165-C365-424C-8D41-24AAA4FF3C40<br/>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





