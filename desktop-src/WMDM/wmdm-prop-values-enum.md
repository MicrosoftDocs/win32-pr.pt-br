---
title: Estrutura de WMDM_PROP_VALUES_ENUM
description: A \_ estrutura de enumeração de valores prop do WMDM \_ \_ contém um conjunto enumerado de valores válidos para uma propriedade específica em uma configuração de propriedade específica.
ms.assetid: 8094f3c0-a7ed-4e63-8503-aaac3fd9c012
keywords:
- Estrutura de WMDM_PROP_VALUES_ENUM Windows Media Gerenciador de Dispositivos
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
ms.openlocfilehash: a1c70088d57189dd36d360bc8910a15717d964ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813203"
---
# <a name="wmdm_prop_values_enum-structure"></a>\_Estrutura de \_ enumeração de valores de prop WMDM \_

A estrutura de **\_ \_ \_ enumeração de valores prop do WMDM** contém um conjunto enumerado de valores válidos para uma propriedade específica em uma configuração de propriedade específica.

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

**Valores principais**
</dt> <dd>

Ponteiro para uma matriz de valores. O tamanho da matriz é igual ao valor de **cEnumValues**.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura é usada na estrutura **\_ \_ desc prop do WMDM** para descrever um conjunto enumerado de valores válidos. Um conjunto enumerado de valores válidos é aplicável quando \_ SqlEnum \_ prop \_ \_ valores válidos \_ enum é selecionado na enumeração **de \_ \_ \_ \_ \_ formato de valores válidos de prop enum do WMDM** .

O chamador é necessário para liberar a memória usada por **valores principais**. Para obter um exemplo de como fazer isso, consulte [**a \_ \_ funcionalidade de formato WMDM**](wmdm-format-capability.md).

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

[**\_intervalo de \_ valores de prop do WMDM \_**](wmdm-prop-values-range.md)
</dt> <dt>

[**Estruturas**](structures.md)
</dt> </dl>

 

 





