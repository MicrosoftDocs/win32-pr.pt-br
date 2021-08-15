---
description: A função CreateProtocol notifica Monitor de Rede que existe um analisador de protocolo específico.
ms.assetid: 13ae261f-b1c0-4afc-b718-d64b3d4ec5ee
title: Função CreateProtocol (Netmon.h)
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
ms.openlocfilehash: 173f744406ef2b360c0af7158e397c2001f146b9f2339bf6aaf3468b9a1465dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117796347"
---
# <a name="createprotocol-function"></a>Função CreateProtocol

A **função CreateProtocol** notifica Monitor de Rede que existe um analisador de protocolo específico.

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

*ProtocolName* \[ Em\]
</dt> <dd>

Nome do protocolo que o analisador detectará.

</dd> <dt>

*lpEntryPoints* \[ Em\]
</dt> <dd>

Uma [estrutura ENTRYPOINTS](entrypoints.md) que contém os pontos de entrada de DLL do analisador restantes. Consulte Comentários para ver uma lista das funções de exportação referenciadas por cada ponto de entrada. Os pontos de entrada devem ser fornecidos na ordem especificada pela estrutura **ENTRYPOINTS.**

</dd> <dt>

*cbEntryPoints* \[ Em\]
</dt> <dd>

O tamanho da estrutura **ENTRYPOINTS.** Monitor de Rede fornece uma macro ENTRYPOINTS SIZE que você pode \_ usar para especificar o tamanho da estrutura.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será um alçado para o protocolo.

Se a função não for bem-sucedida, o valor de retorno será **NULL.**

## <a name="remarks"></a>Comentários

A DLL do analisador chama **CreateProtocol** durante sua implementação [de DllMain](dllmain-parser.md). A **função CreateProtocol** é chamada quando o sistema operacional carrega a DLL do analisador pela primeira vez.

Os pontos de entrada referenciados no *parâmetro lpEntryPoints* incluem ponteiros para as seguintes funções de exportação que devem ser fornecidas na ordem apresentada aqui.

-   [Registrar](register-parser.md)
-   [Cancelar registro](deregister.md)
-   [RecognizeFrame](recognizeframe.md)
-   [AttachProperties](attachproperties.md)
-   [FormatProperties](formatproperties.md)



| Para obter informações sobre                                                                                 | Consulte                                                     |
|----------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| O que são analisadores e como eles funcionam com Monitor de Rede.                                          | [Analisadores](parsers.md)                                  |
| Como implementar **DllMain inclui** um exemplo de chamada **a CreateProtocol** em **DllMain**. | [Implementando DllMain](implementing-dllmain-parser.md) |



 

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

[Dllmain](/windows/desktop/Dlls/dllmain)
</dt> </dl>

 

