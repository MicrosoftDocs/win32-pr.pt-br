---
title: Implementação de arquivo de IPropertyStorage-Compound
description: A implementação COM da arquitetura de armazenamento estruturado é chamada de arquivos compostos.
ms.assetid: c4b4f313-de58-44f2-8ce1-a07cc187d8ca
keywords:
- IPropertyStorage Strctd STG, implementações, arquivo composto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03d927b0145077f12e5ba508ca65554ca33633a3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823832"
---
# <a name="ipropertystorage-compound-file-implementation"></a>Implementação de arquivo de IPropertyStorage-Compound

A implementação COM da arquitetura de armazenamento estruturado é chamada de [arquivos compostos](istorage-compound-file-implementation.md). Os objetos de armazenamento conforme implementados em arquivos compostos incluem uma implementação de ambos os [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), a interface que gerencia um único conjunto de propriedades persistentes e [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage), a interface que gerencia grupos de conjuntos de propriedades persistentes. Para obter mais informações sobre a interface **IPropertyStorage** , consulte [Considerações sobre](property-storage-considerations.md) **IPropertyStorage** e armazenamento de propriedades.

Para obter um ponteiro para a implementação do arquivo composto de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), chame [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) para criar um novo objeto de arquivo composto ou [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) para abrir um objeto de arquivo composto criado anteriormente. No caso de **StgCreateStorageEx**, o parâmetro *stgfmt* deve ser definido como armazenamento stgfmt \_ . No caso de **StgOpenStorageEx**, o parâmetro *stgfmt* deve ser definido como stgfmt \_ Storage ou stgfmt \_ any. Em ambos os casos, o parâmetro *riid* deve ser definido como IID \_ IPropertySetStorage. Ambas as funções fornecem um ponteiro para a interface Object [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) . Chamando o método [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) ou [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) dessa interface, você receberá um ponteiro para a interface **IPropertyStorage** , que pode ser usada para chamar qualquer um de seus métodos.

Uma maneira alternativa de obter um ponteiro para a implementação do arquivo composto de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) é chamar as funções [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) e [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) mais antigas ou especificar um parâmetro *riid* de IStorage de IID \_ para a função [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) ou [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) . Em ambos os casos, um ponteiro para a interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) do objeto é retornado. Com os conjuntos de propriedades persistentes, chame [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para a interface **IPropertySetStorage** , especificando o nome definido pelo cabeçalho para o IPropertySetStorage de IID do identificador de interface (IID) \_ .

## <a name="when-to-use"></a>Quando usar

Use [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) para gerenciar Propriedades em um único conjunto de propriedades. Seus métodos dão suporte à leitura, gravação e exclusão de propriedades e aos nomes de cadeia de caracteres opcionais que podem ser associados a identificadores de propriedade. Outros métodos dão suporte às operações de confirmação e de reversão de armazenamento padrão. Também há um método que permite definir os horários associados ao armazenamento de propriedades e outro que permite a atribuição de um CLSID que pode ser usado para associar outro código, como o código de interface do usuário, com o conjunto de propriedades. Chamar o método [**enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) fornece um ponteiro para a implementação do arquivo composto de [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg), que permite enumerar as propriedades no conjunto.

> [!Note]  
> Se você obtiver um ponteiro para [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) chamando [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile), [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex), [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) ou [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) em um armazenamento de conjunto de propriedades de modo simples, os métodos **IPropertyStorage** aderirão às regras de fluxos de modo simples. O armazenamento do conjunto de propriedades é o modo simples se ele foi obtido para um arquivo que foi criado ou aberto com o \_ sinalizador simples STGM. Nesse caso, nem sempre é possível tornar o fluxo subjacente maior e não é possível substituir as propriedades existentes por Propriedades maiores. Para obter mais informações, consulte [implementação de arquivo composto IPropertySetStorage](ipropertysetstorage-compound-file-implementation.md).

 

## <a name="ipropertystorage-and-caching"></a>IPropertyStorage e Caching

A implementação de arquivo composto de caches [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) abre conjuntos de propriedades na memória para melhorar o desempenho. Como resultado, as alterações em um conjunto de propriedades não são gravadas no arquivo composto até que os métodos [**Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) ou **Release** (última referência) sejam chamados.

## <a name="simple-mode-property-sets"></a>Conjuntos de propriedades de modo simples

Um objeto de armazenamento de propriedade estará no modo simples se for criado a partir de um objeto de armazenamento de conjunto de propriedades de modo simples. Por exemplo, um objeto de armazenamento de conjunto de propriedades estaria no modo simples se ele fosse obtido da função [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) , com o \_ sinalizador simples STGM definido no parâmetro *grfMode* . Observe que "modo simples" não está relacionado a "conjuntos de propriedades simples". Um conjunto de propriedades é simples se for criado chamando [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) com o sinalizador de PROPSETFLAG não \_ simples definido no parâmetro *grfFlags* . Para obter mais informações sobre conjuntos de propriedades simples e não simples, consulte [armazenamento e objetos de fluxo para um conjunto de propriedades](storage-vs--stream-for-a-property-set.md).

Quando um objeto de armazenamento de propriedade de modo simples é criado, não há restrições quanto ao seu uso. Quando um objeto de armazenamento de propriedade de modo simples existente é aberto, o objeto de fluxo subjacente que armazena o conjunto de propriedades não pode ser aumentado. Consequentemente, nem sempre é possível modificar tal objeto de armazenamento de propriedade se a alteração exigir um fluxo maior.

## <a name="property-set-formats"></a>Formatos de conjunto de propriedades

A implementação do arquivo composto de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) dá suporte aos formatos de serialização da versão 0 e do conjunto de propriedades da versão 1. Há suporte para o formato versão 1 em computadores que executam o Windows 2000. Para obter mais informações, consulte [serialização do conjunto de propriedades](version-0-vs--version-1-property-set-serialization.md). Os conjuntos de propriedades são criados no formato da versão 0 e permanecem nesse formato, a menos que novos recursos sejam solicitados. Quando isso ocorre, o formato é atualizado para a versão 1.

