---
description: Recarrega as configurações de cor do registro.
ms.assetid: 1F2EE08A-4193-4F0C-BE4F-0551FA71CFA8
title: Função FRefreshStyle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRefreshStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 5c071d76712877650bba8ecf502687538bb6ac354e62a0285dc08e2f22f25873
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103686"
---
# <a name="frefreshstyle-function"></a>Função FRefreshStyle

Recarrega as configurações de cor do registro.

## <a name="syntax"></a>Sintaxe


```C++
BOOL __cdecl FRefreshStyle(void);
```



## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna verdadeiro em caso de êxito; caso contrário, FALSE.

## <a name="remarks"></a>Comentários

Esta função não está associada a uma biblioteca de importação ou arquivo de cabeçalho; Ele deve ser chamado usando as funções [**LoadLibrary**](-loadlibrary.md) e [**GetProcAddress**](-getprocaddress-.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Imeshare.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**GetProcAddress**](-getprocaddress-.md)
</dt> <dt>

[**LoadLibrary**](-loadlibrary.md)
</dt> </dl>

 

 




