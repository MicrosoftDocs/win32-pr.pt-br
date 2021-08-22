---
description: Essa classe é a classe de tipo de evento para eventos de chamada de função principal do driver. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 8c913145-ac50-4d40-8519-5fed79d977ba
title: Classe DriverMajorFunctionCall
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DriverMajorFunctionCall
- DriverMajorFunctionCall.MajorFunction
- DriverMajorFunctionCall.MinorFunction
- DriverMajorFunctionCall.RoutineAddr
- DriverMajorFunctionCall.FileObject
- DriverMajorFunctionCall.Irp
- DriverMajorFunctionCall.UniqMatchId
api_type:
- NA
api_location: ''
ms.openlocfilehash: b69012ae3d9dd46d2dd54c3859895288b9113fa89c772172e3f66a730b058d4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070236"
---
# <a name="drivermajorfunctioncall-class"></a>Classe DriverMajorFunctionCall

Essa classe é a classe de tipo de evento para eventos de chamada de função principal do driver.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[EventType{34}, EventTypeName{"DrvMjFnCall"}]
class DriverMajorFunctionCall : DiskIo
{
  uint32 MajorFunction;
  uint32 MinorFunction;
  uint32 RoutineAddr;
  uint32 FileObject;
  uint32 Irp;
  uint32 UniqMatchId;
};
```

## <a name="members"></a>Membros

A **classe DriverMajorFunctionCall** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe DriverMajorFunctionCall** tem essas propriedades.

<dl> <dt>

**FileObject**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(4), Pointer
</dt> </dl>

Corresponder o valor desse ponteiro ao valor do ponteiro **FileObject** em um evento [**DiskIo \_ TypeGroup1**](diskio-typegroup1.md) para determinar o tipo de operação de E/S.

</dd> <dt>

**Irp**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(5), Pointer
</dt> </dl>

Pacote de solicitação de E/S.

</dd> <dt>

**MajorFunction**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(1)
</dt> </dl>

Código que identifica a função principal que está sendo chamada.

</dd> <dt>

**MinorFunction**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(2)
</dt> </dl>

Código que idenitifies a função secundária que está sendo chamada.

</dd> <dt>

**RoutineAddr**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(3), Pointer
</dt> </dl>

Endereço da função de driver que está sendo chamada.

</dd> <dt>

**UniqMatchId**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(6)
</dt> </dl>

Identificador que identifica exclusivamente a solicitação. Use esse identificador para correlacionar com os outros eventos de driver, por exemplo, [**o evento DriverCompleteRequest.**](drivercompleterequest.md)

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**DiskIo**](diskio.md)
</dt> </dl>

 

 




