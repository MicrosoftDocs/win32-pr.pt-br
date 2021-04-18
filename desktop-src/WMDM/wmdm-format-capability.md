---
title: Estrutura de WMDM_FORMAT_CAPABILITY
description: A \_ estrutura de \_ recursos de formato WMDM descreve os recursos de um dispositivo para um determinado formato.
ms.assetid: 9672173D-B11E-4DCB-BCAE-38B94FCC8B99
keywords:
- Estrutura de WMDM_FORMAT_CAPABILITY Windows Media Gerenciador de Dispositivos
topic_type:
- apiref
api_name:
- WMDM_FORMAT_CAPABILITY
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14f8dbdd81aff63a819624cdb1c778cb9bec712b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796456"
---
# <a name="wmdm_format_capability-structure"></a>Estrutura de recursos de \_ formato WMDM \_

A estrutura de **\_ \_ recursos de formato WMDM** descreve os recursos de um dispositivo para um determinado formato. Essa estrutura contém um conjunto de configurações de propriedade em uma matriz de estruturas de **\_ \_ configuração de prop do WMDM** . Cada configuração de propriedade representa um conjunto de valores de propriedade compatíveis em todas as propriedades com suporte para um determinado formato. O aplicativo pode obter essa estrutura chamando o método **IWMDMDevice3:: GetFormatCapability** e passando o código de formato. Para obter uma lista de códigos de formato, consulte [**WMDM \_ FORMATCODE**](wmdm-formatcode.md).

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _WMDM_FORMAT_CAPABILITY {
  UINT              nPropConfig;
  WMDM_PROP_CONFIG  *pConfigs;
} WMDM_FORMAT_CAPABILITY;
```



## <a name="members"></a>Membros

<dl> <dt>

**nPropConfig**
</dt> <dd>

Número de configurações de propriedade na matriz **pConfigs** .

</dd> <dt>

**pConfigs**
</dt> <dd>

Ponteiro para uma matriz de estruturas de [**\_ \_ configuração de prop do WMDM**](wmdm-prop-config.md) . O tamanho da matriz é igual ao valor de **nPropConfig**.

</dd> </dl>

## <a name="remarks"></a>Comentários

A estrutura de **\_ \_ recursos de formato WMDM** fornece um mecanismo flexível para expressar os recursos do dispositivo para um determinado formato.

Se o conteúdo for destinado a ser renderizado pelo dispositivo (por exemplo, um arquivo de áudio a ser reproduzido pelo dispositivo), as propriedades do conteúdo deverão corresponder a uma das configurações de propriedade retornadas por [**IWMDMDevice3:: GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) na estrutura de **\_ \_ recursos do formato WMDM** . Por exemplo, para um arquivo de áudio, a taxa de bits e a taxa de amostragem devem satisfazer uma das configurações de propriedade retornadas.

O chamador é responsável por liberar a memória alocada para essa estrutura. A função a seguir demonstra como limpar uma estrutura de **\_ \_ recursos de formato do WMDM** .


```C++
void FreeFormatCapability(WMDM_FORMAT_CAPABILITY formatCap)
{
    // Loop through all configurations.
    for (UINT i=0; i < formatCap.nPropConfig; i++) 
    {
        // Loop through all descriptions of a configuration and delete
        // the values particular to that description type.
        for (UINT j=0; j < formatCap.pConfigs[i].nPropDesc; j++) 
        {
            switch (formatCap.pConfigs[i].pPropDesc[j].ValidValuesForm)
            {
                case WMDM_ENUM_PROP_VALID_VALUES_ENUM:
                    for (UINT k=0; k < formatCap.pConfigs[i].pPropDesc[j].ValidValues.EnumeratedValidValues.cEnumValues; k++)
                    {
                        PropVariantClear (&(formatCap.pConfigs[i].pPropDesc[j].ValidValues.EnumeratedValidValues.pValues[k]));
                    }
                    CoTaskMemFree(formatCap.pConfigs[i].pPropDesc[j].ValidValues.EnumeratedValidValues.pValues);
                    break;
                case WMDM_ENUM_PROP_VALID_VALUES_RANGE:
                    PropVariantClear (&(formatCap.pConfigs[i].pPropDesc[j].ValidValues.ValidValuesRange.rangeMin));
                    PropVariantClear (&(formatCap.pConfigs[i].pPropDesc[j].ValidValues.ValidValuesRange.rangeMax));
                    PropVariantClear (&(formatCap.pConfigs[i].pPropDesc[j].ValidValues.ValidValuesRange.rangeStep));
                    break;
                case WMDM_ENUM_PROP_VALID_VALUES_ANY:
                    // No dynamically allocated memory for this value.
                default:
                    break;
            }

            // Free the memory for the description name.
            CoTaskMemFree(formatCap.pConfigs[i].pPropDesc[j].pwszPropName);
        }
        // Free the memory holding the array of description items for this configuration.
        CoTaskMemFree(formatCap.pConfigs[i].pPropDesc);
    }

    // Free the memory pointing to the array of configurations.
    CoTaskMemFree(formatCap.pConfigs);
    formatCap.nPropConfig = 0;
}
```



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

[**\_configuração de prop do WMDM \_**](wmdm-prop-config.md)
</dt> <dt>

[**WMDM \_ prop \_ desc**](wmdm-prop-desc.md)
</dt> <dt>

[**\_enumeração de \_ valores de prop do WMDM \_**](wmdm-prop-values-enum.md)
</dt> <dt>

[**\_intervalo de \_ valores de prop do WMDM \_**](wmdm-prop-values-range.md)
</dt> <dt>

[**Estruturas**](structures.md)
</dt> </dl>

 

 





