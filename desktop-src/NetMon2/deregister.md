---
description: A função de exportação de cancelamento de registro libera os recursos usados para criar o banco de dados de propriedades de protocolo. A DLL do analisador deve implementar o cancelamento de registro.
ms.assetid: 80852aed-07aa-440f-a537-f6cce461292e
title: Função de retorno de chamada de cancelamento de registro (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Deregister
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: cb06ab6e08a674a186bcdb260140915c378db9affc13b17db33d9132109cec78
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911216"
---
# <a name="deregister-callback-function"></a>Cancelar registro da função de retorno de chamada

A função de exportação de **cancelamento de registro** libera os recursos usados para criar o [*banco de dados de propriedades*](p.md)de protocolo. A DLL do analisador deve implementar o **cancelamento de registro**.

## <a name="syntax"></a>Sintaxe


```C++
VOID Deregister(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hProtocol* \[ no\]
</dt> <dd>

Identificador do protocolo para um banco de dados específico.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Nenhum.

## <a name="remarks"></a>Comentários

Monitor de Rede chama o **cancelamento do registro** depois de passar todas as informações de captura para a DLL do analisador. A DLL do analisador deve implementar uma função de **cancelamento de registro** para cada protocolo compatível com o analisador.

Ao implementar o **cancelamento do registro**, a DLL do analisador deve chamar a função [DestroyPropertyDatabase](destroypropertydatabase.md) para liberar os recursos do banco de [*dados de propriedade*](p.md) .



| Para obter informações sobre                                        | Consulte                                                    |
|-----------------------------------------------------------|--------------------------------------------------------|
| Quais analisadores são e como eles funcionam com Monitor de Rede. | [Analisadores](parsers.md)                                 |
| Quais pontos de entrada são incluídos na DLL do analisador.        | [Arquitetura de DLL do analisador](parser-dll-architecture.md) |
| Como implementar o **cancelamento de registro**  inclui um exemplo.     | [Implementando cancelamento de registro](implementing-deregister.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[DestroyPropertyDatabase](destroypropertydatabase.md)
</dt> </dl>

 

 




