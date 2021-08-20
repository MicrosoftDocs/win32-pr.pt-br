---
description: A função GetProtocolFromTable retorna um identificador para um protocolo&\# 8212; com base em uma determinada tabela e valor de entrega.
ms.assetid: 34b07079-0b20-40d8-a529-4179ecc68ebf
title: Função GetProtocolFromTable (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolFromTable
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: ba50756c515c363b4a574867ed8bcf71bf249a883022664cc31ecd15391eadc3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117981976"
---
# <a name="getprotocolfromtable-function"></a>Função GetProtocolFromTable

A função **GetProtocolFromTable** retorna um identificador para um protocolo com base em uma determinada tabela e valor de entrega.

## <a name="syntax"></a>Sintaxe


```C++
HPROTOCOL WINAPI GetProtocolFromTable(
  _In_  LPHANDOFFTABLE hTable,
  _In_  DWORD          ItemToFind,
  _Out_ PDWORD_PTR     lpInstData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hTable* \[ no\]
</dt> <dd>

Identificador para uma tabela de entrega.

</dd> <dt>

*ItemToFind* \[ no\]
</dt> <dd>

Valor usado para localizar o protocolo em uma tabela de entrega. O valor deve estar disponível nos dados do protocolo.

</dd> <dt>

*lpInstData* \[ fora\]
</dt> <dd>

Se disponível na tabela entrega, os dados da instância para o próximo protocolo. Os dados da instância não podem ter mais de um \_ PTR de comprimento.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será um identificador de protocolo.

Se a função não for bem-sucedida, o valor de retorno será **nulo**.

## <a name="remarks"></a>Comentários

Ao implementar a função de exportação [RecognizeFrame](recognizeframe.md) , a função **GetProtocolFromTable** é usada para obter um identificador para o próximo protocolo. A função **GetProtocolFromTable** será chamada para recuperar um identificador do próximo protocolo se o protocolo identificar o protocolo a seguir.

**Dados de instância**

Os dados da instância podem ser quaisquer dados que sejam menores ou iguais a um \_ PTR de comprimento, ou um ponteiro para dados, como dados de quadro brutos, que não precisam ser alocados pelo analisador ou liberados pelo parser.

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

[RecognizeFrame](recognizeframe.md)
</dt> </dl>

 

 




