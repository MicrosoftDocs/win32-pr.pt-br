---
description: O tipo de enumeração WPD \_ PARAMETER USAGE TYPES descreve como um parâmetro de método é usado em um determinado \_ \_ método.
ms.assetid: 60cbb4fa-c5fd-4402-bfd4-8fd95c009a33
title: WPD_PARAMETER_USAGE_TYPES enumeração (PortableDevice.h)
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
ms.openlocfilehash: 8ece49d1b961ce6ce5c14241d14bf69480e1eb79028f57a2cb959f5d7c4b79dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117842063"
---
# <a name="wpd_parameter_usage_types-enumeration"></a>Enumeração DE TIPOS DE \_ \_ USO DE \_ PARÂMETRO WPD

O [**tipo de enumeração WPD \_ PARAMETER USAGE \_ \_ TYPES**](/windows/desktop/wpd_sdk/wpd-parameter-usage-types) descreve como um parâmetro de método é usado em um determinado método.

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

<span id="WPD_PARAMETER_USAGE_RETURN"></span><span id="wpd_parameter_usage_return"></span>**RETORNO DE USO \_ \_ DO PARÂMETRO WPD \_**
</dt> <dd>

O parâmetro recebe o valor de retorno, se especificado pelo método .

</dd> <dt>

<span id="WPD_PARAMETER_USAGE_IN"></span><span id="wpd_parameter_usage_in"></span>**USO DE PARÂMETRO WPD \_ \_ \_ NO**
</dt> <dd>

O parâmetro contém um valor de entrada antes que o método seja chamado.

</dd> <dt>

<span id="WPD_PARAMETER_USAGE_OUT"></span><span id="wpd_parameter_usage_out"></span>**USO DO PARÂMETRO WPD \_ \_ \_ OUT**
</dt> <dd>

O parâmetro contém um valor de saída quando o método retorna.

</dd> <dt>

<span id="WPD_PARAMETER_USAGE_INOUT"></span><span id="wpd_parameter_usage_inout"></span>**INOUT DE \_ \_ USO DO PARÂMETRO WPD \_**
</dt> <dd>

O parâmetro contém um valor de entrada antes de o método ser chamado e um valor de saída quando ele retorna.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



 