Por exemplo, se um conjunto de Propriedades for criado com o \_ sinalizador padrão PROPSETFLAG, seu formato será a versão 0. Desde que os tipos de propriedade que estejam em conformidade com o formato da versão 0 sejam gravados e lidos a partir desse conjunto de propriedades, o conjunto de propriedades permanecerá no formato da versão 0. Se um tipo de propriedade da versão 1 for gravado no conjunto de propriedades, o conjunto de propriedades será atualizado automaticamente para a versão 1. Subsequentemente, esse conjunto de propriedades não pode mais ser lido por implementações que reconhecem apenas a versão 0.

## <a name="ipropertystorage-and-variant-types"></a>Tipos de IPropertyStorage e variantes

A implementação do arquivo composto de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) não dá suporte à expedição de tipos Variant VT \_ Unknown ou VT \_ no membro **VT** da estrutura [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .

A tabela a seguir lista os tipos de variante que têm suporte em um SafeArray; ou seja, esses valores podem ser combinados com \_ a matriz VT no membro **VT** da estrutura [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .



Tipos de variante com suporte em SafeArray por implementação de arquivo composto de IPropertyStorage

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

A implementação do arquivo composto do [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) dá suporte aos seguintes métodos:

<dl> <dt>

<span id="IPropertyStorage__ReadMultiple"></span><span id="ipropertystorage__readmultiple"></span><span id="IPROPERTYSTORAGE__READMULTIPLE"></span>[**IPropertyStorage::ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple)
</dt> <dd>

Lê as propriedades especificadas na matriz *rgpspec* e fornece os valores de todas as propriedades válidas na matriz *rgVar* de PROPVARIANTs. Na implementação de arquivo composto COM, os identificadores de propriedade duplicados que se referem aos tipos de fluxo ou de armazenamento resultam em várias chamadas para [**IStorage:: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) ou [**IStorage:: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) e o êxito ou a falha de **ReadMultiple** depende da capacidade da implementação de armazenamento subjacente para compartilhar operações de abertura. Como em um arquivo composto \_ , STGM compartilhamento \_ exclusivo é forçado, várias tentativas abertas falharão. Não há suporte para a abertura do mesmo objeto de armazenamento mais de uma vez no mesmo armazenamento pai. O \_ sinalizador exclusivo de compartilhamento de STGM \_ deve ser especificado.

Além disso, para garantir a operação thread-safe se a mesma propriedade com valor de armazenamento ou fluxo for solicitada várias vezes por meio do mesmo ponteiro [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) na implementação do arquivo composto com, a operação de abertura terá êxito ou falhará dependendo se a propriedade já estiver aberta e se o sistema de arquivos subjacente lida com várias aberturas de um fluxo ou armazenamento. Assim, a operação **ReadMultiple** em uma propriedade com valor de fluxo ou de armazenamento sempre resulta em uma chamada para [**IStorage:: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream)ou [**IStorage:: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage), que passa o acesso (STGM \_ ReadWrite e assim por diante) e sinalizadores de compartilhamento (STGM \_ compartilhamento \_ exclusivo e assim por diante) especificados quando o conjunto de propriedades original foi aberto ou criado.

Se o método falhar, os valores gravados em *rgVar* \[ \] serão indefinidos. Se algumas propriedades de fluxo ou de valor de armazenamento forem abertas com êxito, mas ocorrer um erro antes da execução ser concluída, elas deverão ser liberadas antes que o método seja retornado.

</dd> <dt>

<span id="IPropertyStorage__WriteMultiple"></span><span id="ipropertystorage__writemultiple"></span><span id="IPROPERTYSTORAGE__WRITEMULTIPLE"></span>[**IPropertyStorage::WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple)
</dt> <dd>

Grava as propriedades especificadas na matriz *rgpspec* \[ \] , atribuindo a elas as marcas e os valores de [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) especificados em *rgVar* \[ \] . As propriedades que já existem são atribuídas aos valores **PROPVARIANT** especificados. As propriedades que não existem atualmente são criadas.

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

Exclui os nomes de propriedade das propriedades especificadas na  \[ \] matriz rgPropID.

</dd> <dt>

<span id="IPropertyStorage__SetClass"></span><span id="ipropertystorage__setclass"></span><span id="IPROPERTYSTORAGE__SETCLASS"></span>[**IPropertyStorage:: SetClass**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-setclass)
</dt> <dd>

Define o **CLSID** do fluxo do conjunto de propriedades. Na implementação do arquivo composto, definir o CLSID em um conjunto de propriedades não simples (que pode conter, legalmente, as propriedades com valor de armazenamento ou de fluxo, conforme descrito em [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)) também define o CLSID no subarmazenamento subjacente para que ele possa ser obtido por meio de uma chamada para [**IStorage:: stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat).

</dd> <dt>

<span id="IPropertyStorage__Commit"></span><span id="ipropertystorage__commit"></span><span id="IPROPERTYSTORAGE__COMMIT"></span>[**IPropertyStorage:: Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit)
</dt> <dd>

Para os conjuntos de propriedades simples e não simples, o libera a imagem do conjunto de propriedades para o armazenamento subjacente. Além disso, para conjuntos de propriedades de modo transacionado não simples, esse método executa uma confirmação (como em [**IStorage:: Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit)) no armazenamento que contém o conjunto de propriedades.

</dd> <dt>

<span id="IPropertyStorage__Revert"></span><span id="ipropertystorage__revert"></span><span id="IPROPERTYSTORAGE__REVERT"></span>[**IPropertyStorage:: Revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert)
</dt> <dd>

Somente para conjuntos de propriedades não simples, o chama o método [**REVERT**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert) do armazenamento subjacente e reabre o fluxo ' Contents '. Para conjuntos de propriedades simples, essa interface sempre retorna S \_ OK. Os conjuntos de propriedades não simples são aqueles que foram criados usando o sinalizador PROPSETFLAG não \_ simples no método [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) . Para obter mais informações, consulte [armazenamento e objetos de fluxo para um conjunto de propriedades](storage-vs--stream-for-a-property-set.md) .

</dd> <dt>

<span id="IPropertyStorage__Enum"></span><span id="ipropertystorage__enum"></span><span id="IPROPERTYSTORAGE__ENUM"></span>[**IPropertyStorage:: enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum)
</dt> <dd>

Constrói uma instância de [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg), os métodos que podem ser chamados para enumerar as estruturas [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) que fornecem informações sobre cada uma das propriedades no conjunto. Essa implementação cria uma matriz na qual o conjunto de propriedades inteiro é lido e que pode ser compartilhado quando **IEnumSTATPROPSTG:: clone** é chamado. As alterações no conjunto de propriedades não são refletidas em uma instância **IEnumSTATPROPSTG** aberta. Para ver essas alterações, uma nova instância desse enumerador deve ser construída.

</dd> <dt>

<span id="IPropertyStorage__Stat"></span><span id="ipropertystorage__stat"></span><span id="IPROPERTYSTORAGE__STAT"></span>[**IPropertyStorage:: stat**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-stat)
</dt> <dd>

Preenche os membros de uma estrutura [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) , que contém dados sobre o conjunto de propriedades como um todo. No retorno, fornece um ponteiro para a estrutura. Para conjuntos de armazenamento não simples, essa implementação chama [**IStorage:: stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) (ou [**IStream:: stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)) para obter os tempos do armazenamento ou fluxo subjacente. Para conjuntos de armazenamento simples, nenhuma vez é mantida.

</dd> <dt>

<span id="IPropertyStorage__SetTimes"></span><span id="ipropertystorage__settimes"></span><span id="IPROPERTYSTORAGE__SETTIMES"></span>[**IPropertyStorage:: settimes**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes)
</dt> <dd>

Somente para conjuntos de propriedades não simples, o define os tempos suportados pelo armazenamento subjacente. A implementação do armazenamento de arquivos compostos dá suporte a todos os três: modificação, acesso e criação. Essa implementação de [**Settimes**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes) chama o método [**IStorage:: SetElementTimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes) do armazenamento subjacente para recuperar esses horários.

</dd> </dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[**IStorage:: SetElementTimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes)
</dt> </dl>

 

 