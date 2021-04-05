---
title: Método GetError IBackgroundCopyError (Deliveryoptimization. h)
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
ms.openlocfilehash: e14803c225ade6085658582e18b9ba2d52fc90c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918358"
---
# <a name="ibackgroundcopyerrorgeterror-method"></a>Método IBackgroundCopyError:: GetError

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

*pContext* \[ fora\]
</dt> <dd>

Contexto no qual o erro ocorreu. Para obter uma lista de valores de contexto, consulte a enumeração [**BG_ERROR_CONTEXT**](bg-error-context.md) .

</dd> <dt>

*pErrorCode* \[ fora\]
</dt> <dd>

Código de erro do erro que ocorreu.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna **S_OK** em caso de êxito ou um dos valores padrão com HRESULT em erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]<br/>                                       |
| parâmetro<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyError é definido como 19C613A0-FCB8-4F28-81AE-897C3D078F81<br/>             |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IBackgroundCopyError**](ibackgroundcopyerror.md)
</dt> <dt>

[**IBackgroundCopyError:: GetFile**](ibackgroundcopyerror-getfile-method.md)
</dt> </dl>

 

 





