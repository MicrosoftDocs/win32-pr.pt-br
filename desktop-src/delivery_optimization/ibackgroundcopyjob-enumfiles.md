---
title: Método IBackgroundCopyJob EnumFiles (Deliveryoptimization.h)
description: Recupera um ponteiro de interface IEnumBackgroundCopyFiles que você usa para enumerar os arquivos em um trabalho.
ms.assetid: 94FA5D7B-08C1-497E-9813-571D35AE3BCF
keywords:
- Método EnumFiles
- Método EnumFiles, interface IBackgroundCopyJob
- Interface IBackgroundCopyJob, método EnumFiles
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.EnumFiles
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4ecd27e1de8dfaa16d7f5d2dc3218d3c993148a0878976e329b4953cefdc4c29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543012"
---
# <a name="ibackgroundcopyjobenumfiles-method"></a>Método IBackgroundCopyJob::EnumFiles

Recupera um ponteiro de interface [**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md) que você usa para enumerar os arquivos em um trabalho.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT EnumFiles(
  [out] IEnumBackgroundCopyFiles **ppEnumFiles
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppEnumFiles* \[ out\]
</dt> <dd>

Ponteiro de interface [**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md) que você usa para enumerar os arquivos no trabalho. Libere *ppEnumFiles* quando terminar.

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
| IID<br/>                      | IID_IBackgroundCopyJob é definido como 37668D37-507E-4160-9316-26306D150B12<br/>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





