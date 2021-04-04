---
title: Implementação IPropertySetStorage-autônoma
description: A implementação autônoma fornecida pelo sistema do IPropertySetStorage inclui uma implementação de IPropertyStorage e IPropertySetStorage.
ms.assetid: 0ea5aadf-0b3f-44ac-9bb7-a7e8292f04c2
keywords:
- IPropertySetStorage Strctd STG, implementações
- IPropertySetStorage Strctd STG, implementações, autônoma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f9fd0afe31775b06b3a5f61f4c79939be976e98
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007655"
---
# <a name="ipropertysetstorage-stand-alone-implementation"></a>Implementação IPropertySetStorage-autônoma

A implementação autônoma fornecida pelo sistema do [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) inclui uma implementação de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) e **IPropertySetStorage**. [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) é a interface que lê e grava Propriedades em um armazenamento de conjunto de propriedades. [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) é a interface que cria e abre conjuntos de propriedades em um armazenamento. As interfaces [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) e [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) também são fornecidas na implementação autônoma.

Para usar a implementação autônoma do [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage), primeiro obtenha um ponteiro para a implementação autônoma fornecida pelo sistema e associe a implementação fornecida pelo sistema com o objeto de armazenamento. Para obter um ponteiro para a implementação autônoma do **IPropertySetStorage**, chame a função [**StgCreatePropSetStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg) e forneça o parâmetro *pStorage* especificando o objeto de armazenamento que conterá o conjunto de propriedades. Essa função fornece um ponteiro para a nova interface **IPropertySetStorage** para o objeto de armazenamento especificado.

A implementação autônoma do [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) cria conjuntos de propriedades em qualquer objeto de armazenamento, não apenas em armazenamentos de arquivos compostos. A implementação autônoma não depende de arquivos compostos e pode ser usada com qualquer implementação de armazenamentos estruturados. Quaisquer restrições nos armazenamentos estruturados fornecidos pelo chamador se aplicam a essa implementação de conjuntos de propriedades. Por exemplo, se você fornecer um armazenamento de modo simples para [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg), o **IPropertySetStorage** resultante será restringido pelo [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)fornecido.

Para obter mais informações sobre a implementação de arquivo composto dessa interface, consulte a seção [IPropertySetStorage-composição de arquivos](ipropertysetstorage-compound-file-implementation.md).

## <a name="when-to-use"></a>Quando usar

Chame os métodos de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) para criar, abrir e excluir conjuntos de propriedades em qualquer armazenamento estruturado. Também há um método que fornece um ponteiro para o enumerador [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) que pode ser usado para enumerar os conjuntos de propriedades no armazenamento.

A implementação autônoma também fornece as funções auxiliares [**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) e [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) , além dos métodos [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) e [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) , para criar e abrir conjuntos de propriedades. Essas duas funções adicionam suporte para o \_ valor sem buffer PROPSETFLAG para que você possa gravar as alterações diretamente no conjunto de propriedades em vez de armazená-las em um cache. Para obter mais informações, consulte [**constantes PROPSETFLAG**](propsetflag-constants.md).

## <a name="methods"></a>Métodos

A implementação autônoma do [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) dá suporte aos métodos a seguir.

<dl> <dt>

<span id="IPropertySetStorage__Create"></span><span id="ipropertysetstorage__create"></span><span id="IPROPERTYSETSTORAGE__CREATE"></span>[**IPropertySetStorage:: criar**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)
</dt> <dd>

Cria uma nova propriedade definida no armazenamento e retorna um ponteiro para a interface [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) no conjunto de propriedades.

Se você planeja usar o valor sem \_ buffer PROPSETFLAG, use a função [**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) em vez disso para criar e abrir o novo conjunto de propriedades e obter um ponteiro para a implementação autônoma da interface [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) no conjunto de propriedades.

</dd> <dt>

<span id="IPropertySetStorage__Open"></span><span id="ipropertysetstorage__open"></span><span id="IPROPERTYSETSTORAGE__OPEN"></span>[**IPropertySetStorage:: abrir**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)
</dt> <dd>

Abre um conjunto de propriedades existente no armazenamento e retorna um ponteiro para a interface [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) no conjunto de propriedades.

Se você planeja usar o valor sem \_ buffer PROPSETFLAG, use a função [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) em vez disso, para obter um ponteiro para a implementação autônoma de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) no conjunto de propriedades especificado.

</dd> <dt>

<span id="IPropertySetStorage__Delete"></span><span id="ipropertysetstorage__delete"></span><span id="IPROPERTYSETSTORAGE__DELETE"></span>[**IPropertySetStorage::D excluir**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-delete)
</dt> <dd>

Exclui um conjunto de propriedades neste armazenamento de conjunto de propriedades.

</dd> <dt>

<span id="IPropertySetStorage__Enum"></span><span id="ipropertysetstorage__enum"></span><span id="IPROPERTYSETSTORAGE__ENUM"></span>[**IPropertySetStorage:: enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum)
</dt> <dd>

Cria um objeto que pode ser usado para enumerar estruturas [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) . Cada estrutura **STATPROPSETSTG** fornece dados sobre um único conjunto de propriedades.

> [!Note]  
> O conjunto de propriedades DocumentSummaryInformation e UserDefined é exclusivo, pois ele pode ter duas seções de conjunto de propriedades em um único fluxo subjacente. Para obter mais informações, consulte [os conjuntos de propriedades DocumentSummaryInformation e UserDefined](the-documentsummaryinformation-and-userdefined-property-sets.md) .

 

</dd> </dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Implementação IPropertyStorage-autônoma](ipropertystorage-stand-alone-implementation.md)
</dt> <dt>

[**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)
</dt> <dt>

[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[**IStorage:: EnumElements**](/windows/desktop/api/Objidl/nf-objidl-istorage-enumelements)
</dt> <dt>

[**Constantes PROPSETFLAG**](propsetflag-constants.md)
</dt> <dt>

[**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)
</dt> <dt>

[**StgCreatePropSetStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg)
</dt> <dt>

[**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg)
</dt> <dt>

[**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg)
</dt> <dt>

[**Constantes STGM**](stgm-constants.md)
</dt> </dl>

 

 