---
description: Essa classe é a classe de tipo de evento para eventos de término de operação de arquivo. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 3925d5bf-f412-4248-a61f-e667efa9debd
title: Classe FileIo_OpEnd
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_OpEnd
- FileIo_OpEnd.IrpPtr
- FileIo_OpEnd.ExtraInfo
- FileIo_OpEnd.NtStatus
api_type:
- NA
api_location: ''
ms.openlocfilehash: d3f1c495cf44b84f8d7661b40cadec6ea255c6a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662798"
---
# <a name="fileio_opend-class"></a>\_Classe aberta de FileIo

Essa classe é a classe de tipo de evento para eventos de término de operação de arquivo.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[EventType{76}, EventTypeName{"OperationEnd"}]
class FileIo_OpEnd : FileIo
{
  uint32 IrpPtr;
  uint32 ExtraInfo;
  uint32 NtStatus;
};
```

## <a name="members"></a>Membros

A **classe \_ aberta FileIo** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ aberta FileIo** tem essas propriedades.

<dl> <dt>

**ExtraInfo**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (2), ponteiro
</dt> </dl>

Informações extras retornadas pelo sistema de arquivos para a operação. Por exemplo, para uma solicitação de leitura, o número real de bytes lidos.

</dd> <dt>

**IrpPtr**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (1), ponteiro
</dt> </dl>

Pacote de solicitação de e/s. Essa propriedade identifica a atividade de e/s que está terminando.

</dd> <dt>

**NtStatus**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (3)
</dt> </dl>

Valor de retorno da operação.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os eventos de [**FileIo**](fileio.md) são registrados no início da operação. Os eventos abertos podem ser habilitados separadamente para indicar o fim dessas operações. O IRP pode ser usado para correlacionar os eventos de início e término.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**FileIo**](fileio.md)
</dt> </dl>

 

 




