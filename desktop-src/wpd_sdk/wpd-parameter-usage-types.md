---
description: O \_ tipo de enumeração de tipos de uso de parâmetro WPD \_ \_ descreve como um parâmetro de método é usado em um determinado método.
ms.assetid: 60cbb4fa-c5fd-4402-bfd4-8fd95c009a33
title: Enumeração de WPD_PARAMETER_USAGE_TYPES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_PARAMETER_USAGE_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 72d4ebffccc3d1bc7d446848c29ebbc60539430e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751543"
---
# <a name="wpd_parameter_usage_types-enumeration"></a>\_Enumeração de \_ tipos de uso de parâmetro WPD \_

O tipo de enumeração de [**\_ tipos de \_ uso \_ de parâmetro WPD**](/windows/desktop/wpd_sdk/wpd-parameter-usage-types) descreve como um parâmetro de método é usado em um determinado método.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagWPD_PARAMETER_USAGE_TYPES { 
  WPD_PARAMETER_USAGE_RETURN  = 0,
  WPD_PARAMETER_USAGE_IN      = 1,
  WPD_PARAMETER_USAGE_OUT     = 2,
  WPD_PARAMETER_USAGE_INOUT   = 3
} WPD_PARAMETER_USAGE_TYPES;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_PARAMETER_USAGE_RETURN"></span><span id="wpd_parameter_usage_return"></span>**\_retorno de \_ uso de parâmetro WPD \_**
</dt> <dd>

O parâmetro receberá o valor de retorno, se especificado pelo método.

</dd> <dt>

<span id="WPD_PARAMETER_USAGE_IN"></span><span id="wpd_parameter_usage_in"></span>**\_ \_ uso de parâmetro WPD \_ em**
</dt> <dd>

O parâmetro contém um valor de entrada antes que o método seja chamado.

</dd> <dt>

<span id="WPD_PARAMETER_USAGE_OUT"></span><span id="wpd_parameter_usage_out"></span>**\_uso de parâmetro WPD \_ \_**
</dt> <dd>

O parâmetro contém um valor de saída quando o método retorna.

</dd> <dt>

<span id="WPD_PARAMETER_USAGE_INOUT"></span><span id="wpd_parameter_usage_inout"></span>**\_uso de parâmetro de WPD \_ \_**
</dt> <dd>

O parâmetro contém um valor de entrada antes que o método seja chamado e um valor de saída quando ele retorna.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



 

