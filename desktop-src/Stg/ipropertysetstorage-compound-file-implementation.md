---
title: Implementação de arquivo de IPropertySetStorage-Compound
description: A implementação do objeto de armazenamento de arquivo composto COM inclui uma implementação de ambos os IPropertyStorage, a interface que gerencia um único conjunto de propriedades persistentes e IPropertySetStorage, a interface que gerencia grupos de conjuntos de propriedades persistentes.
ms.assetid: de2cb778-c6eb-4487-996b-87405674f603
keywords:
- IPropertySetStorage Strctd STG, implementações, arquivo composto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9053a7cf6bf1ae7e4230b15eb0117c428acb08da
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641545"
---
# <a name="ipropertysetstorage-compound-file-implementation"></a>Implementação de arquivo de IPropertySetStorage-Compound

A [implementação do objeto de armazenamento de arquivo composto com](ipropertystorage-compound-file-implementation.md) inclui uma implementação de ambos os [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), a interface que gerencia um único conjunto de propriedades persistentes e [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage), a interface que gerencia grupos de conjuntos de propriedades persistentes.

Para obter um ponteiro para a implementação do arquivo composto de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage), especifique o nome definido pelo cabeçalho para o ISTORAGE de IID do identificador \_ como o parâmetro *riid* ou use as funções [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) ou [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) . Em ambos os casos, especifique \_ o armazenamento STGFMT como o parâmetro *STGFMT* . (STGFMT \_ Qualquer um pode ser especificado como alternativa no caso de **StgOpenStorageEx**.) Além disso, especifique o nome definido pelo cabeçalho para o IPropertySetStorage de IID do identificador de interface (IID) \_ como o parâmetro *riid* . Ambas as funções fornecem um ponteiro para a interface Object **IPropertySetStorage** .

Outra maneira de obter um ponteiro para a implementação do arquivo composto é especificar o nome definido pelo cabeçalho para o IStorage de IID do identificador \_ como o parâmetro *riid* ou usar as funções [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) ou [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) . Isso fornecerá um ponteiro para a interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) do objeto. Quando você quiser lidar com conjuntos de propriedades persistentes, chame [**IStorage:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para a interface [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) .

## <a name="when-to-use-ipropertysetstorage"></a>Quando usar o IPropertySetStorage

Chame os métodos de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) para criar, abrir ou excluir conjuntos de propriedades no armazenamento do conjunto de propriedades de arquivo composto atual. Há também um método, [**IPropertySetStorage:: enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum), que fornece um ponteiro para um enumerador que pode ser usado para enumerar os conjuntos de propriedades no armazenamento.

## <a name="methods"></a>Métodos

[**IPropertySetStorage:: criar**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)

Cria um novo conjunto de propriedades no armazenamento de arquivo composto atual e, no retorno, fornece um ponteiro de interface para a implementação de arquivo composto [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) . Nessa implementação, os conjuntos de propriedades poderão ser transacionados somente se PROPSETFLAG não \_ for especificado. Esse método requer que o modo de compartilhamento especificado no parâmetro *grfMode* seja STGM \_ compartilhamento \_ exclusivo e que o modo de acesso seja STGM \_ Read ou STGM \_ ReadWrite (o modo de gravação STGM \_ não tem suporte).

[**IPropertySetStorage:: abrir**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)

Abre um conjunto de propriedades existente no armazenamento de propriedade atual. No retorno, ele fornece um ponteiro de interface para a implementação do arquivo composto de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage). Esse método requer que o modo de compartilhamento especificado no parâmetro *grfMode* seja STGM \_ \_ de compartilhamento exclusivo e que o modo de acesso seja STGM \_ Read ou STGM \_ ReadWrite ( \_ não há suporte para a gravação de STGM).

[**IPropertySetStorage::D excluir**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-delete)

Exclui um conjunto de propriedades neste armazenamento de propriedades.

[**IPropertySetStorage:: enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum)

Cria um objeto usado para enumerar estruturas [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) . Cada estrutura **STATPROPSETSTG** fornece dados sobre um único conjunto de propriedades.

## <a name="remarks"></a>Comentários

A partir do Windows 2000, a implementação de arquivo composto do [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) dá suporte ao modo simples. O modo simples é indicado especificando o \_ sinalizador simples STGM para as funções [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) e [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) . Se o arquivo composto for aberto no modo simples, a implementação **IPropertySetStorage** associada será limitada da seguinte maneira:

-   Somente os conjuntos de propriedades simples podem ser criados. Ou seja, especificar o valor não simples de PROPSETFLAG \_ no parâmetro *grfFlags* para o método [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) resulta em um erro.
-   Depois de criar um arquivo composto com [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) usando \_ o STGM simples e consultar a interface [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) , você só poderá chamar [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) uma vez. Em seguida, você deve liberar a interface [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) antes de chamar o método **Create** novamente. Para obter mais informações sobre o modo simples, consulte [**constantes STGM**](stgm-constants.md).
-   Você não pode usar o método [**IPropertySetStorage:: Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) para abrir um conjunto de propriedades depois de usar [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) para criar o objeto de armazenamento. Em vez disso, você deve usar [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) antes de consultar [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) e chamar o método **Open** .
-   Depois de abrir um arquivo composto com [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) usando o \_ sinalizador simples do STGM e a consulta para a interface [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) , você pode abrir um conjunto de propriedades por vez usando [**IPropertySetStorage:: Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open). Além disso, talvez não seja possível que o tamanho total do conjunto de propriedades seja aumentado enquanto o conjunto de propriedades estiver aberto.

Os conjuntos de propriedades simples não podem ser transacionados. Não é possível especificar STGM \_ transacionado no parâmetro *grfMode* dos métodos [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) e [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) , a menos que você também especifique PROPSETFLAG não \_ simples no parâmetro *grfFlags* . Lembre-se de que os conjuntos de propriedades simples e não simples não estão relacionados aos conjuntos de propriedades de modo simples descritos acima. Para obter mais informações sobre conjuntos de propriedades simples e não simples, consulte [armazenamento e objetos de fluxo para um conjunto de propriedades](storage-vs--stream-for-a-property-set.md).

> [!Note]  
> Os conjuntos de propriedades DocumentSummaryInformation e UserDefined são exclusivos, pois podem ter duas seções de conjunto de propriedades. Para obter mais informações, consulte [os conjuntos de propriedades DocumentSummaryInformation e UserDefined](the-documentsummaryinformation-and-userdefined-property-sets.md).

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[IPropertyStorage-implementação de arquivo composto](ipropertystorage-compound-file-implementation.md)
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
</dt> </dl>

 

 