---
description: Esta seção descreve as constantes, enumerações e sinalizadores do sistema de propriedades do Windows.
ms.assetid: ff735b9c-e444-4e6f-8e80-0b2a5d770386
title: Constantes, enumerações e sinalizadores (sistema de propriedades do Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8681c773181b69b24b1fe2d01d380d730c33e220
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169746"
---
# <a name="constants-enumerations-and-flags"></a>Constantes, enumerações e sinalizadores

Esta seção descreve as constantes, enumerações e sinalizadores do sistema de propriedades do Windows.



| Tópico                                                                              | Sumário                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GETPROPERTYSTOREFLAGS**](/windows/desktop/api/Propsys/ne-propsys-getpropertystoreflags)                             | Indica sinalizadores que modificam o objeto de repositório de propriedades recuperado por métodos que criam um repositório de propriedades, como [**IShellItem2:: GetPropertyStore**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellitem2-getpropertystore) ou [**IPropertyStoreFactory:: GetPropertyStore**](/windows/win32/api/propsys/nf-propsys-ipropertystorefactory-getpropertystore).<br/>                                                                                        |
| [**PDOPSTATUS**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-pdopstatus)                                                 | Fornece sinalizadores de status de operação.<br/>                                                                                                                                                                                                                                                                                                                                                |
| [**sinalizadores de PKA \_**](/windows/win32/api/propsys/ne-propsys-pka_flags)                                                  | Descreve o comportamento da matriz de alteração de propriedade.<br/>                                                                                                                                                                                                                                                                                                                                       |
| [**\_tipo de agregação PROPDESC \_**](/windows/win32/api/propsys/ne-propsys-propdesc_aggregation_type)                 | Descreve como os valores de propriedade são exibidos quando vários itens são selecionados. Para uma propriedade específica, o \_ tipo de agregação PROPDESC \_ descreve como a propriedade deve ser exibida quando vários itens que têm um valor para a propriedade são selecionados, por exemplo, se os valores devem ser somados ou ser calculados com a cadeia de caracteres "múltiplos valores" padrão.<br/> |
| [**\_tipo de COLUMNINDEX PROPDESC \_**](/windows/win32/api/propsys/ne-propsys-propdesc_columnindex_type)                 | Indica se uma propriedade pode ou não ser indexada.<br/>                                                                                                                                                                                                                                                                                                                             |
| [**\_tipo de condição PROPDESC \_**](/windows/win32/api/propsys/ne-propsys-propdesc_condition_type)                     | Descreve o tipo de condição a ser usado ao exibir a propriedade na interface do usuário do construtor de consultas no Windows Vista, mas não no Windows 7 e posterior.<br/>                                                                                                                                                                                                                                      |
| [**PROPDESC \_ ENUMFILTER**](/windows/win32/api/propsys/ne-propsys-propdesc_enumfilter)                              | Descreve a lista filtrada de descrições de propriedade que é retornada.<br/>                                                                                                                                                                                                                                                                                                          |
| [**\_sinalizadores de formato PROPDESC \_**](/windows/win32/api/propsys/ne-propsys-propdesc_format_flags)                         | Usado pelas funções auxiliares de descrição de propriedade, como [**PSFormatForDisplay**](/windows/win32/api/propsys/nf-propsys-psformatfordisplay), para indicar o formato de uma cadeia de caracteres de propriedade.<br/>                                                                                                                                                                                                                         |
| [**\_tipo de RELATIVEDESCRIPTION PROPDESC \_**](/windows/win32/api/propsys/ne-propsys-propdesc_relativedescription_type) | Descreve o tipo de descrição relativa para uma descrição de propriedade, conforme determinado pelo atributo *relativeDescriptionType* do elemento [DisplayInfo](./propdesc-schema-displayinfo.md) .<br/>                                                                                                                                                                                   |
| [**\_sinalizadores PROPDESC SEARCHINFO \_**](/windows/win32/api/propsys/ne-propsys-propdesc_searchinfo_flags)                 | Determina se e como uma propriedade é indexada pelo Windows Search.<br/>                                                                                                                                                                                                                                                                                                             |
| [**\_sinalizadores de tipo PROPDESC \_**](/windows/win32/api/propsys/ne-propsys-propdesc_type_flags)                             | Descreve os atributos do elemento [TypeInfo](./propdesc-schema-typeinfo.md) no arquivo. propDesc da propriedade.<br/>                                                                                                                                                                                                                                                                |
| [**\_sinalizadores de exibição do PROPDESC \_**](/windows/win32/api/propsys/ne-propsys-propdesc_view_flags)                             | Esses sinalizadores descrevem as propriedades nas cadeias de caracteres da lista de descrição de propriedade.<br/>                                                                                                                                                                                                                                                                                                           |
| [**sinalizadores de PROPERTYUI \_**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_propertyui_flags)                                    | Especifica os recursos de propriedade.<br/>                                                                                                                                                                                                                                                                                                                                                    |
| [**PROPVAR \_ comparar \_ unidade**](/windows/win32/api/propvarutil/ne-propvarutil-propvar_compare_unit)                           | Esses sinalizadores são associados a determinadas comparações de estrutura [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .<br/>                                                                                                                                                                                                                                                                               |
| [**Estado do PSC \_**](/windows/win32/api/propsys/ne-propsys-psc_state)                                                  | Especifica o estado de uma propriedade. Eles são definidos manualmente pelo código que está hospedando o cache do repositório de propriedades na memória.<br/>                                                                                                                                                                                                                                                        |



 

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

 

 
