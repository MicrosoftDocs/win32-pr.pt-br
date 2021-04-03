---
description: A função createprotocol notifica Monitor de Rede de que existe um analisador de protocolo específico.
ms.assetid: 13ae261f-b1c0-4afc-b718-d64b3d4ec5ee
title: Função createprotocol (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateProtocol
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 0b35f9505758256750ae02d24d6c2a84ed0646b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091725"
---
# <a name="createprotocol-function"></a>Função createprotocol

A função **createprotocol** notifica monitor de rede de que existe um analisador de protocolo específico.

## <a name="syntax"></a>Sintaxe


```C++
HPROTOCOL WINAPI CreateProtocol(
  _In_ LPSTR         ProtocolName,
  _In_ LPENTRYPOINTS lpEntryPoints,
  _In_ DWORD         cbEntryPoints
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ProtocolName* \[ no\]
</dt> <dd>

Nome do protocolo que o analisador detectará.

</dd> <dt>

*lpEntryPoints* \[ no\]
</dt> <dd>

Uma estrutura de [entryPoints](entrypoints.md) que contém os pontos de entrada da dll do analisador restante. Consulte comentários para obter uma lista das funções de exportação às quais cada ponto de entrada faz referência. Os pontos de entrada devem ser fornecidos na ordem que a estrutura de **entryPoints** especifica.

</dd> <dt>

*cbEntryPoints* \[ no\]
</dt> <dd>

O tamanho da estrutura de **entryPoints** . Monitor de Rede fornece uma \_ macro de tamanho de entryPoints que você pode usar para especificar o tamanho da estrutura.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será um identificador para o protocolo.

Se a função não for bem-sucedida, o valor de retorno será **nulo**.

## <a name="remarks"></a>Comentários

A DLL do analisador chama **createprotocol** durante sua implementação de [DllMain](dllmain-parser.md). A função **createprotocol** é chamada quando o sistema operacional carrega a DLL do analisador pela primeira vez.

Os pontos de entrada referenciados no parâmetro *lpEntryPoints* incluem ponteiros para as seguintes funções de exportação que devem ser fornecidas na ordem apresentada aqui.

-   [Registrar](register-parser.md)
-   [Cancelar registro](deregister.md)
-   [RecognizeFrame](recognizeframe.md)
-   [Anexarproperties](attachproperties.md)
-   [Formatproperties](formatproperties.md)



| Para obter informações sobre                                                                                 | Consulte                                                     |
|----------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| Quais analisadores são e como eles funcionam com Monitor de Rede.                                          | [Analisadores](parsers.md)                                  |
| Como implementar **DllMain** inclui um exemplo de chamada de **createprotocol** em **DllMain**. | [Implementando DllMain](implementing-dllmain-parser.md) |



 

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

[DllMain](/windows/desktop/Dlls/dllmain)
</dt> </dl>

 

