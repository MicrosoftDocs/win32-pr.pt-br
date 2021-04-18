---
title: Considerações de armazenamento de propriedade
description: IPropertyStorage ReadMultiple lê quantas propriedades especificadas na matriz rgpspec como são encontradas no conjunto de propriedades.
ms.assetid: 7540966f-a3b2-46c9-9e04-b15133a517eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aad6aabf8b22a7c01f91a090136e6cc8156c791
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105749440"
---
# <a name="property-storage-considerations"></a>Considerações de armazenamento de propriedade

[**IPropertyStorage:: ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) lê quantas propriedades especificadas na matriz *rgpspec* como são encontradas no conjunto de propriedades. Desde que qualquer uma das propriedades solicitadas seja lida, uma solicitação para recuperar uma propriedade que não existe não é um erro. Em vez disso, isso deve fazer com \_ que o VT vazio seja gravado para  essa propriedade \[ \] na matriz rgVar no retorno. Quando nenhuma das propriedades solicitadas existir, o método deverá retornar S \_ false e definir o VT \_ vazio em cada [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant). Se qualquer outro erro for retornado, nenhum valor de propriedade será recuperado e o chamador não precisará se preocupar em liberá-los.

O parâmetro *rgpspec* é uma matriz de estruturas [**PROPSPEC**](/windows/win32/api/propidlbase/ns-propidlbase-propspec) , que especificam para cada propriedade seu identificador de propriedade ou, se uma for atribuída, um identificador de cadeia de caracteres. Você pode mapear uma cadeia de caracteres para um identificador de propriedade chamando [**IPropertyStorage:: WritePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writepropertynames). O uso de identificadores de propriedade, no entanto, provavelmente será significativamente mais eficiente do que o uso de cadeias de caracteres.

As propriedades que são solicitadas pelo nome da cadeia de caracteres (PRSPEC \_ LPWSTR) são mapeadas sem diferenciação de maiúsculas e minúsculas para identificadores de propriedade (IDs), pois elas são especificadas no conjunto de propriedades atual (e de acordo com a localidade do sistema atual).

Quando o tipo de propriedade é VT \_ LPSTR e a propriedade é lida de um conjunto de propriedades ANSI, ou seja, a página de código para o conjunto de propriedades é definida como algo diferente de Unicode, o valor da propriedade usa a mesma página de código que o conjunto de propriedades. Quando uma propriedade ' VT \_ LPSTR ' é lida de um conjunto de propriedades Unicode, o valor da propriedade usa a página de código ANSI padrão atual do sistema, ou seja, a página de código retornada da função **GetACP** .

Um [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant), exceto aqueles que são ponteiros para fluxos e armazenamentos, é chamado de **PROPVARIANT** simples. Esses **PROPVARIANT** simples recebem dados por valor, portanto, uma chamada para [**IPropertyStorage:: ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) fornece uma cópia dos dados que o chamador possui. Para criar ou atualizar essas propriedades, chame [**IPropertyStorage:: WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple).

Por outro lado, os tipos de variantes VT \_ Stream, VT \_ Streamed \_ Object, VT \_ Storage e VT \_ armazenado \_ são propriedades não simples, porque em vez de fornecer um valor, o método recupera um ponteiro para a interface indicada, da qual os dados podem ser lidos. Esses tipos permitem o armazenamento de grandes quantidades de informações por meio de uma única propriedade. Há vários problemas que surgem no uso de propriedades não simples.

Para criar essas propriedades, como para as outras propriedades, chame [**IPropertyStorage:: WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple). Em vez de chamar o mesmo método para atualizar, no entanto, é mais eficiente primeiro chamar [**IPropertyStorage:: ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) para obter o ponteiro de interface para o fluxo ou armazenamento e, em seguida, gravar dados usando os métodos [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) ou [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) . Um fluxo ou armazenamento aberto por meio de uma propriedade é sempre aberto no modo direto, portanto, um nível adicional de transação aninhada não é introduzido. No entanto, pode ainda haver uma transação no conjunto de propriedades como um todo, dependendo de como ela foi aberta ou criada por meio de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage). Além disso, as marcas de acesso e modo de compartilhamento especificadas quando o conjunto de propriedades é aberto ou criado são passadas para fluxos baseados em propriedade ou armazenamentos.

