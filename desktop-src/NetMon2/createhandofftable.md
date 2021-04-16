---
description: A função createentregatable cria uma tabela de entrega que inclui as informações de conjunto de entrega armazenadas no arquivo INI do analisador.
ms.assetid: 6dbca2fa-33fb-48e8-b663-be59aec6264b
title: Função createentregatable (Netmon. h)
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
ms.openlocfilehash: 450bb4e4b158a937d48d753a5ff5c831f8fa58c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750791"
---
# <a name="createhandofftable-function"></a>Função createentregatable

A função **Createentregatable** cria uma [*tabela de entrega*](h.md) que inclui as informações de conjunto de entrega armazenadas no arquivo ini do analisador.

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

*secName* \[ no\]
</dt> <dd>

Cadeia de caracteres que indica a seção do arquivo INI onde estão localizadas as informações do conjunto de entrega.

</dd> <dt>

*iniFile* \[ no\]
</dt> <dd>

Cadeia de caracteres que inclui o nome do arquivo INI do analisador.

</dd> <dt>

*hTable* \[ fora\]
</dt> <dd>

Identificador para uma estrutura de **entrega** criada e mantida pelo monitor de rede.

</dd> <dt>

*nMaxProtocolEntries* \[ no\]
</dt> <dd>

Número que especifica o número máximo de entradas que a tabela de entrega pode processar.

</dd> <dt>

*base* \[ no\]
</dt> <dd>

A base numérica dos números de conjunto de entrega armazenados no arquivo INI.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será o número de entradas na tabela entrega.

Se a função não for bem-sucedida, o valor de retorno será zero.

## <a name="remarks"></a>Comentários

A tabela de entrega criada pelo Monitor de Rede é baseada nas informações fornecidas no analisador INI. O identificador retornado para a tabela entrega pode ser usado para obter um identificador para um dos protocolos incluídos na tabela. Para obter um identificador de um desses protocolos, chame [GetProtocolFromTable](getprotocolfromtable.md).

Observe que o aplicativo Analisador nunca acessa a estrutura de **entrega** diretamente. Essa estrutura é criada e mantida por Monitor de Rede.

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

[GetProtocolFromTable](getprotocolfromtable.md)
</dt> <dt>

[ENTREGA](handofftable.md)
</dt> </dl>

 

 




