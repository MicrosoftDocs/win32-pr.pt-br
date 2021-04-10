---
description: O método CreateObject do objeto Microsoft. Windows. ActCtx cria um objeto no contexto do manifesto atual.
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
ms.openlocfilehash: 2b4c4393d59ea5ab711dbf4bb1f4c88d906b6582
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170033"
---
# <a name="actctxcreateobject-method"></a>Método ActCtx. CreateObject

O método **CreateObject** do objeto [**Microsoft. Windows. ActCtx**](microsoft-windows-actctx-object.md) cria um objeto no contexto do manifesto atual.

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

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Sxsoa.dll</dt> </dl> |
| IID<br/>                      | IID \_ IActCtx é definido como 8FA7728F-B69B-4EE5-99F2-E2AA021BEF28<br/>           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Método GetObject**](getobject.md)
</dt> </dl>

 

 