Os tempos de vida do fluxo baseado em propriedade ou ponteiros de armazenamento, embora teoricamente independente dos seus ponteiros [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) e [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) associados, na verdade, dependem efetivamente deles. Os dados visíveis por meio do fluxo ou do armazenamento estão relacionados à transação no objeto de armazenamento de Propriedade do qual ele é recuperado, assim como para um objeto de armazenamento (com suporte a [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)) com o fluxo e subobjetos de armazenamento contidos. Se a transação no objeto pai for anulada, os ponteiros [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) e **IStorage** existentes subordinados a esse objeto não estarão mais acessíveis. Como **IPropertyStorage** é a única interface no objeto de armazenamento de propriedade, o tempo de vida útil dos ponteiros **IStream** e **IStorage** contidos é limitado pelo tempo de vida da interface **IPropertyStorage** .

A implementação também deve lidar com a situação em que a mesma propriedade com valor de fluxo ou de armazenamento é solicitada várias vezes por meio da mesma instância de interface [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) . Por exemplo, na implementação do arquivo composto COM, a abertura terá êxito ou falhará dependendo se a propriedade já estiver aberta ou não.

Outro problema é várias aberturas no modo transacionado. O resultado depende do nível de isolamento que foi especificado por meio de uma chamada para métodos [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) (o método [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) ou [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) , por meio dos sinalizadores STGM) no momento em que o armazenamento de propriedade foi aberto.

Se a chamada para abrir o conjunto de propriedades especificar o acesso de leitura/gravação, as propriedades com valor de [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) e [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)sempre serão abertas com acesso de leitura/gravação. Os dados podem então ser escritos por meio dessas interfaces, alterando o valor da propriedade, que é a maneira mais eficiente de atualizar essas propriedades. O próprio valor da propriedade não tem um nível adicional de aninhamento de transações, portanto, as alterações têm o escopo definido na transação (se houver) no objeto de armazenamento de propriedade.

## <a name="storage-and-stream-properties"></a>Propriedades de armazenamento e fluxo

Para gravar um fluxo ou um objeto de armazenamento em um conjunto de propriedades, o conjunto de propriedades deve ter sido criado como não simples. Para obter mais informações sobre conjuntos de propriedades simples e não simples, consulte a seção intitulada [armazenamento e objetos de fluxo para um conjunto de propriedades](storage-vs--stream-for-a-property-set.md). Os tipos de propriedade a seguir, conforme especificado no campo *VT* dos elementos da matriz *rgVar* , são tipos de armazenamento ou de fluxo: VT \_ Stream, \_ armazenamento VT, \_ objeto transmitido por VT \_ , \_ objeto armazenado VT \_ .

Para gravar um fluxo ou um objeto de armazenamento como uma propriedade em um conjunto de propriedades não simples, chame [**IPropertyStorage:: WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple). Embora você também chame esse método para atualizar propriedades simples, ele não é uma maneira eficiente de atualizar o fluxo e os objetos de armazenamento em um conjunto de propriedades. Isso ocorre porque a atualização de uma dessas propriedades por meio de uma chamada para **WriteMultiple** cria no objeto de armazenamento de propriedade uma cópia dos dados passados e os ponteiros [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) ou [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) não são mantidos além da duração dessa chamada. Geralmente, é mais eficiente atualizar os objetos Stream ou Storage diretamente chamando [**IPropertyStorage:: ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) para obter o ponteiro de interface para o fluxo ou armazenamento e, em seguida, gravar dados por meio dos métodos **IStream** ou **IStorage** .

Por exemplo, você pode chamar [**IPropertyStorage:: WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) para gravar um fluxo **nulo** ou objeto de armazenamento. Em seguida, a implementação criará um objeto vazio no conjunto de propriedades. Você pode obter acesso a esse objeto chamando [**IPropertyStorage:: ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple). Quando você terminar de atualizar esse objeto, não precisará gravá-lo no conjunto de propriedades, pois as atualizações entrarão diretamente no conjunto de propriedades.

Um fluxo ou armazenamento aberto por meio de uma propriedade é sempre aberto no modo direto, portanto, um nível adicional de transação aninhada não é introduzido. Ainda pode haver uma transação no conjunto de propriedades como um todo. (Por exemplo, se o [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) foi obtido chamando [**IPropertySetStorage:: Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) com o STGM \_ Sinalizador transacionado definido no parâmetro *grfMode* .) Além disso, um armazenamento ou fluxo baseado em propriedade é aberto no modo de leitura/gravação, se possível, dado o modo no conjunto de propriedades; caso contrário, o modo de leitura será usado.

