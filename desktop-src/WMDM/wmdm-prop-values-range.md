---
title: WMDM_PROP_VALUES_RANGE estrutura
description: A estrutura INTERVALO DE VALORES PROP DO WMDM descreve um intervalo de valores \_ \_ \_ válidos para uma propriedade específica em uma configuração de propriedade específica.
ms.assetid: fb823a66-cc9c-4632-a4f0-03c7255c3ccb
keywords:
- WMDM_PROP_VALUES_RANGE estrutura windows Media Gerenciador de Dispositivos
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
ms.openlocfilehash: a668b5acd8427df5b4bc163788c225f4eaee9a16b70af25312ae8ec94cb2bb63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004776"
---
# <a name="wmdm_prop_values_range-structure"></a>Estrutura DE INTERVALO DE \_ VALORES DE PROP \_ \_ DO WMDM

A **estrutura INTERVALO DE VALORES PROP \_ \_ \_ DO WMDM** descreve um intervalo de valores válidos para uma propriedade específica em uma configuração de propriedade específica.

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

**Rangemax**
</dt> <dd>

Valor máximo no intervalo.

</dd> <dt>

**rangeStep**
</dt> <dd>

O tamanho da etapa em que os valores válidos são incrementados do valor mínimo para o valor máximo. Isso permite especificar valores discretos permitidos em um intervalo.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura é usada na estrutura [**\_ \_ DESC PROP do WMDM**](wmdm-prop-desc.md) para descrever um intervalo de valores válidos. Um intervalo de valores válidos é aplicável quando WMDM ENUM PROP VALID VALUES ENUM é selecionado na \_ \_ \_ \_ \_ enumeração [**WMDM \_ ENUM \_ PROP VALID VALUES \_ FORM \_ \_ FORM.**](wmdm-enum-prop-valid-values-form.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdm.idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[**FORMULÁRIO DE VALORES VÁLIDOS DO WMDM \_ ENUM \_ PROP \_ \_ \_**](wmdm-enum-prop-valid-values-form.md)
</dt> <dt>

[**FUNCIONALIDADE DE FORMATO \_ \_ WMDM**](wmdm-format-capability.md)
</dt> <dt>

[**CONFIGURAÇÃO \_ DE PROP DO WMDM \_**](wmdm-prop-config.md)
</dt> <dt>

[**DESC DO WMDM \_ PROP \_**](wmdm-prop-desc.md)
</dt> <dt>

[**ENUM DE \_ VALORES DE PROP \_ \_ WMDM**](wmdm-prop-values-enum.md)
</dt> <dt>

[**Estruturas**](structures.md)
</dt> </dl>

 

 





