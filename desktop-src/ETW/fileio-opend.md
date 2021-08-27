---
description: Essa classe é a classe de tipo de evento para eventos de fim de operação de arquivo. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 3925d5bf-f412-4248-a61f-e667efa9debd
title: FileIo_OpEnd classe
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
ms.openlocfilehash: 74042df74f8e128c4d92b6e4f1c886a7bba2f673c1a8a998a4b7f251475c3f93
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130586"
---
# <a name="fileio_opend-class"></a>Classe \_ OpEnd FileIo

Essa classe é a classe de tipo de evento para eventos de fim de operação de arquivo.

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

A **classe \_ OpEnd FileIo** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ OpEnd FileIo** tem essas propriedades.

<dl> <dt>

**Extrainfo**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(2), Pointer
</dt> </dl>

Informações adicionais retornadas pelo sistema de arquivos para a operação. Por exemplo, para uma solicitação de leitura, o número real de bytes que foram lidos.

</dd> <dt>

**IrpPtr**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(1), Pointer
</dt> </dl>

Pacote de solicitação de E/S. Essa propriedade identifica a atividade de E/S que está terminando.

</dd> <dt>

**NtStatus**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(3)
</dt> </dl>

Valor de retorno da operação.

</dd> </dl>

## <a name="remarks"></a>Comentários

[**Os eventos fileIo**](fileio.md) são registrados no início da operação. Eventos OpEnd podem ser habilitados separadamente para indicar o final dessas operações. O Irp pode ser usado para correlacionar os eventos de início e término.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Fileio**](fileio.md)
</dt> </dl>

 

 




