---
title: Estrutura de WMDM_PROP_DESC
description: A estrutura do WMDM \_ prop \_ desc descreve os valores válidos de uma propriedade em uma configuração de propriedade específica.
ms.assetid: e4766e1e-6c1b-4a2d-ad2e-c07035ca2be2
keywords:
- Estrutura de WMDM_PROP_DESC Windows Media Gerenciador de Dispositivos
topic_type:
- apiref
api_name:
- WMDM_PROP_DESC
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cad250745d51f00d3bb0492b6da8d3f9802bf87b78d65f4640324a68caa9ddf3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903936"
---
# <a name="wmdm_prop_desc-structure"></a>\_Estrutura desc prop do WMDM \_

A estrutura do **WMDM \_ prop \_ desc** descreve os valores válidos de uma propriedade em uma configuração de propriedade específica.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _WMDM_PROP_DESC {
  LPWSTR                           pwszPropName;
  WMDM_ENUM_PROP_VALID_VALUES_FORM ValidValuesForm;
  union  {
    WMDM_PROP_VALUES_RANGE ValidValuesRange;
    WMDM_PROP_VALUES_ENUM  EnumeratedValidValues;
  } ValidValues;
} WMDM_PROP_DESC;
```



## <a name="members"></a>Membros

<dl> <dt>

**pwszPropName**
</dt> <dd>

Nome da propriedade. O aplicativo deve liberar essa memória quando terminar de usá-la.

</dd> <dt>

**ValidValuesForm**
</dt> <dd>

Um valor de enumeração do [**\_ \_ \_ \_ \_ formulário de valores válidos da prop do WMDM enum**](wmdm-enum-prop-valid-values-form.md) que descreve o tipo de valores, como um intervalo ou uma lista. O valor dessa enumeração determina qual variável de membro é usada.

</dd> <dt>

**ValidValues**
</dt> <dd>

Mantém os valores válidos da propriedade em uma configuração de propriedade específica. Esse membro contém um dos três itens: o valor de enumeração \_ WMDM \_ enum \_ prop \_ Values válidos \_ any; o membro **ValidValuesRange**; ou o membro **EnumeratedValidValues**. O valor ou o membro é indicado por **ValidValuesForm**.

<dl> <dt>

**ValidValuesRange**
</dt> <dd>

Uma estrutura de [**\_ \_ \_ intervalo de valores prop do WMDM**](wmdm-prop-values-range.md) que contém um intervalo de valores válidos. Isso está presente somente quando **ValidValuesForm** está definido como WMDM \_ enum \_ prop \_ \_ valores válidos \_ Range. Consulte Observações.

</dd> <dt>

**EnumeratedValidValues**
</dt> <dd>

Uma estrutura de [**\_ \_ \_ enumeração de valores prop do WMDM**](wmdm-prop-values-enum.md) que contém um conjunto enumerado de valores válidos. Isso só estará presente quando **ValidValuesForm** for definido como WMDM \_ enum \_ prop \_ \_ valores válidos \_ enum. Consulte Observações.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

A **estrutura \_ \_ desc prop do WMDM** contém uma descrição de propriedade que consiste em um nome de propriedade e seus valores válidos em uma configuração específica.

O chamador é necessário para liberar a memória usada por **ValidValuesRange** ou **EnumeratedValues**. Para obter um exemplo de como fazer isso, consulte [**a \_ \_ funcionalidade de formato WMDM**](wmdm-format-capability.md).

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

[**\_enumeração de \_ valores de prop do WMDM \_**](wmdm-prop-values-enum.md)
</dt> <dt>

[**\_intervalo de \_ valores de prop do WMDM \_**](wmdm-prop-values-range.md)
</dt> <dt>

[**Estruturas**](structures.md)
</dt> </dl>

 

 





