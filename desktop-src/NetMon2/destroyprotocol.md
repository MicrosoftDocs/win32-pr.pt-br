---
description: A função DestroyProtocol destrói o protocolo criado pela função createprotocol.
ms.assetid: f7621c2a-1905-4748-b8e3-7b49f3f2bf03
title: Função DestroyProtocol (Netmon. h)
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
ms.openlocfilehash: be96a13816a6a35bdd554380dacd5e8e2f5d5450
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169376"
---
# <a name="destroyprotocol-function"></a>Função DestroyProtocol

A função **DestroyProtocol** destrói o protocolo criado pela função **createprotocol** .

## <a name="syntax"></a>Sintaxe


```C++
VOID WINAPI DestroyProtocol(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hProtocol* \[ no\]
</dt> <dd>

Identificador para o protocolo a ser destruído.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Nenhum.

## <a name="remarks"></a>Comentários

A DLL do analisador chama a função **DestroyProtocol** durante sua implementação de [DllMain](dllmain-parser.md). **DestroyProtocol** é chamado quando o sistema operacional vai descarregar a dll.



| Para obter informações sobre                                        | Consulte                                                     |
|-----------------------------------------------------------|---------------------------------------------------------|
| Quais analisadores são e como eles funcionam com Monitor de Rede. | [Analisadores](parsers.md)                                  |
| A implementação de **DllMain** inclui um exemplo.         | [Implementando DllMain](implementing-dllmain-parser.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[DllMain](dllmain-parser.md)
</dt> </dl>

 

 




