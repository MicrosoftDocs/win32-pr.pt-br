---
description: A função CreatePropertyDatabase cria um banco de dados de propriedade que armazena as propriedades de um protocolo.
ms.assetid: 0a3be6ae-d7ce-4315-b4f2-b46bcfa25b69
title: Função CreatePropertyDatabase (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreatePropertyDatabase
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 7c07f6f3e4569c06f0b3890e3ef3a26bca10b3272849fc005dfb3be6cbc2836b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118367213"
---
# <a name="createpropertydatabase-function"></a>Função CreatePropertyDatabase

A função **CreatePropertyDatabase** cria um banco de dados de propriedade que armazena as propriedades de um protocolo.

## <a name="syntax"></a>Sintaxe


```C++
DWORD WINAPI CreatePropertyDatabase(
  _In_ HPROTOCOL hProtocol,
  _In_ DWORD     nProperties
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hProtocol* \[ no\]
</dt> <dd>

Identificador do protocolo associado ao banco de dados. Quando Monitor de Rede chama a função de [registro](register-parser.md) , monitor de rede passa o identificador de protocolo para a DLL do analisador.

</dd> <dt>

*nProperties* \[ no\]
</dt> <dd>

Número de propriedades armazenadas no banco de dados. Defina esse parâmetro como o número de propriedades que o protocolo dá suporte.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.

Se a função não for bem-sucedida, o valor de retorno será um código de erro.



| Código de retorno                                                                                             | Descrição                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>**\_erro interno de NMERR \_**</dt> </dl>   | Ocorreu um erro interno.<br/>                                     |
| <dl> <dt>**NMERR \_ HPOTOCOL inválida \_**</dt> </dl> | O identificador para o protocolo especificado em *hProtocol* é inválido.<br/>     |
| <dl> <dt>**NMERR \_ \_ de \_ memória insuficiente**</dt> </dl>   | Monitor de Rede não tem memória suficiente para criar o banco de dados.<br/> |



 

## <a name="remarks"></a>Comentários

A função **CreatePropertyDatabase** deve ser chamada somente ao implementar a função [Register](register-parser.md) . O analisador usa **CreatePropertyDatabase** para criar um banco de dados de propriedade que descreve as propriedades de um protocolo. Monitor de Rede usa o banco de dados para interpretar as informações no protocolo.

A função **CreatePropertyDatabase** aloca as estruturas que monitor de rede precisa para manter um banco de dados de propriedade.

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

[Registrar](register-parser.md)
</dt> </dl>

 

 




