---
description: Registry_V1_TypeGroup1 classe - essa classe é a classe de tipo de evento para eventos do Registro. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 59c455a0-af7e-4fd5-9af4-07ff72ee0545
title: Registry_V1_TypeGroup1 classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Registry_V1_TypeGroup1
- Registry_V1_TypeGroup1.Status
- Registry_V1_TypeGroup1.KeyHandle
- Registry_V1_TypeGroup1.ElapsedTime
- Registry_V1_TypeGroup1.Index
- Registry_V1_TypeGroup1.KeyName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 80b6bfbac1afbe3797bd76dfa49dee6666a339eb46c336d3e6c68f6b236c0848
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069766"
---
# <a name="registry_v1_typegroup1-class"></a>Classe \_ \_ TypeGroup1 do Registro V1

Essa classe é a classe de tipo de evento para eventos do Registro.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[EventType{10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22}, EventTypeName{"Create", "Open", "Delete", "Query", "SetValue", "DeleteValue", "QueryValue", "EnumerateKey", "EnumerateValueKey", "QueryMultipleValue", "SetInformation", "Flush", "RunDown"}]
class Registry_V1_TypeGroup1 : Registry
{
  uint32 Status;
  uint32 KeyHandle;
  sint64 ElapsedTime;
  uint32 Index;
  string KeyName;
};
```

## <a name="members"></a>Membros

A **classe \_ \_ TypeGroup1 do Registro V1** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ \_ TypeGroup1 do Registro V1** tem essas propriedades.

<dl> <dt>

ElapsedTime
</dt> <dd> <dl> <dt>

Tipo de dados: **sint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(3)
</dt> </dl>

Tempo decorrido da operação do Registro.

</dd> <dt>

Índice
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(4)
</dt> </dl>

O índice de sub-chave para a operação do Registro (como EnumerateKey).

</dd> <dt>

Keyhandle
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(2), Pointer
</dt> </dl>

Lidar com a chave do Registro.

</dd> <dt>

KeyName
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(5), StringTermination("NullTerminated"), Format("w")
</dt> </dl>

Nome da chave do Registro.

</dd> <dt>

Status
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(1), Pointer
</dt> </dl>

Valor NTSTATUS da operação do Registro.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Registro**](registry.md)
</dt> <dt>

[**Registro \_ V1**](registry-v1.md)
</dt> </dl>

 

 