Como mencionado anteriormente, quando um fluxo ou objeto de armazenamento é gravado em um conjunto de propriedades com o método [**WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) , uma cópia do objeto é feita. Quando tal cópia é feita em um objeto de fluxo, a operação de cópia começa na posição de busca atual da origem. A posição de busca é indefinida em caso de falha, mas em caso de sucesso ela está no final do fluxo; o ponteiro de busca não é restaurado para sua posição original.

Se uma propriedade de fluxo ou de armazenamento tiver sido lida de um conjunto de propriedades com [**ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple), ainda estiver aberta e uma chamada subsequente para [**WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) para a mesma propriedade for feita, a operação **WriteMultiple** terá sucesso. O fluxo ou a propriedade de armazenamento aberta anteriormente é colocada no estado revertido (todas as chamadas para ela retornarão STG \_ E \_ erro revertido).

Se o método [**WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) retornar um erro ao gravar uma matriz de propriedades ou até mesmo propriedades individuais não simples, a quantidade de dados realmente gravados será indefinida.

## <a name="reference-properties"></a>Propriedades de referência

Se uma estrutura [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) especificada incluir o \_ sinalizador VT ByRef em seu membro **VT** , a propriedade associada será uma propriedade de referência. Uma propriedade de referência é desreferenciada automaticamente antes de gravar o valor no conjunto de propriedades. Por exemplo, se o membro **VT** da estrutura **PROPVARIANT** especifica um valor do tipo VT \_ ByRef \| VT \_ i4, o valor real gravado é um tipo VT \_ i4. Uma chamada subsequente para o método [**IPropertyStorage:: ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) retorna um valor como VT \_ i4. O uso de propriedades de referência é semelhante à chamada da função [VariantCopyInd](/windows/win32/api/oleauto/nf-oleauto-variantcopyind) . O [VariantCopyInd](/windows/win32/api/oleauto/nf-oleauto-variantcopyind) libera a variante de destino e faz uma cópia do VARIANTARG de origem, executando o indireção necessário se a origem for especificada como VT \_ ByRef. Essa função é útil quando uma cópia de uma variante é necessária e para garantir que ela não seja um VT \_ ByRef, por exemplo, ao manipular argumentos em uma implementação de [**IDispatch:: Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke).

## <a name="notes-to-callers"></a>Notas aos Chamadores

É recomendável que os conjuntos de propriedades sejam criados como Unicode, não definindo o \_ sinalizador ANSI PROPSETFLAG no parâmetro *GrfFlags* de [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create). Também é recomendável que você evite usar \_ valores de ' VT LPSTR ' e use valores do VT \_ LPWSTR em vez disso. Quando a página de código do conjunto de propriedades é Unicode, \_ os valores da cadeia de caracteres VT LPSTR são convertidos em Unicode quando armazenados e de volta para valores de cadeia de caracteres multibyte quando recuperados. Quando a página de código do conjunto de propriedades não for Unicode, os nomes de propriedade, \_ cadeias de caracteres VT BSTR e valores de propriedade não simples serão convertidos em cadeias de caracteres multibyte quando armazenados e convertidos de volta para Unicode quando recuperados, todos usando a página de código ANSI do sistema atual.

## <a name="notes-to-implementers"></a>Notas aos Implementadores

Ao alocar um identificador de propriedade, a implementação pode escolher qualquer valor que não esteja atualmente em uso no conjunto de propriedades para um identificador de propriedade, desde que não seja 0 ou 1 ou maior que 0x80000000, todos os quais são valores reservados. O parâmetro *propidNameFirst* estabelece um valor mínimo para identificadores de propriedade dentro do conjunto e deve ser maior que 1 e menor que 0x80000000. Consulte a seção de comentários acima.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[IPropertyStorage-implementação de arquivo composto](ipropertystorage-compound-file-implementation.md)
</dt> <dt>

[IPropertyStorage-implementação do sistema de arquivos NTFS](ipropertystorage-ntfs-file-system-implementation.md)
</dt> <dt>

[Implementação IPropertyStorage-autônoma](ipropertystorage-stand-alone-implementation.md)
</dt> </dl>

 

 