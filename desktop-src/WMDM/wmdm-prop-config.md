---
title: Estrutura de WMDM_PROP_CONFIG
description: A \_ estrutura de configuração do sqlprop \_ descreve um conjunto de valores de propriedade compatíveis em todas as propriedades com suporte pelo dispositivo para um determinado formato. Essa estrutura contém várias descrições de propriedade em uma matriz de \_ estruturas desc prop do WMDM \_ .
ms.assetid: cf116861-e31d-4561-b262-e271888afc24
keywords:
- Estrutura de WMDM_PROP_CONFIG Windows Media Gerenciador de Dispositivos
topic_type:
- apiref
api_name:
- WMDM_PROP_CONFIG
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b19314b2f012d25fa2d97b44b9dc7524f9e3355
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813396"
---
# <a name="wmdm_prop_config-structure"></a>Estrutura de configuração de \_ prop do WMDM \_

A estrutura de **\_ \_ configuração do sqlprop** descreve um conjunto de valores de propriedade compatíveis em todas as propriedades com suporte pelo dispositivo para um determinado formato. Essa estrutura contém várias descrições de propriedade em uma matriz de estruturas [**\_ \_ desc prop do WMDM**](wmdm-prop-desc.md) .

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _WMDM_PROP_CONFIG {
  UINT           nPreference;
  UINT           nPropDesc;
  WMDM_PROP_DESC *pPropDesc;
} WMDM_PROP_CONFIG;
```



## <a name="members"></a>Membros

<dl> <dt>

**nPreference**
</dt> <dd>

Nível de preferência do dispositivo para esta configuração. O valor mais baixo indica a configuração mais preferencial.

</dd> <dt>

**nPropDesc**
</dt> <dd>

Número de descrições de propriedade contidas nessa configuração. Há uma única descrição de propriedade para cada propriedade com suporte para o formato especificado.

</dd> <dt>

**pPropDesc**
</dt> <dd>

Ponteiro para uma matriz de [**estruturas \_ \_ desc prop do WMDM**](wmdm-prop-desc.md) contendo descrições de propriedade. O tamanho da matriz é igual ao valor de **nPropDesc**. O aplicativo deve liberar essa memória quando terminar com ela.

</dd> </dl>

## <a name="remarks"></a>Comentários

A estrutura de [**\_ \_ recursos de formato WMDM**](wmdm-format-capability.md) retornada por [**IWMDMDevice3:: GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) para um formato específico consiste em um número de configurações de propriedade. **WMDM \_ As \_** estruturas de configuração da prop descrevem essas configurações.

Uma configuração de propriedade descreve valores para todas as propriedades com suporte para um determinado formato. Os valores de propriedades diferentes em uma única configuração são compatíveis entre si. Por exemplo, para um arquivo de áudio, uma configuração incluirá valores válidos de taxa de amostra e valores válidos da taxa de bits, de modo que todas as combinações dessas taxas de amostra e de bits possam ser reproduzidas no dispositivo.

O chamador é necessário para liberar a memória usada pelo **pPropDesc**. Para obter um exemplo de como fazer isso, consulte [**a \_ \_ funcionalidade de formato WMDM**](wmdm-format-capability.md).

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

[**WMDM \_ prop \_ desc**](wmdm-prop-desc.md)
</dt> <dt>

[**\_enumeração de \_ valores de prop do WMDM \_**](wmdm-prop-values-enum.md)
</dt> <dt>

[**\_intervalo de \_ valores de prop do WMDM \_**](wmdm-prop-values-range.md)
</dt> <dt>

[**Estruturas**](structures.md)
</dt> </dl>

 

 





