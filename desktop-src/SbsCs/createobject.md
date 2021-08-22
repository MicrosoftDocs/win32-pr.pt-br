---
description: O método CreateObject do Microsoft. Windows. O objeto ActCtx cria um objeto no contexto do manifesto atual.
ms.assetid: 531e6501-bb68-472b-b483-1f52815ba9d7
title: Método ActCtx. CreateObject
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ActCtx.CreateObject
api_type:
- COM
api_location:
- Sxsoa.dll
ms.openlocfilehash: 4161ccdcc2562405123d8cb5276aa1f849121c0271b6c6e3f23a32551f6f3dda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142389"
---
# <a name="actctxcreateobject-method"></a>Método ActCtx. CreateObject

O método **CreateObject** do [**Microsoft. Windows.**](microsoft-windows-actctx-object.md)O objeto ActCtx cria um objeto no contexto do manifesto atual.

## <a name="syntax"></a>Sintaxe


```JScript
ActCtx.CreateObject(
  objectId
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*objectId* 
</dt> <dd>

Uma cadeia de caracteres que especifica o tipo de objeto a ser criado. Por exemplo, uma ProgID COM.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Sxsoa.dll</dt> </dl> |
| IID<br/>                      | IID \_ IActCtx é definido como 8FA7728F-B69B-4EE5-99F2-E2AA021BEF28<br/>           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Método GetObject**](getobject.md)
</dt> </dl>

 

 




