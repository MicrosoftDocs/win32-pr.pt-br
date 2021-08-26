---
description: Carrega o arquivo de recurso Apphelp.
ms.assetid: fca50e00-9324-410a-a572-69441f332593
title: Função SdbOpenApphelpResourceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbOpenApphelpResourceFile
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: ab865a29e0879119ca50cf4177aa7649bd82a83e70c07e1b7068a5d8fcd2cc30
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044986"
---
# <a name="sdbopenapphelpresourcefile-function"></a>Função SdbOpenApphelpResourceFile

Carrega o arquivo de recurso Apphelp.

## <a name="syntax"></a>Sintaxe


```C++
HMODULE WINAPI SdbOpenApphelpResourceFile(
  _In_opt_ LPCWSTR pwszACResourceFile
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pwszACResourceFile* \[ in, opcional\]
</dt> <dd>

O caminho para o arquivo de recurso. Se esse parâmetro for **NULL,** a DLL do recurso local será aberta.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

A função retorna um handle para o arquivo de recurso aberto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




