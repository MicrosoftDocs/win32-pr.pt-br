---
description: Esta seção descreve as constantes Windows sistema de propriedades, enumerações e sinalizadores.
ms.assetid: ff735b9c-e444-4e6f-8e80-0b2a5d770386
title: Constantes, enumerações e sinalizadores (Windows de propriedades)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24e39d357ae741ae49c4fa98c886e8c08b3594a2ea3a7e4e045def96abe8c2fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119718198"
---
# <a name="constants-enumerations-and-flags"></a>Constantes, enumerações e sinalizadores

Esta seção descreve as constantes Windows sistema de propriedades, enumerações e sinalizadores.



| Tópico                                                                              | Sumário                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GETPROPERTYSTOREFLAGS**](/windows/desktop/api/Propsys/ne-propsys-getpropertystoreflags)                             | Indica sinalizadores que modificam o objeto de repositório de propriedades recuperado por métodos que criam um repositório de propriedades, como [**IShellItem2::GetPropertyStore**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellitem2-getpropertystore) ou [**IPropertyStoreFactory::GetPropertyStore**](/windows/win32/api/propsys/nf-propsys-ipropertystorefactory-getpropertystore).<br/>                                                                                        |
| [**PDOPSTATUS**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-pdopstatus)                                                 | Fornece sinalizadores de status da operação.<br/>                                                                                                                                                                                                                                                                                                                                                |
| [**SINALIZADORES PKA \_**](/windows/win32/api/propsys/ne-propsys-pka_flags)                                                  | Descreve o comportamento da matriz de alteração de propriedade.<br/>                                                                                                                                                                                                                                                                                                                                       |
| [**TIPO DE \_ AGREGAÇÃO \_ PROPDESC**](/windows/win32/api/propsys/ne-propsys-propdesc_aggregation_type)                 | Descreve como os valores de propriedade são exibidos quando vários itens são selecionados. Para uma propriedade específica, PROPDESC AGGREGATION TYPE descreve como a propriedade deve ser exibida quando vários itens que têm um valor para a propriedade são selecionados, como se os valores devem ser somados ou médios ou apenas exibidos com a cadeia de \_ \_ caracteres padrão "Vários Valores".<br/> |
| [**TIPO PROPDESC \_ \_ COLUMNINDEX**](/windows/win32/api/propsys/ne-propsys-propdesc_columnindex_type)                 | Indica se ou como uma propriedade pode ser indexada.<br/>                                                                                                                                                                                                                                                                                                                             |
| [**TIPO DE \_ CONDIÇÃO \_ PROPDESC**](/windows/win32/api/propsys/ne-propsys-propdesc_condition_type)                     | Descreve o tipo de condição a ser usado ao exibir a propriedade na interface do usuário do construtor de consultas no Windows Vista, mas não no Windows 7 e posteriores.<br/>                                                                                                                                                                                                                                      |
| [**PROPDESC \_ ENUMFILTER**](/windows/win32/api/propsys/ne-propsys-propdesc_enumfilter)                              | Descreve a lista filtrada de descrições de propriedade retornadas.<br/>                                                                                                                                                                                                                                                                                                          |
| [**SINALIZADORES DE FORMATO \_ PROPDESC \_**](/windows/win32/api/propsys/ne-propsys-propdesc_format_flags)                         | Usado por funções auxiliares de descrição da propriedade, como [**PSFormatForDisplay,**](/windows/win32/api/propsys/nf-propsys-psformatfordisplay)para indicar o formato de uma cadeia de caracteres de propriedade.<br/>                                                                                                                                                                                                                         |
| [**TIPO \_ PROPDESC \_ RELATIVEDESCRIPTION**](/windows/win32/api/propsys/ne-propsys-propdesc_relativedescription_type) | Descreve o tipo de descrição relativa para uma descrição da propriedade, conforme determinado pelo atributo *relativeDescriptionType* do [elemento displayInfo.](./propdesc-schema-displayinfo.md)<br/>                                                                                                                                                                                   |
| [**SINALIZADORES \_ DE PROPDESC SEARCHINFO \_**](/windows/win32/api/propsys/ne-propsys-propdesc_searchinfo_flags)                 | Determina se e como uma propriedade é indexada por Windows Search.<br/>                                                                                                                                                                                                                                                                                                             |
| [**SINALIZADORES DE \_ TIPO PROPDESC \_**](/windows/win32/api/propsys/ne-propsys-propdesc_type_flags)                             | Descreve atributos do [elemento typeInfo](./propdesc-schema-typeinfo.md) no arquivo .propdesc da propriedade.<br/>                                                                                                                                                                                                                                                                |
| [**SINALIZADORES DE \_ EXIBIÇÃO \_ PROPDESC**](/windows/win32/api/propsys/ne-propsys-propdesc_view_flags)                             | Esses sinalizadores descrevem propriedades nas cadeias de caracteres de lista de descrição da propriedade.<br/>                                                                                                                                                                                                                                                                                                           |
| [**SINALIZADORES \_ PROPERTYUI**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_propertyui_flags)                                    | Especifica os recursos de propriedade.<br/>                                                                                                                                                                                                                                                                                                                                                    |
| [**UNIDADE DE \_ COMPARAÇÃO PROPVAR \_**](/windows/win32/api/propvarutil/ne-propvarutil-propvar_compare_unit)                           | Esses sinalizadores estão associados a determinadas [**comparações de estrutura PROPVARIANT.**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)<br/>                                                                                                                                                                                                                                                                               |
| [**ESTADO \_ do PSC**](/windows/win32/api/propsys/ne-propsys-psc_state)                                                  | Especifica o estado de uma propriedade. Eles são definidos manualmente pelo código que está hospedando o cache do armazenamento de propriedades na memória.<br/>                                                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Propriedades do Windows](props.md)
</dt> <dt>

[Esquema de descrição da propriedade](property-description-schema.md)
</dt> <dt>

[Conjuntos de propriedades](property-sets.md)
</dt> <dt>

[Interfaces](interfaces.md)
</dt> <dt>

[Funções](functions.md)
</dt> <dt>

[Estruturas](structures.md)
</dt> </dl>

 

 
