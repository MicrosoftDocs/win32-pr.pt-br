---
title: Implementação de IPropertyStorage-Stand-alone
description: A implementação do IPropertySetStorage fornecida pelo sistema e autônomo inclui uma implementação de IPropertyStorage, a interface que lê e grava propriedades em um armazenamento de conjunto de propriedades.
ms.assetid: 8de32538-de11-4e4d-9269-145b2accb099
keywords:
- Implementação de IPropertyStorage-Stand-alone
- IPropertyStorage Strctd Stg , implementações, autônomo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 200d7f328670b8945807b7db7f742feabe58ad32847e3c56aa98a34278a71fbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119662546"
---
# <a name="ipropertystorage-stand-alone-implementation"></a>Implementação de IPropertyStorage-Stand-alone

A implementação do [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) fornecida pelo sistema e autônomo inclui uma implementação de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), a interface que lê e grava propriedades em um armazenamento de conjunto de propriedades. A interface **IPropertySetStorage** cria e abre conjuntos de propriedades em um armazenamento. As interfaces [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) e [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) também são fornecidas na implementação autônomo.

Para obter um ponteiro para a implementação autônomo de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), chame a função [**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) para criar um novo conjunto de propriedades ou [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) para obter o ponteiro de interface em um conjunto de propriedades existente (ou chame os métodos [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) ou [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) da implementação autônomo [**IPropertySetStorage).**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)

A implementação autônomo de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) cria conjuntos de propriedades em qualquer objeto de armazenamento ou fluxo, não apenas em fluxos e armazenamentos de arquivos compostos. A implementação autônomo não depende de arquivos compostos e pode ser usada com qualquer implementação de armazenamentos estruturados. Para obter mais informações sobre a implementação de arquivo composto dessa interface, consulte [IPropertyStorage-Compound File Implementation](ipropertystorage-compound-file-implementation.md).

## <a name="when-to-use"></a>Quando usar

Use [**IPropertyStorage para**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) gerenciar propriedades em um único conjunto de propriedades. Seus métodos suportam ler, escrever e excluir propriedades e os nomes de cadeia de caracteres opcionais que podem ser associados a IDs de propriedade. Outros métodos suportam as operações padrão de confirmação e reversão de armazenamento. Também há um método que define os tempos associados ao armazenamento de propriedades e outro que permite que a atribuição de um CLSID seja usada para associar outro código, como o código de interface do usuário, ao conjunto de propriedades. O [**método Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) fornece um ponteiro para a implementação autônomo de [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg), que enumera as propriedades no conjunto.

## <a name="version-0-and-version-1-property-set-formats"></a>Formatos de conjunto de propriedades das versões 0 e 1

A implementação autônomo de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) dá suporte aos formatos de serialização da versão 0 e do conjunto de propriedades da versão 1. Para obter mais informações, consulte [Serialização do conjunto de propriedades](version-0-vs--version-1-property-set-serialization.md). Os conjuntos de propriedades são criados no formato versão 0 e permanecem nesse formato, a menos que novos recursos sejam solicitados. Nesse momento, o formato é atualizado para a versão 1.

Por exemplo, se um conjunto de propriedades for criado com o sinalizador PROPSETFLAG \_ DEFAULT, seu formato será a versão 0. Desde que os tipos de propriedade que estão em conformidade com o formato da versão 0 sejam gravados e lidos desse conjunto de propriedades, o conjunto de propriedades permanecerá no formato versão 0. Se um tipo de propriedade versão 1 for gravado no conjunto de propriedades, o conjunto de propriedades será atualizado automaticamente para a versão 1. Posteriormente, esse conjunto de propriedades não pode mais ser lido por implementações que só entendem a versão 0.

## <a name="ipropertystorage-and-variant-types"></a>Tipos IPropertyStorage e Variant

A implementação autônomo de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) não dá suporte aos tipos variantes VT UNKNOWN ou VT DISPATCH no membro vt da \_ estrutura \_ [**PROPVARIANT.**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) 

Os seguintes tipos de variantes têm suporte em um SafeArray; ou seja, esses valores podem ser combinados com VT \_ ARRAY no **membro vt** da [**estrutura PROPVARIANT.**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)



Tipos variantes com suporte no SafeArray pela implementação de arquivo composto [ **de IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)

VT \_ I1

VT \_ UI1

VT \_ I2

VT \_ UI2

VT \_ I4

