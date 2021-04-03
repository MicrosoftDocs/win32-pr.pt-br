---
description: A função DestroyPropertyDatabase libera os recursos usados para criar o banco de dados de propriedades de protocolo.
ms.assetid: a0d1c416-8b08-47ca-a88e-e70588574376
title: Função DestroyPropertyDatabase (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyPropertyDatabase
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: baedae22e948b38d9ff162942269ac4529896826
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922620"
---
# <a name="destroypropertydatabase-function"></a>Função DestroyPropertyDatabase

A função **DestroyPropertyDatabase** libera os recursos usados para criar o [*banco de dados de propriedades*](p.md)de protocolo.

## <a name="syntax"></a>Sintaxe


```C++
DWORD WINAPI DestroyPropertyDatabase(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hProtocol* \[ no\]
</dt> <dd>

Identificador para o banco de dados de propriedades a ser destruído. O identificador é passado para a DLL do analisador quando Monitor de Rede chama a função de [cancelamento de registro](deregister.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.

Se a função não for bem-sucedida, o valor de retorno será um código de erro.



| Código de retorno                                                                                              | Descrição                                |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <dt>**\_erro interno de NMERR \_**</dt> </dl>    | Ocorreu um erro interno. <br/>    |
| <dl> <dt>**NMERR \_ HPROTOCOL inválida \_**</dt> </dl> | Identificador inválido em *hProtocol*. <br/> |



 

## <a name="remarks"></a>Comentários

A função **DestroyPropertyDatabase** deve ser chamada somente ao implementar a função de exportação de [cancelamento de registro](deregister.md) para o protocolo. Para DLLs do analisador que dão suporte a vários protocolos, a função **DestroyPropertyDatabase** é chamada para cada implementação de **cancelamento de registro**.



| Para obter informações sobre                                        | Consulte                                                    |
|-----------------------------------------------------------|--------------------------------------------------------|
| Quais analisadores são e como eles funcionam com Monitor de Rede. | [Analisadores](parsers.md)                                 |
| Quais pontos de entrada são incluídos na DLL do analisador.        | [Arquitetura de DLL do analisador](parser-dll-architecture.md) |
| Como implementar o **cancelamento de registro**  inclui um exemplo.     | [Implementando cancelamento de registro](implementing-deregister.md) |



 

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

[Cancelar registro](deregister.md)
</dt> </dl>

 

 




