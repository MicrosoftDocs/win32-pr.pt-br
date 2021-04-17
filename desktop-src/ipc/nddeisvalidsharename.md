---
description: Determina se um nome de compartilhamento usa a sintaxe apropriada.
ms.assetid: 4ffcff5d-0db5-4761-a31a-acefd2b8d9e2
title: Função NDdeIsValidShareName (Nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeIsValidShareName
- NDdeIsValidShareNameA
- NDdeIsValidShareNameW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: cbe1b7ead2d6f8e2d315833c44b354c50cc8b62c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780211"
---
# <a name="nddeisvalidsharename-function"></a>Função NDdeIsValidShareName

\[Não há mais suporte para DDE de rede. Nddeapi.dll está presente no Windows Vista, mas todas as chamadas de função retornam NDDE \_ não \_ implementado.\]

Determina se um nome de compartilhamento usa a sintaxe apropriada.

## <a name="syntax"></a>Sintaxe


```C++
BOOL NDdeIsValidShareName(
  _In_ LPTSTR shareName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ShareName* \[ no\]
</dt> <dd>

O nome do compartilhamento a ser validado. Este parâmetro não pode ser **nulo**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o nome do compartilhamento tiver uma sintaxe válida, o valor de retorno será diferente de zero.

Se o nome do compartilhamento não tiver uma sintaxe válida, o valor de retorno será zero.

## <a name="remarks"></a>Comentários

Essa função também é chamada por [**NDdeShareAdd**](nddeshareadd.md) quando cria o compartilhamento DDE.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Cabeçalho<br/>                   | <dl> <dt>Nddeapi. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Nddeapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **NDdeIsValidShareNameW** (Unicode) e **NDdeIsValidShareNameA** (ANSI)<br/>    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral de troca dinâmica de dados de rede](network-dynamic-data-exchange.md)
</dt> <dt>

[Funções DDE de rede](network-dde-functions.md)
</dt> <dt>

[**NDdeShareAdd**](nddeshareadd.md)
</dt> </dl>

 

 




