---
description: Obtém a ID da interface de uma referência agile a um objeto .
ms.assetid: 627A7EE4-CFEF-47F6-BA99-51BEB78C5D55
title: Método IAgileReference::Resolve
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAgileReference.Resolve
api_type:
- COM
api_location:
- objidl.h
ms.openlocfilehash: 0b58013ba81bb394715a0042f3f3d7435a381fa01f5b985bd9ad81d12122441e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758767"
---
# <a name="iagilereferenceresolve-method"></a>Método IAgileReference::Resolve

Obtém a ID da interface de uma referência agile a um objeto .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Resolve(
  [in]          REFIID riid,
  [out, retval] void   **ppvObjectReference
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*riid* \[ Em\]
</dt> <dd>

A ID da interface a ser recuperada da referência agile. Não é necessário ser o mesmo que a interface registrada.

</dd> <dt>

*ppvObjectReference* \[ out, retval\]
</dt> <dd>

Após a conclusão \* *bem-sucedida, ppvObjectReference é* um ponteiro para a interface especificada por *riid.*

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Valor retornado                                                                              | Descrição                                                                    |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> </dl>          | O método foi concluído com êxito.<br/>                                  |
| <dl> <dt>E \_ NOINTERFACE</dt> </dl> | A interface solicitada não é implementada no objeto registrado.<br/> |



 

## <a name="remarks"></a>Comentários

Chame a [**função RoGetAgileReference**](/windows/desktop/api/ComBaseApi/nf-combaseapi-rogetagilereference) para criar uma referência agile a um objeto . Chame o **método Resolve** para localizador o objeto no apartment no qual **Resolve** é chamado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8.1 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>            |
| Servidor mínimo com suporte<br/> | Windows Server 2012 Aplicativos UWP de aplicativos da área \[ de trabalho \| R2\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IAgileReference**](/windows/desktop/api/objidl/nn-objidl-iagilereference)
</dt> <dt>

[**RoGetAgileReference**](/windows/desktop/api/ComBaseApi/nf-combaseapi-rogetagilereference)
</dt> </dl>

 

 