VT \_ UI4

VT \_ INT

UINT \_ da VT

VT \_ R4

VT \_ R8

VT \_ CY

DATA \_ DA VT

VT \_ BSTR

BOOL da VT \_

DECIMAL \_ da VT

ERRO \_ DA VT

VARIANTE \_ DA VT

 



 

Quando a VT \_ VARIANT é combinada com o VT \_ ARRAY, o SafeArray em si contém [**estruturas PROPVARIANT.**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) No entanto, os tipos desses elementos devem ser retirados da lista anterior, não podem ser VT VARIANT e não podem incluir os indicadores \_ VT \_ VECTOR, VT ARRAY ou \_ VT \_ BYREF.

## <a name="ipropertystorage-methods"></a>Métodos IPropertyStorage

A implementação autônomo de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) dá suporte aos seguintes métodos:

<dl> <dt>

<span id="IPropertyStorage__ReadMultiple"></span><span id="ipropertystorage__readmultiple"></span><span id="IPROPERTYSTORAGE__READMULTIPLE"></span>[**IPropertyStorage::ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple)
</dt> <dd>

Lê as propriedades especificadas na matriz *rgpspec* e fornece os valores de todas as propriedades válidas na matriz *rgvar* de [**elementos PROPVARIANT.**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)

Na implementação do sistema, autônomo, identificadores de propriedade duplicados que se referem a tipos de armazenamento ou fluxo resultam em várias chamadas para [**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) ou [**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) e o sucesso ou falha do [**ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) depende da capacidade da implementação de armazenamento subjacente de compartilhar armazenamentos abertos.

Além disso, para garantir a operação thread-safe se a mesma propriedade com valor de armazenamento ou fluxo for solicitada várias vezes por meio do mesmo ponteiro [**IPropertyStorage,**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) a abertura terá êxito ou falhará dependendo se a propriedade já estiver aberta ou não e se o sistema de arquivos subjacente tratará várias aberturas de um fluxo ou armazenamento. Portanto, a operação [**ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) em uma propriedade com valor de armazenamento ou fluxo sempre resulta em uma chamada para [**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream)ou [**IStorage::OpenStorage,**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage)passando os valores de acesso (STGM READWRITE, por exemplo) e compartilhamento \_ (STGM SHARE EXCLUSIVE, por exemplo) especificados quando o conjunto de propriedades foi originalmente aberto ou \_ \_ criado.

Se o método falhar, os valores gravados em *rgvar* \[ \] serão indefinido. Se algumas propriedades com valor de armazenamento ou fluxo são abertas com êxito, mas ocorre um erro antes que a execução seja concluída, essas propriedades devem ser liberadas antes que o método retorne.

</dd> <dt>

<span id="IPropertyStorage__WriteMultiple"></span><span id="ipropertystorage__writemultiple"></span><span id="IPROPERTYSTORAGE__WRITEMULTIPLE"></span>[**IPropertyStorage::WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple)
</dt> <dd>

Grava as propriedades especificadas na *matriz rgpspec,* atribuindo a elas as marcas e valores \[ \] [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) especificados em *rgvar* \[ \] . As propriedades que já existem são atribuídas aos valores **PROPVARIANT** especificados e as propriedades que não existem atualmente são criadas.

</dd> <dt>

<span id="IPropertyStorage__DeleteMultiple"></span><span id="ipropertystorage__deletemultiple"></span><span id="IPROPERTYSTORAGE__DELETEMULTIPLE"></span>[**IPropertyStorage::D eleteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletemultiple)
</dt> <dd>

Exclui as propriedades especificadas no *rgpspec* \[ \] .

</dd> <dt>

<span id="IPropertyStorage__ReadPropertyNames"></span><span id="ipropertystorage__readpropertynames"></span><span id="IPROPERTYSTORAGE__READPROPERTYNAMES"></span>[**IPropertyStorage::ReadPropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readpropertynames)
</dt> <dd>

Lê os nomes de cadeia de caracteres existentes associados às IDs de propriedade especificadas na *matriz rgpropid.* \[ \]

</dd> <dt>

<span id="IPropertyStorage__WritePropertyNames"></span><span id="ipropertystorage__writepropertynames"></span><span id="IPROPERTYSTORAGE__WRITEPROPERTYNAMES"></span>[**IPropertyStorage::WritePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writepropertynames)
</dt> <dd>

