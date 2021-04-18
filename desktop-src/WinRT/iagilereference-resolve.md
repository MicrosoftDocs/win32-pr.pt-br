---
description: Obtém a ID da interface de uma referência ágil a um objeto.
ms.assetid: 627A7EE4-CFEF-47F6-BA99-51BEB78C5D55
title: 'Método IAgileReference:: resolve'
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
ms.openlocfilehash: 1c3ac95802a44f4305abb24566744ad98c67b174
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765779"
---
# <a name="iagilereferenceresolve-method"></a>Método IAgileReference:: resolve

Obtém a ID da interface de uma referência ágil a um objeto.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Resolve(
  [in]          REFIID riid,
  [out, retval] void   **ppvObjectReference
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*riid* \[ no\]
</dt> <dd>

A ID da interface a ser recuperada da referência ágil. Não é necessário ser o mesmo que a interface registrada.

</dd> <dt>

*ppvObjectReference* \[ out, retval\]
</dt> <dd>

Após a conclusão bem-sucedida, \* *ppvObjectReference* é um ponteiro para a interface especificada por *riid*.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Valor retornado                                                                              | Descrição                                                                    |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> </dl>          | O método foi concluído com êxito.<br/>                                  |
| <dl> <dt>E \_ NOinterface</dt> </dl> | A interface solicitada não está implementada no objeto registrado.<br/> |



 

## <a name="remarks"></a>Comentários

Chame a função [**RoGetAgileReference**](/windows/desktop/api/ComBaseApi/nf-combaseapi-rogetagilereference) para criar uma referência ágil a um objeto. Chame o método **resolve** para localizar o objeto no apartamento no qual **resolve** é chamado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]<br/>            |
| Servidor mínimo com suporte<br/> | \[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IAgileReference**](/windows/desktop/api/objidl/nn-objidl-iagilereference)
</dt> <dt>

[**RoGetAgileReference**](/windows/desktop/api/ComBaseApi/nf-combaseapi-rogetagilereference)
</dt> </dl>

 

 




