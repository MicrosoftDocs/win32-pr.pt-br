---
description: Essa classe é a classe de tipo de evento para eventos de solicitação de conclusão de driver. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: c9c9be05-c1c6-4d77-a47a-44a61ebfcdc7
title: Classe DriverCompleteRequest
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DriverCompleteRequest
- DriverCompleteRequest.RoutineAddr
- DriverCompleteRequest.Irp
- DriverCompleteRequest.UniqMatchId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2ef20d7bf097c35e03e94ee9bb80e7fd74ad93d3f28830c66b155b3cacf400b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118151627"
---
# <a name="drivercompleterequest-class"></a>Classe DriverCompleteRequest

Essa classe é a classe de tipo de evento para eventos de solicitação de conclusão de driver.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[EventType{52}, EventTypeName{"DrvComplReq"}]
class DriverCompleteRequest : DiskIo
{
  uint32 RoutineAddr;
  uint32 Irp;
  uint32 UniqMatchId;
};
```

## <a name="members"></a>Membros

A classe **DriverCompleteRequest** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **DriverCompleteRequest** tem essas propriedades.

<dl> <dt>

**IRP**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (2), ponteiro
</dt> </dl>

Pacote de solicitação de e/s.

</dd> <dt>

**RoutineAddr**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (1), ponteiro
</dt> </dl>

Endereço da função de driver que está sendo chamada.

</dd> <dt>

**UniqMatchId**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (3)
</dt> </dl>

Identificador que identifica a solicitação de forma exclusiva. Use esse identificador para correlacionar com os outros eventos de driver, por exemplo, o evento [**DriverCompleteRequestReturn**](drivercompleterequestreturn.md) .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**DiskIo**](diskio.md)
</dt> </dl>

 

 




