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
ms.openlocfilehash: 098e79ab49373dc115189a2c47dc3604fba10ef9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752323"
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

 

 




