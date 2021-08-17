---
title: IPropertySetStorage-Compound de arquivos
description: A implementação do objeto de armazenamento de arquivos composto COM inclui uma implementação de IPropertyStorage, a interface que gerencia um único conjunto de propriedades persistentes e IPropertySetStorage, a interface que gerencia grupos de conjuntos de propriedades persistentes.
ms.assetid: de2cb778-c6eb-4487-996b-87405674f603
keywords:
- IPropertySetStorage Strctd Stg , implementações, arquivo composto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec3bc0d423b304b6d456ccddab158a48ba0b6d5f3f310d293c6aed0dedb2a556
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119662656"
---
# <a name="ipropertysetstorage-compound-file-implementation"></a>IPropertySetStorage-Compound de arquivos

A implementação do objeto de armazenamento de arquivos composto [COM](ipropertystorage-compound-file-implementation.md) inclui uma implementação de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), a interface que gerencia um único conjunto de propriedades persistentes e [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage), a interface que gerencia grupos de conjuntos de propriedades persistentes.

Para obter um ponteiro para a implementação de arquivo composto de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage), especifique o nome definido pelo header para o identificador IID IStorage como o parâmetro riid ou use as funções \_ [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) ou [**StgOpenStorageEx.**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)  Em ambos os casos, especifique STGFMT \_ STORAGE como o parâmetro *stgfmt.* (STGFMT \_ ANY pode ser especificado como alternativa no caso de **StgOpenStorageEx**.) Além disso, especifique o nome definido pelo header para o IID (identificador de interface) \_ IPropertySetStorage como o *parâmetro riid.* Ambas as funções fornecem um ponteiro para a interface **IPropertySetStorage do** objeto.

Outra maneira de obter um ponteiro para a implementação de arquivo composto é especificar o nome definido pelo header para o identificador IID IStorage como o parâmetro riid ou usar as funções \_ [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) ou [**StgOpenStorage.**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)  Isso fornecerá um ponteiro para a interface [**IStorage do**](/windows/desktop/api/Objidl/nn-objidl-istorage) objeto. Quando você quiser lidar com conjuntos de propriedades persistentes, chame [**IStorage::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para a interface [**IPropertySetStorage.**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)

## <a name="when-to-use-ipropertysetstorage"></a>Quando usar IPropertySetStorage

Chame os métodos de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) para criar, abrir ou excluir conjuntos de propriedades no armazenamento atual do conjunto de propriedades de arquivo composto. Também há um método, [**IPropertySetStorage::Enum,**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum)que fornece um ponteiro para um enumerador que pode ser usado para enumerar os conjuntos de propriedades no armazenamento.

## <a name="methods"></a>Métodos

[**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)

Cria uma nova propriedade definida no armazenamento de arquivos composto atual e, no retorno, fornece um ponteiro de interface para a implementação de arquivo composto [**IPropertyStorage.**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) Nessa implementação, os conjuntos de propriedades poderão ser transacionados somente se PROPSETFLAG \_ NONSIMPLE for especificado. Esse método requer que o modo de compartilhamento especificado no parâmetro *grfMode* seja STGM SHARE EXCLUSIVE e que o modo de acesso seja \_ \_ STGM READ ou \_ STGM READWRITE (não há suporte para o modo \_ STGM \_ WRITE).

[**IPropertySetStorage::Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)

Abre um conjunto de propriedades existente no armazenamento de propriedades atual. No retorno, ele fornece um ponteiro de interface para a implementação de arquivo composto de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage). Esse método requer que o modo de compartilhamento especificado no parâmetro *grfMode* seja STGM SHARE EXCLUSIVE e que o modo de acesso seja \_ \_ STGM READ ou STGM READWRITE (não há suporte para \_ \_ STGM \_ WRITE).

[**IPropertySetStorage::D elete**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-delete)

Exclui um conjunto de propriedades nesse armazenamento de propriedades.

[**IPropertySetStorage::Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum)

Cria um objeto usado para enumerar estruturas [**STATPROPSETSTG.**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) Cada **estrutura STATPROPSETSTG** fornece dados sobre um único conjunto de propriedades.

## <a name="remarks"></a>Comentários

A partir Windows 2000, a implementação de arquivo composto [**de IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) dá suporte ao modo simples. O modo simples é indicado especificando o sinalizador STGM SIMPLE para as funções \_ [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) e [**StgOpenStorageEx.**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) Se o arquivo composto for aberto no modo simples, a implementação **IPropertySetStorage** associada será limitada da seguinte maneira:

-   Somente conjuntos de propriedades simples podem ser criados. Ou seja, especificar o valor DE PROPSETFLAG NONSIMPLE no parâmetro \_ *grfFlags* para o método [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) resulta em um erro.
-   Depois de criar um arquivo composto com [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) usando STGM SIMPLE e consultar a \_ interface [**IPropertySetStorage,**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) você só poderá chamar [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) uma vez. Em seguida, você deve liberar a interface [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) antes de chamar o **método Create** novamente. Para obter mais informações sobre o modo simples, consulte [**Constantes STGM**](stgm-constants.md).
-   Não é possível usar o método [**IPropertySetStorage::Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) para abrir um conjunto de propriedades depois de usar [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) para criar o objeto de armazenamento. Em vez disso, você deve usar [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) antes de consultar [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) e chamar o **método Open.**
-   Depois de abrir um arquivo composto com [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) usando o sinalizador STGM SIMPLE e a consulta para a interface IPropertySetStorage, você pode abrir um conjunto de propriedades por vez usando \_ [**IPropertySetStorage::Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open). [](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) Além disso, talvez não seja possível aumentar o tamanho total do conjunto de propriedades enquanto o conjunto de propriedades estiver aberto.

Conjuntos de propriedades simples não podem ser transacionados. Você não pode especificar STGM TRANSACTED no parâmetro grfmode dos métodos Create e Open, a menos que você também especifique \_ PROPSETFLAG NONSIMPLE no parâmetro  [](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) [](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) \_ *grfFlags.* Esteja ciente de que conjuntos de propriedades simples e não simples não estão relacionados aos conjuntos de propriedades de modo simples descritos acima. Para obter mais informações sobre conjuntos de propriedades simples e não simples, [consulte Armazenamento e Objetos de Fluxo para um Conjunto de Propriedades](storage-vs--stream-for-a-property-set.md).

> [!Note]  
> Os conjuntos de propriedades DocumentSummaryInformation e UserDefined são exclusivos porque podem ter duas seções de conjunto de propriedades. Para obter mais informações, [consulte The DocumentSummaryInformation e UserDefined Property Sets](the-documentsummaryinformation-and-userdefined-property-sets.md).

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[IPropertyStorage – Implementação de arquivo composto](ipropertystorage-compound-file-implementation.md)
</dt> <dt>

[**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)
</dt> <dt>

[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[**IStorage::EnumElements**](/windows/desktop/api/Objidl/nf-objidl-istorage-enumelements)
</dt> <dt>

[**Constantes PROPSETFLAG**](propsetflag-constants.md)
</dt> <dt>

[**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)
</dt> </dl>

 

 