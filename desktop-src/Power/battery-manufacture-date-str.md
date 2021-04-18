---
description: Contém a data de fabricação de uma bateria.
ms.assetid: 0cda66fc-bf4a-4a38-b43c-6eecde46c414
title: Estrutura de BATTERY_MANUFACTURE_DATE (Poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_MANUFACTURE_DATE
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: cdd3f067bc3ed2e3339710e0a5bd48c8f42e6525
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758926"
---
# <a name="battery_manufacture_date-structure"></a>Estrutura de data de \_ fabricação da bateria \_

Contém a data de fabricação de uma bateria. Essa estrutura é usada pela estrutura [**de \_ \_ informações de consulta de bateria**](battery-query-information-str.md) quando o nível de informações BatteryManufactureDate é solicitado.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _BATTERY_MANUFACTURE_DATE {
  UCHAR  Day;
  UCHAR  Month;
  USHORT Year;
} BATTERY_MANUFACTURE_DATE, *PBATTERY_MANUFACTURE_DATE;
```



## <a name="members"></a>Membros

<dl> <dt>

**Day**
</dt> <dd>

O dia do mês de fabricação, no intervalo de 1 a 31. Apesar do tipo de dados, esse não é um valor codificado em ASCII. É um byte não assinado.

</dd> <dt>

**Mês**
</dt> <dd>

O mês de fabricação, no intervalo de 1 (Janeiro) a 12 (Dezembro). Apesar do tipo de dados, esse não é um valor codificado em ASCII. É um byte não assinado.

</dd> <dt>

**Year**
</dt> <dd>

O ano de fabricação. Normalmente, isso estará no intervalo de 1900-2100.

</dd> </dl>

## <a name="remarks"></a>Comentários

A data é codificada no formato Gregoriano ou do calendário ocidental.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                                                                                                                                                                                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                                                                                                                                                                                |
| parâmetro<br/>                   | <dl> <dt>Poclass. h; </dt> <dt>Batclass. h no Windows server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_informações de consulta de bateria \_**](battery-query-information-str.md)
</dt> <dt>

[**\_informações de \_ consulta da bateria do IOCTL \_**](ioctl-battery-query-information.md)
</dt> </dl>

 

 




