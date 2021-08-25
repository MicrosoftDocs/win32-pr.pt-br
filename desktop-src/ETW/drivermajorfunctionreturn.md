---
description: Essa classe é a classe de tipo de evento para os eventos de retorno de chamada de função principal do driver. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: b3358935-d6fb-49eb-bdf7-4366b4fd14c5
title: Classe DriverMajorFunctionReturn
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DriverMajorFunctionReturn
- DriverMajorFunctionReturn.Irp
- DriverMajorFunctionReturn.UniqMatchId
api_type:
- NA
api_location: ''
ms.openlocfilehash: de8c18d7655aec0f9ae4748c384b26015a5a1083721aae367e132ea7c39f80a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914466"
---
# <a name="drivermajorfunctionreturn-class"></a>Classe DriverMajorFunctionReturn

Essa classe é a classe de tipo de evento para os eventos de retorno de chamada de função principal do driver.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[EventType{35}, EventTypeName{"DrvMjFnRet"}]
class DriverMajorFunctionReturn : DiskIo
{
  uint32 Irp;
  uint32 UniqMatchId;
};
```

## <a name="members"></a>Membros

A classe **DriverMajorFunctionReturn** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **DriverMajorFunctionReturn** tem essas propriedades.

<dl> <dt>

**IRP**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (1), ponteiro
</dt> </dl>

Pacote de solicitação de e/s.

</dd> <dt>

**UniqMatchId**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (2)
</dt> </dl>

Identificador que identifica a solicitação de forma exclusiva. Use esse identificador para correlacionar com os outros eventos de driver, por exemplo, o evento [**DriverCompleteRequest**](drivercompleterequest.md) .

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

 

 




