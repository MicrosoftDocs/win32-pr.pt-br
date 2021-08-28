---
description: O método GetObject Obtém uma instância de uma Microsoft existente. Windows. Objeto ActCtx.
ms.assetid: 547525f3-afef-463b-823a-df8ccd954f36
title: Método ActCtx. GetObject
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ActCtx.GetObject
api_type:
- COM
api_location:
- Sxsoa.dll
ms.openlocfilehash: b6c47c00f50cdeaa97fd0fafcd8aefa3c4863bc1
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886606"
---
# <a name="actctxgetobject-method"></a>Método ActCtx. GetObject

O método **GetObject** Obtém uma instância de um [**Microsoft. Windows existente. Objeto ActCtx**](microsoft-windows-actctx-object.md) .

## <a name="syntax"></a>Sintaxe


```JScript
ActCtx.GetObject(
  bstrName
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrName* 
</dt> <dd>

Cadeia de caracteres necessária que indica o objeto. o nome deve estar no registro em **HKEY \_ LOCAL \_ MACHINE** \\ **Microsoft** \\ **Visual Studio** \\ **6,0** \\ **&lt; package &gt;** \\ **Automation**.

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

[**Método CreateObject**](createobject.md)
</dt> </dl>

 

 




