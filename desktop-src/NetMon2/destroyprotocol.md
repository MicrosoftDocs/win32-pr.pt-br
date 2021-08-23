---
description: A função DestroyProtocol destrói o protocolo que a função CreateProtocol cria.
ms.assetid: f7621c2a-1905-4748-b8e3-7b49f3f2bf03
title: Função DestroyProtocol (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyProtocol
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2c3a89bfd74a01a7455ecd9393d913ddd906474ceabd1c8884f187444cb483a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911136"
---
# <a name="destroyprotocol-function"></a>Função DestroyProtocol

A **função DestroyProtocol** destrói o protocolo que a **função CreateProtocol** cria.

## <a name="syntax"></a>Sintaxe


```C++
VOID WINAPI DestroyProtocol(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hProtocol* \[ Em\]
</dt> <dd>

Lidar com o protocolo a ser destruído.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Nenhum.

## <a name="remarks"></a>Comentários

A DLL do analisador chama a **função DestroyProtocol** durante sua implementação de [DllMain.](dllmain-parser.md) **DestroyProtocol** é chamado quando o sistema operacional vai descarregar a DLL.



| Para obter informações sobre                                        | Consulte                                                     |
|-----------------------------------------------------------|---------------------------------------------------------|
| O que são analisadores e como eles funcionam com Monitor de Rede. | [Analisadores](parsers.md)                                  |
| Como implementar **o DllMain** inclui um exemplo.         | [Implementando DllMain](implementing-dllmain-parser.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Dllmain](dllmain-parser.md)
</dt> </dl>

 

 




