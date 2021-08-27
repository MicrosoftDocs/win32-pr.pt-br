---
title: WMDM_PROP_VALUES_ENUM estrutura
description: A estrutura ENUM WMDM PROP VALUES contém um conjunto enumerado de valores válidos para uma propriedade \_ \_ específica em uma \_ configuração de propriedade específica.
ms.assetid: 8094f3c0-a7ed-4e63-8503-aaac3fd9c012
keywords:
- WMDM_PROP_VALUES_ENUM estrutura windows Media Gerenciador de Dispositivos
topic_type:
- apiref
api_name:
- WMDM_PROP_VALUES_ENUM
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35766ed71b864c5eb7f0bbbebf5eda384a25e174501aa2a56e790840a4c636c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004786"
---
# <a name="wmdm_prop_values_enum-structure"></a>Estrutura \_ ENUM DE VALORES DE PROP \_ DO WMDM \_

A **estrutura \_ \_ \_ ENUM WMDM PROP VALUES** contém um conjunto enumerado de valores válidos para uma propriedade específica em uma configuração de propriedade específica.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _WMDM_PROP_VALUES_ENUM {
  UINT        cEnumValues;
  PROPVARIANT *pValues;
} WMDM_PROP_VALUES_ENUM;
```



## <a name="members"></a>Membros

<dl> <dt>

**cEnumValues**
</dt> <dd>

Contagem de valores enumerados.

</dd> <dt>

**pValues**
</dt> <dd>

Ponteiro para uma matriz de valores. O tamanho da matriz é igual ao valor **de cEnumValues**.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura é usada na estrutura **\_ \_ DESC PROP do WMDM** para descrever um conjunto enumerado de valores válidos. Um conjunto enumerado de valores válidos é aplicável quando WMDM ENUM PROP VALID VALUES ENUM é selecionado na \_ \_ \_ \_ \_ enumeração **WMDM \_ ENUM \_ PROP VALID VALUES \_ \_ \_ FORM** FORM.

O chamador é necessário para liberar a memória usada por **pValues.** Para ver um exemplo de como fazer isso, consulte [**WMDM \_ FORMAT \_ CAPABILITY**](wmdm-format-capability.md).

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

[**INTERVALO DE VALORES DO WMDM \_ PROP \_ \_**](wmdm-prop-values-range.md)
</dt> <dt>

[**Estruturas**](structures.md)
</dt> </dl>

 

 





