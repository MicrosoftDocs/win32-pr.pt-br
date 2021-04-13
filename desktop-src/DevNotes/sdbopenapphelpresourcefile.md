---
description: Carrega o arquivo de recurso AppHelp.
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
ms.openlocfilehash: 2f1dfb1695e25bfb82e01ffa4f9eac4e245a6ffa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370429"
---
# <a name="sdbopenapphelpresourcefile-function"></a>Função SdbOpenApphelpResourceFile

Carrega o arquivo de recurso AppHelp.

## <a name="syntax"></a>Sintaxe


```C++
HMODULE WINAPI SdbOpenApphelpResourceFile(
  _In_opt_ LPCWSTR pwszACResourceFile
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pwszACResourceFile* \[ em, opcional\]
</dt> <dd>

O caminho para o arquivo de recurso. Se esse parâmetro for **NULL**, a DLL de recurso local será aberta.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

A função retorna um identificador para o arquivo de recurso aberto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




