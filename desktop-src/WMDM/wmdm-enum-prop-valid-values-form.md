---
title: Enumeração de WMDM_ENUM_PROP_VALID_VALUES_FORM
description: O \_ tipo de enumeração de formulário valores válidos de prop Enumerate do WMDM \_ \_ \_ \_ descreve possíveis formas de valores válidos para uma propriedade.
ms.assetid: 49d174b4-c8a3-4c16-ad21-4b66dcf8088f
keywords:
- WMDM_ENUM_PROP_VALID_VALUES_FORM de enumeração do Windows Media Gerenciador de Dispositivos
topic_type:
- apiref
api_name:
- WMDM_ENUM_PROP_VALID_VALUES_FORM
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d7db971f359a9cead2aae6083a934086d42c481
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781470"
---
# <a name="wmdm_enum_prop_valid_values_form-enumeration"></a>\_Enumeração de \_ \_ formato de \_ valores válidos de prop enum \_ do WMDM

O tipo de enumeração de **\_ \_ \_ \_ \_ formulário valores válidos de prop Enumerate do WMDM** descreve possíveis formas de valores válidos para uma propriedade.

## <a name="syntax"></a>Syntax


```C++
typedef enum _WMDM_ENUM_PROP_VALID_VALUES_FORM { 
  WMDM_ENUM_PROP_VALID_VALUES_ANY,
  WMDM_ENUM_PROP_VALID_VALUES_RANGE,
  WMDM_ENUM_PROP_VALID_VALUES_ENUM
} WMDM_ENUM_PROP_VALID_VALUES_FORM;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WMDM_ENUM_PROP_VALID_VALUES_ANY"></span><span id="wmdm_enum_prop_valid_values_any"></span>**\_ \_ \_ \_ todos os valores válidos de prop do WMDM enum \_**
</dt> <dd>

Todos os valores são válidos.

</dd> <dt>

<span id="WMDM_ENUM_PROP_VALID_VALUES_RANGE"></span><span id="wmdm_enum_prop_valid_values_range"></span>**\_intervalo de \_ \_ valores válidos \_ de \_ prop do WMDM enum**
</dt> <dd>

Os valores válidos são expressos como um intervalo. Para obter informações detalhadas, consulte a estrutura do [**\_ intervalo de \_ valores \_ de prop**](wmdm-prop-values-range.md) . do WMDM.

</dd> <dt>

<span id="WMDM_ENUM_PROP_VALID_VALUES_ENUM"></span><span id="wmdm_enum_prop_valid_values_enum"></span>**\_enumeração de \_ \_ valores válidos \_ de \_ prop do WMDM enum**
</dt> <dd>

Os valores válidos são um conjunto enumerado. Para obter informações detalhadas, consulte a estrutura de [**\_ enumeração de \_ valores \_ de prop**](wmdm-prop-values-enum.md) . do WMDM.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa enumeração é usada na estrutura [**\_ \_ desc prop do WMDM**](wmdm-prop-desc.md) para especificar a forma de valores válidos para uma propriedade.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Tipos de enumeração**](enumeration-types.md)
</dt> <dt>

[**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[**\_funcionalidade de formato WMDM \_**](wmdm-format-capability.md)
</dt> <dt>

[**\_configuração de prop do WMDM \_**](wmdm-prop-config.md)
</dt> <dt>

[**WMDM \_ prop \_ desc**](wmdm-prop-desc.md)
</dt> <dt>

[**\_enumeração de \_ valores de prop do WMDM \_**](wmdm-prop-values-enum.md)
</dt> <dt>

[**\_intervalo de \_ valores de prop do WMDM \_**](wmdm-prop-values-range.md)
</dt> </dl>

 

 





