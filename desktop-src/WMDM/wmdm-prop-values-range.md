---
title: Estrutura de WMDM_PROP_VALUES_RANGE
description: A \_ \_ estrutura de intervalo de valores prop do WMDM \_ descreve um intervalo de valores válidos para uma determinada propriedade em uma configuração de propriedade específica.
ms.assetid: fb823a66-cc9c-4632-a4f0-03c7255c3ccb
keywords:
- Estrutura de WMDM_PROP_VALUES_RANGE Windows Media Gerenciador de Dispositivos
topic_type:
- apiref
api_name:
- WMDM_PROP_VALUES_RANGE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ba82a1067db97e93fff2845e69e89f978548b73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781071"
---
# <a name="wmdm_prop_values_range-structure"></a>\_Estrutura do \_ intervalo de valores prop do WMDM \_

A estrutura de **\_ \_ \_ intervalo de valores prop do WMDM** descreve um intervalo de valores válidos para uma determinada propriedade em uma configuração de propriedade específica.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _WMDM_PROP_VALUES_RANGE {
  PROPVARIANT rangeMin;
  PROPVARIANT rangeMax;
  PROPVARIANT rangeStep;
} WMDM_PROP_VALUES_RANGE;
```



## <a name="members"></a>Membros

<dl> <dt>

**rangeMin**
</dt> <dd>

Valor mínimo no intervalo.

</dd> <dt>

**rangeMax**
</dt> <dd>

Valor máximo no intervalo.

</dd> <dt>

**rangeStep**
</dt> <dd>

O tamanho da etapa em que os valores válidos são incrementados do valor mínimo para o valor máximo. Isso permite especificar valores permitidos distintos em um intervalo.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura é usada na estrutura [**\_ \_ desc prop do WMDM**](wmdm-prop-desc.md) para descrever um intervalo de valores válidos. Um intervalo de valores válidos é aplicável quando \_ SqlEnum \_ prop \_ \_ valores válidos \_ enum é selecionado na enumeração [**de \_ \_ \_ \_ \_ formato de valores válidos de prop enum**](wmdm-enum-prop-valid-values-form.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[**\_formulário de \_ \_ valores válidos \_ de prop Enumeração WMDM \_**](wmdm-enum-prop-valid-values-form.md)
</dt> <dt>

[**\_funcionalidade de formato WMDM \_**](wmdm-format-capability.md)
</dt> <dt>

[**\_configuração de prop do WMDM \_**](wmdm-prop-config.md)
</dt> <dt>

[**WMDM \_ prop \_ desc**](wmdm-prop-desc.md)
</dt> <dt>

[**\_enumeração de \_ valores de prop do WMDM \_**](wmdm-prop-values-enum.md)
</dt> <dt>

[**Estruturas**](structures.md)
</dt> </dl>

 

 





