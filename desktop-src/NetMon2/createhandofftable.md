---
description: A função CreateHandoffTable cria uma tabela de entrega que inclui as informações do conjunto de entrega armazenadas no arquivo INI do analisador.
ms.assetid: 6dbca2fa-33fb-48e8-b663-be59aec6264b
title: Função CreateHandoffTable (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateHandoffTable
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 70709223d5dcebcae819389feb8623006b793126a911fc674491b1d665268056
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911196"
---
# <a name="createhandofftable-function"></a>Função CreateHandoffTable

A **função CreateHandoffTable** cria uma tabela [*de*](h.md) entrega que inclui as informações do conjunto de entrega armazenadas no arquivo INI do analisador.

## <a name="syntax"></a>Sintaxe


```C++
DWORD WINAPI CreateHandoffTable(
  _In_  LPSTR          secName,
  _In_  LPSTR          iniFile,
  _Out_ LPHANDOFFTABLE *hTable,
  _In_  DWORD          nMaxProtocolEntries,
  _In_  DWORD          base
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*secName* \[ Em\]
</dt> <dd>

Cadeia de caracteres que indica a seção do arquivo INI em que as informações do conjunto de entrega estão localizadas.

</dd> <dt>

*iniFile* \[ Em\]
</dt> <dd>

Cadeia de caracteres que inclui o nome do arquivo INI do analisador.

</dd> <dt>

*hTable* \[ out\]
</dt> <dd>

Lidar com uma **estrutura HANDOFFTABLE** criada e mantida por Monitor de Rede.

</dd> <dt>

*nMaxProtocolEntries* \[ Em\]
</dt> <dd>

Número que especifica o número máximo de entradas que a tabela de entrega pode processar.

</dd> <dt>

*base* \[ Em\]
</dt> <dd>

Base numérica de números de conjunto de entrega armazenados no arquivo INI.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será o número de entradas na tabela de entrega.

Se a função não for bem-sucedida, o valor de retorno será zero.

## <a name="remarks"></a>Comentários

A tabela de entrega criada por Monitor de Rede é baseada nas informações fornecidas no INI do analisador. O alça retornado para a tabela de entrega pode ser usado para obter um alça para um dos protocolos incluídos na tabela. Para obter um handle de um desses protocolos, chame [GetProtocolFromTable](getprotocolfromtable.md).

Observe que o aplicativo analisador nunca acessa a estrutura **HANDOFFTABLE** diretamente. Essa estrutura é criada e mantida por Monitor de Rede.

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

[GetProtocolFromTable](getprotocolfromtable.md)
</dt> <dt>

[HANDOFFTABLE](handofftable.md)
</dt> </dl>

 

 




