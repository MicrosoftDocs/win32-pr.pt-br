---
title: Implementação IPropertyStorage-autônoma
description: A implementação autônoma fornecida pelo sistema do IPropertySetStorage inclui uma implementação de IPropertyStorage, a interface que lê e grava Propriedades em um armazenamento de conjunto de propriedades.
ms.assetid: 8de32538-de11-4e4d-9269-145b2accb099
keywords:
- Implementação IPropertyStorage-autônoma
- IPropertyStorage Strctd STG, implementações, autônoma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f35965831b0105557044461236030e3543c13217
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366183"
---
# <a name="ipropertystorage-stand-alone-implementation"></a>Implementação IPropertyStorage-autônoma

A implementação autônoma fornecida pelo sistema do [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) inclui uma implementação de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), a interface que lê e grava Propriedades em um armazenamento de conjunto de propriedades. A interface **IPropertySetStorage** cria e abre conjuntos de propriedades em um armazenamento. As interfaces [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) e [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) também são fornecidas na implementação autônoma.

Para obter um ponteiro para a implementação autônoma de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), chame a função [**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) para criar um novo conjunto de propriedades ou [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) para obter o ponteiro de interface em um conjunto de propriedades existente (ou chamar os métodos [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) ou [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) da implementação autônoma [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) ).

A implementação autônoma do [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) cria conjuntos de propriedades em qualquer objeto de armazenamento ou fluxo, não apenas em armazenamentos de arquivos compostos e fluxos. A implementação autônoma não depende de arquivos compostos e pode ser usada com qualquer implementação de armazenamentos estruturados. Para obter mais informações sobre a implementação de arquivo composto dessa interface, consulte [implementação de arquivo composto IPropertyStorage](ipropertystorage-compound-file-implementation.md).

## <a name="when-to-use"></a>Quando usar

Use [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) para gerenciar Propriedades em um único conjunto de propriedades. Seus métodos dão suporte à leitura, gravação e exclusão de propriedades e aos nomes de cadeia de caracteres opcionais que podem ser associados a IDs de propriedade. Outros métodos dão suporte às operações de confirmação e de reversão de armazenamento padrão. Também há um método que define os horários associados ao armazenamento de propriedades e outro que permite que a atribuição de um CLSID seja usada para associar outro código, como o código de interface do usuário, com o conjunto de propriedades. O método [**enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) fornece um ponteiro para a implementação autônoma de [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg), que enumera as propriedades no conjunto.

## <a name="version-0-and-version-1-property-set-formats"></a>Formatos de conjunto de propriedades versão 0 e versão 1

A implementação autônoma do [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) dá suporte aos formatos de serialização da versão 0 e do conjunto de propriedades da versão 1. Para obter mais informações, consulte [serialização do conjunto de propriedades](version-0-vs--version-1-property-set-serialization.md). Os conjuntos de propriedades são criados no formato da versão 0 e permanecem nesse formato, a menos que novos recursos sejam solicitados. Nesse momento, o formato é atualizado para a versão 1.

Por exemplo, se um conjunto de Propriedades for criado com o \_ sinalizador padrão PROPSETFLAG, seu formato será a versão 0. Desde que os tipos de propriedade que estejam em conformidade com o formato da versão 0 sejam gravados e lidos a partir desse conjunto de propriedades, o conjunto de propriedades permanecerá no formato da versão 0. Se um tipo de propriedade da versão 1 for gravado no conjunto de propriedades, o conjunto de propriedades será atualizado automaticamente para a versão 1. Subsequentemente, esse conjunto de propriedades não pode mais ser lido por implementações que entendem apenas a versão 0.

## <a name="ipropertystorage-and-variant-types"></a>Tipos de IPropertyStorage e variantes

