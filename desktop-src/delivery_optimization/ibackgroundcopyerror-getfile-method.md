---
title: Método GetFile IBackgroundCopyError (Deliveryoptimization. h)
description: Recupera um ponteiro de interface para o objeto de arquivo associado ao erro.
ms.assetid: 7E1DB3EE-0690-4D0E-BA98-70F5FBDCF12F
keywords:
- Método GetFile
- Método GetFile, interface IBackgroundCopyError
- Interface IBackgroundCopyError, método GetFile
topic_type:
- apiref
api_name:
- IBackgroundCopyError.GetFile
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fbed5497bcebb3518c7f6a56646976cc01fbfebc501af4a08e861139311f4bc1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096706"
---
# <a name="ibackgroundcopyerrorgetfile-method"></a>Método IBackgroundCopyError:: GetFile

Recupera um ponteiro de interface para o objeto de arquivo associado ao erro.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetFile(
  [out] IBackgroundCopyFile **ppFile
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppFile* \[ fora\]
</dt> <dd>

Um ponteiro de interface [**IBackgroundCopyFile**](ibackgroundcopyfile.md) cujos métodos você usa para determinar os nomes de arquivo local e remoto associados ao erro. O parâmetro *ppFile* será definido como **NULL** se o erro não estiver associado ao arquivo local ou remoto. Quando terminar, libere *ppFile*.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna os valores de **HRESULT** a seguir.



| Código de retorno                                                                                                | Descrição                                                                                                    |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl>                   | Um ponteiro de interface foi recuperado com êxito para o objeto de arquivo.<br/>                                     |
| <dl> <dt>**DO_E_FILE_NOT_AVAILABLE**</dt> </dl> | O erro não está associado a um arquivo local ou remoto. O parâmetro *ppFile* está definido como **NULL**.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, \[ somente aplicativos da área de trabalho da versão 1709\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Servidor, versão 1709 \[ aplicativos da área de trabalho\]<br/>                                       |
| Cabeçalho<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyError é definido como 19C613A0-FCB8-4F28-81AE-897C3D078F81<br/>             |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IBackgroundCopyError**](ibackgroundcopyerror.md)
</dt> <dt>

[**IBackgroundCopyError:: GetError**](ibackgroundcopyerror-geterror-method.md)
</dt> </dl>

 

 





