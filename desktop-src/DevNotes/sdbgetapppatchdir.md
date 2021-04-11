---
description: Recupera o diretório AppPatch do sistema.
ms.assetid: 1c79411f-1f90-4b90-84c7-24a34cf0d91d
title: Função SdbGetAppPatchDir
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetAppPatchDir
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 60a3b14bcca1be3ecb8d33b0d3f344f08bc11b28
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088816"
---
# <a name="sdbgetapppatchdir-function"></a>Função SdbGetAppPatchDir

Recupera o diretório AppPatch do sistema.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI SdbGetAppPatchDir(
  _In_opt_ HSDB   hSDB,
  _Out_    LPTSTR szAppPatchPath,
  _In_     DWORD  cchSize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hSDB* \[ em, opcional\]
</dt> <dd>

Um identificador para o banco de dados de Shim retornado pela função [**SdbInitDatabase**](sdbinitdatabase.md) .

</dd> <dt>

*szAppPatchPath* \[ fora\]
</dt> <dd>

O caminho resultante.

</dd> <dt>

*cchSize* \[ no\]
</dt> <dd>

O tamanho do buffer *szAppPatchPath* , em caracteres. Se a função falhar, esse parâmetro será definido como a cadeia de caracteres vazia ("").

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SdbInitDatabase**](sdbinitdatabase.md)
</dt> </dl>

 

 




