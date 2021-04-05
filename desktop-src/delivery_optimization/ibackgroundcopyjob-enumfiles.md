---
title: Método método ibackgroundcopyjob EnumFiles (Deliveryoptimization. h)
description: Recupera um ponteiro de interface IEnumBackgroundCopyFiles que você usa para enumerar os arquivos em um trabalho.
ms.assetid: 94FA5D7B-08C1-497E-9813-571D35AE3BCF
keywords:
- Método EnumFiles
- Método EnumFiles, interface método ibackgroundcopyjob
- Interface método ibackgroundcopyjob, método EnumFiles
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
ms.openlocfilehash: a4b0315f98594357d67fd5dbfed3bf2561f41f71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085687"
---
# <a name="ibackgroundcopyjobenumfiles-method"></a>Método método ibackgroundcopyjob:: EnumFiles

Recupera um ponteiro de interface [**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md) que você usa para enumerar os arquivos em um trabalho.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT EnumFiles(
  [out] IEnumBackgroundCopyFiles **ppEnumFiles
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppEnumFiles* \[ fora\]
</dt> <dd>

Ponteiro de interface [**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md) que você usa para enumerar os arquivos no trabalho. Libere *ppEnumFiles* quando terminar.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna **S_OK** em caso de êxito ou um dos valores padrão com **HRESULT** em erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]<br/>                                       |
| parâmetro<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob é definido como 37668D37-507E-4160-9316-26306D150B12<br/>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Método ibackgroundcopyjob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