A implementação autônoma de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) não dá suporte à expedição de tipos Variant VT \_ Unknown ou VT \_ no membro **VT** da estrutura [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .

Os tipos variantes a seguir têm suporte em um SafeArray; ou seja, esses valores podem ser combinados com \_ a matriz VT no membro **VT** da estrutura [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .



Tipos de variante com suporte em SafeArray por implementação de arquivo composto de [ **IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)

VT \_ i1

\_UI1 VT

\_I2 VT

\_UI2 VT

\_I4 VT

\_UI4 VT

VT \_ int

VT \_ uint

VT \_ R4

R8 de VT \_

VT \_ Cy

Data de VT \_

VT \_ BSTR

BOOL do VT \_

\_decimal VT

erro de VT \_

variante do VT \_

 



 

Quando \_ a variante VT é combinada com \_ a matriz VT, o SAFEARRAY em si mantém as estruturas [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) . No entanto, os tipos desses elementos devem ser extraídos da lista anterior, não pode ser VT \_ Variant e não podem incluir os \_ indicadores de vetor VT, VT \_ array ou VT \_ ByRef.

## <a name="ipropertystorage-methods"></a>Métodos IPropertyStorage

A implementação autônoma do [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) dá suporte aos seguintes métodos:

<dl> <dt>

<span id="IPropertyStorage__ReadMultiple"></span><span id="ipropertystorage__readmultiple"></span><span id="IPROPERTYSTORAGE__READMULTIPLE"></span>[**IPropertyStorage::ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple)
</dt> <dd>

Lê as propriedades especificadas na matriz *rgpspec* e fornece os valores de todas as propriedades válidas na matriz *rgVar* de elementos [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .

Na implementação autônoma fornecida pelo sistema, os identificadores de propriedade duplicados que se referem aos tipos de fluxo/armazenamento resultam em várias chamadas para [**IStorage:: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) ou [**IStorage:: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) e o êxito ou a falha de [**ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) depende da capacidade da implementação de armazenamento subjacente para compartilhar armazenamentos abertos.

Além disso, para garantir a operação thread-safe se a mesma propriedade com valor de fluxo ou de armazenamento for solicitada várias vezes pelo mesmo ponteiro [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) , a abertura terá êxito ou falhará dependendo se a propriedade já estiver aberta e se o sistema de arquivos subjacente lida com várias aberturas de um fluxo ou armazenamento. Assim, a operação [**ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) em uma propriedade com valor de fluxo ou de armazenamento sempre resulta em uma chamada para [**IStorage:: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream)ou [**IStorage:: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage), passando o acesso (STGM \_ ReadWrite, por exemplo) e valores de compartilhamento (STGM \_ compartilhamento \_ exclusivo, por exemplo) especificado quando o conjunto de propriedades foi originalmente aberto ou criado.

Se o método falhar, os valores gravados em *rgVar* \[ \] serão indefinidos. Se algumas propriedades de fluxo ou de valor de armazenamento forem abertas com êxito, mas ocorrer um erro antes da execução ser concluída, essas propriedades deverão ser liberadas antes que o método seja retornado.

</dd> <dt>

<span id="IPropertyStorage__WriteMultiple"></span><span id="ipropertystorage__writemultiple"></span><span id="IPROPERTYSTORAGE__WRITEMULTIPLE"></span>[**IPropertyStorage::WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple)
</dt> <dd>

Grava as propriedades especificadas na matriz *rgpspec* \[ \] , atribuindo a elas as marcas e os valores de [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) especificados em *rgVar* \[ \] . As propriedades que já existem são atribuídas aos valores **PROPVARIANT** especificados, e as propriedades que não existem atualmente são criadas.

</dd> <dt>

<span id="IPropertyStorage__DeleteMultiple"></span><span id="ipropertystorage__deletemultiple"></span><span id="IPROPERTYSTORAGE__DELETEMULTIPLE"></span>[**IPropertyStorage::D eleteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletemultiple)
</dt> <dd>

Exclui as propriedades especificadas em *rgpspec* \[ \] .

</dd> <dt>

<span id="IPropertyStorage__ReadPropertyNames"></span><span id="ipropertystorage__readpropertynames"></span><span id="IPROPERTYSTORAGE__READPROPERTYNAMES"></span>[**IPropertyStorage::ReadPropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readpropertynames)
</dt> <dd>

Lê os nomes de cadeia de caracteres existentes associados às IDs de propriedade especificadas na matriz *rgPropID* \[ \] .

</dd> <dt>

<span id="IPropertyStorage__WritePropertyNames"></span><span id="ipropertystorage__writepropertynames"></span><span id="IPROPERTYSTORAGE__WRITEPROPERTYNAMES"></span>[**IPropertyStorage::WritePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writepropertynames)
</dt> <dd>

Atribui nomes de cadeia de caracteres especificados na matriz *rglpwstrName* às IDs de propriedade especificadas na matriz *rgPropID* .

</dd> <dt>

<span id="IPropertyStorage__DeletePropertyNames"></span><span id="ipropertystorage__deletepropertynames"></span><span id="IPROPERTYSTORAGE__DELETEPROPERTYNAMES"></span>[**IPropertyStorage::D eletePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletepropertynames)
</dt> <dd>

Exclui os nomes de cadeia de caracteres das IDs de propriedade especificadas na matriz *rgPropID* gravando **NULL** no nome da propriedade.

</dd> <dt>

<span id="IPropertyStorage__SetClass"></span><span id="ipropertystorage__setclass"></span><span id="IPROPERTYSTORAGE__SETCLASS"></span>[**IPropertyStorage:: SetClass**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-setclass)
</dt> <dd>

Define o **CLSID** do fluxo do conjunto de propriedades. Na implementação autônoma, definir o CLSID em um conjunto de propriedades não simples (um que pode conter Propriedades com valor de armazenamento ou de fluxo, conforme descrito em [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)) também define o CLSID no subarmazenamento subjacente para que ele possa ser obtido por meio de uma chamada para [**IStorage:: stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat).

</dd> <dt>

<span id="IPropertyStorage__Commit"></span><span id="ipropertystorage__commit"></span><span id="IPROPERTYSTORAGE__COMMIT"></span>[**IPropertyStorage:: Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit)
</dt> <dd>

Para os conjuntos de propriedades simples e não simples, o libera a imagem de memória para o subsistema de disco. Além disso, para conjuntos de propriedades de modo transacionado não simples, esse método chama [**IStorage:: Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) no conjunto de propriedades.

</dd> <dt>

<span id="IPropertyStorage__Revert"></span><span id="ipropertystorage__revert"></span><span id="IPROPERTYSTORAGE__REVERT"></span>[**IPropertyStorage:: Revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert)
</dt> <dd>

Somente para conjuntos de propriedades não simples, o chama o método [**REVERT**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert) do armazenamento subjacente e reabre o fluxo ' Contents '. Para conjuntos de propriedades simples, retorna apenas E \_ OK.

</dd> <dt>

<span id="IPropertyStorage__Enum"></span><span id="ipropertystorage__enum"></span><span id="IPROPERTYSTORAGE__ENUM"></span>[**IPropertyStorage:: enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum)
</dt> <dd>

Cria um objeto enumerador que implementa [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg), os métodos que podem ser chamados para enumerar as estruturas [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) que fornecem informações sobre cada uma das propriedades no conjunto.

Essa implementação cria uma matriz na qual o conjunto de propriedades inteiro é lido e que pode ser compartilhado quando [**IEnumSTATPROPSTG:: clone**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) é chamado.

</dd> <dt>

<span id="IPropertyStorage__Stat"></span><span id="ipropertystorage__stat"></span><span id="IPROPERTYSTORAGE__STAT"></span>[**IPropertyStorage:: stat**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-stat)
</dt> <dd>

Preenche os membros de uma estrutura [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) , que contém informações sobre o conjunto de propriedades como um todo. No retorno, fornece um ponteiro para a estrutura.

Para conjuntos de armazenamento não simples, essa implementação chama [**IStorage:: stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) (ou [**IStream:: stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)) para obter as informações do armazenamento ou fluxo subjacente.

</dd> <dt>

<span id="IPropertyStorage__SetTimes"></span><span id="ipropertystorage__settimes"></span><span id="IPROPERTYSTORAGE__SETTIMES"></span>[**IPropertyStorage:: settimes**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes)
</dt> <dd>

Somente para conjuntos de propriedades não simples, o define os tempos suportados pelo armazenamento subjacente. Essa implementação de [**Settimes**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes) chama o método [**IStorage:: SetElementTimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes) do armazenamento subjacente para modificar os horários. Ele dá suporte às horas com suporte pelo método subjacente que pode ser tempo de modificação, hora de acesso ou hora de criação.

</dd> </dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Implementação IPropertySetStorage-autônoma](ipropertysetstorage-stand-alone-implementation.md)
</dt> <dt>

[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[**IStorage:: SetElementTimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes)
</dt> <dt>

[**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg)
</dt> <dt>

[**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg)
</dt> <dt>

[**StgCreatePropSetStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg)
</dt> </dl>

 

 