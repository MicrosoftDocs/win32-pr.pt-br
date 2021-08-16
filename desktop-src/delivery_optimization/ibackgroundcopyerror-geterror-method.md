---
title: Método GetError IBackgroundCopyError (Deliveryoptimization.h)
description: Recupera o código de erro e identifica o contexto no qual o erro ocorreu.
ms.assetid: C87897CD-9648-4CEF-B963-68EE35356929
keywords:
- Método GetError
- Método GetError, interface IBackgroundCopyError
- Interface IBackgroundCopyError, método GetError
topic_type:
- apiref
api_name:
- IBackgroundCopyError.GetError
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d147bc877f9694617ec94651f53f4cf438c00de8d752710c3659f24ba4ffe21c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118810320"
---
# <a name="ibackgroundcopyerrorgeterror-method"></a>Método IBackgroundCopyError::GetError

Recupera o código de erro e identifica o contexto no qual o erro ocorreu.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetError(
  [out] BG_ERROR_CONTEXT *pContext,
  [out] HRESULT          *pErrorCode
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pContext* \[ out\]
</dt> <dd>

Contexto no qual o erro ocorreu. Para ver uma lista de valores de contexto, [**consulte a enumeração BG_ERROR_CONTEXT**](bg-error-context.md) dados.

</dd> <dt>

*pErrorCode* \[ out\]
</dt> <dd>

Código de erro do erro que ocorreu.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna **S_OK** em caso de êxito ou um dos valores padrão do COM HRESULT em caso de erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1709 somente para \[ aplicativos da área de trabalho\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Servidor, versão 1709 somente \[ aplicativos da área de trabalho\]<br/>                                       |
| Cabeçalho<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyError é definido como 19C613A0-FCB8-4F28-81AE-897C3D078F81<br/>             |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IBackgroundCopyError**](ibackgroundcopyerror.md)
</dt> <dt>

[**IBackgroundCopyError::GetFile**](ibackgroundcopyerror-getfile-method.md)
</dt> </dl>

 

 





