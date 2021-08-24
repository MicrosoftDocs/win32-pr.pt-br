---
description: A função BuildINIPath retorna um caminho totalmente qualificado para um arquivo INI que corresponde às informações que você inserir.
ms.assetid: 214ce89c-8bb2-4e1a-872a-026743a3e3a6
title: Função BuildINIPath (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BuildINIPath
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: b75df338142ab0ec97db3e60cbba1b5f68df3e0e67947d4c13cdccccd409bdf8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744686"
---
# <a name="buildinipath-function"></a>Função BuildINIPath

A **função BuildINIPath** retorna um caminho totalmente qualificado para um arquivo INI que corresponde às informações que você inserir.

## <a name="syntax"></a>Sintaxe


```C++
LPSTR BuildINIPath(
   char *FullPath,
   char *IniFileName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*FullPath* 
</dt> <dd>

Buffer que recebe o nome de arquivo INI totalmente qualificado.

</dd> <dt>

*IniFileName* 
</dt> <dd>

Nome do arquivo INI (o nome completo do arquivo menos a extensão filename).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será um ponteiro para o nome de arquivo INI totalmente qualificado.

Se a função não for bem-sucedida, o valor de retorno será **NULL.**

## <a name="remarks"></a>Comentários

O caminho que essa função retorna é um caminho totalmente qualificado para um arquivo INI que corresponde às informações que você inserir. Por exemplo, se você inserir XNS ou TCP, a função gerará um caminho para Xns.ini ou Tcp.ini, respectivamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                            |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Parser.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




