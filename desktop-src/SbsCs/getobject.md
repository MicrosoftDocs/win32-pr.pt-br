---
description: O método GetObject Obtém uma instância de um objeto Microsoft. Windows. ActCtx existente.
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
ms.openlocfilehash: 11b71d8d40d947472612c91f70e9956aa7798806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647015"
---
# <a name="actctxgetobject-method"></a>Método ActCtx. GetObject

O método **GetObject** Obtém uma instância de um objeto [**Microsoft. Windows. ActCtx**](microsoft-windows-actctx-object.md) existente.

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

Cadeia de caracteres necessária que indica o objeto. O nome deve estar no registro em **HKEY \_ local \_ Machine** \\ **Microsoft** \\ **Visual Studio** \\ **6,0** \\ **<package>** \\ **Automation**.

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

[**Método CreateObject**](createobject.md)
</dt> </dl>

 

 