Atribui nomes de cadeia de caracteres especificados na matriz *rglpwstrName* às IDs de propriedade especificadas na *matriz rgpropid.*

</dd> <dt>

<span id="IPropertyStorage__DeletePropertyNames"></span><span id="ipropertystorage__deletepropertynames"></span><span id="IPROPERTYSTORAGE__DELETEPROPERTYNAMES"></span>[**IPropertyStorage::D eletePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletepropertynames)
</dt> <dd>

Exclui os nomes de cadeia de caracteres das IDs de propriedade especificadas na *matriz rgpropid* escrevendo **NULL** no nome da propriedade.

</dd> <dt>

<span id="IPropertyStorage__SetClass"></span><span id="ipropertystorage__setclass"></span><span id="IPROPERTYSTORAGE__SETCLASS"></span>[**IPropertyStorage::SetClass**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-setclass)
</dt> <dd>

Define o **CLSID do** fluxo do conjunto de propriedades. Na implementação autônomo, definir o CLSID em um conjunto de propriedades não simples (um que pode conter propriedades com valor de armazenamento ou de fluxo, conforme descrito em [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)) também define o CLSID no substorage subjacente para que ele possa ser obtido por meio de uma chamada para [**IStorage::Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat).

</dd> <dt>

<span id="IPropertyStorage__Commit"></span><span id="ipropertystorage__commit"></span><span id="IPROPERTYSTORAGE__COMMIT"></span>[**IPropertyStorage::Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit)
</dt> <dd>

Para conjuntos de propriedades simples e não simples, libera a imagem de memória para o subsistema de disco. Além disso, para conjuntos de propriedades de modo transacionado não simples, esse método chama [**IStorage::Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) no conjunto de propriedades.

</dd> <dt>

<span id="IPropertyStorage__Revert"></span><span id="ipropertystorage__revert"></span><span id="IPROPERTYSTORAGE__REVERT"></span>[**IPropertyStorage::Revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert)
</dt> <dd>

Somente para conjuntos de propriedades não simples, chama o método [**Revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert) do armazenamento subjacente e reabre o fluxo 'contents'. Para conjuntos de propriedades simples, retorna apenas E \_ OK.

</dd> <dt>

<span id="IPropertyStorage__Enum"></span><span id="ipropertystorage__enum"></span><span id="IPROPERTYSTORAGE__ENUM"></span>[**IPropertyStorage::Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum)
</dt> <dd>

Cria um objeto enumerador que implementa [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg), os métodos dos quais podem ser chamados para enumerar as estruturas [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) que fornecem informações sobre cada uma das propriedades no conjunto.

Essa implementação cria uma matriz na qual todo o conjunto de propriedades é lido e que pode ser compartilhado quando [**IEnumSTATPROPSTG::Clone**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) é chamado.

</dd> <dt>

<span id="IPropertyStorage__Stat"></span><span id="ipropertystorage__stat"></span><span id="IPROPERTYSTORAGE__STAT"></span>[**IPropertyStorage::Stat**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-stat)
</dt> <dd>

Preenche os membros de uma estrutura [**STATPROPSETSTG,**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) que contém informações sobre o conjunto de propriedades como um todo. No retorno, fornece um ponteiro para a estrutura.

Para conjuntos de armazenamento não simples, essa implementação chama [**IStorage::Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) [**(ou IStream::Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)) para obter as informações do armazenamento ou fluxo subjacente.

</dd> <dt>

<span id="IPropertyStorage__SetTimes"></span><span id="ipropertystorage__settimes"></span><span id="IPROPERTYSTORAGE__SETTIMES"></span>[**IPropertyStorage::SetTimes**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes)
</dt> <dd>

Somente para conjuntos de propriedades não simples, define os horários com suporte do armazenamento subjacente. Essa implementação de [**SetTimes**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes) chama o [**método IStorage::SetElementTimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes) do armazenamento subjacente para modificar os horários. Ele dá suporte aos horários com suporte pelo método subjacente, que podem ser o tempo de modificação, a hora de acesso ou a hora de criação.

</dd> </dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Implementação de IPropertySetStorage-Stand-alone](ipropertysetstorage-stand-alone-implementation.md)
</dt> <dt>

[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[**IStorage::SetElementTimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes)
</dt> <dt>

[**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg)
</dt> <dt>

[**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg)
</dt> <dt>

[**StgCreatePropSetStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg)
</dt> </dl>

 

 