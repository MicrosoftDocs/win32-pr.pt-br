---
title: IPropertySetStorage-implementação do sistema de arquivos NTFS
description: A versão 5,0 do NTFS fornece uma implementação de IPropertySetStorage para arquivos em um volume NTFS quando os próprios arquivos não são arquivos compostos.
ms.assetid: cd7290bb-bb4e-4dea-9bf6-2e1fdd0ebae8
keywords:
- IPropertySetStorage Strctd STG, implementações, sistema de arquivos NTFS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b0d647b9cb804376a9efeb687b1524585ee938d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105753082"
---
# <a name="ipropertysetstorage-ntfs-file-system-implementation"></a>IPropertySetStorage-implementação do sistema de arquivos NTFS

A versão 5,0 do NTFS fornece uma implementação de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) para arquivos em um volume NTFS quando os próprios arquivos não são arquivos compostos. A implementação do NTFS é equivalente à [implementação do arquivo composto](ipropertysetstorage-compound-file-implementation.md). Para obter mais informações sobre exceções, consulte comentários.

**Para obter um ponteiro para a implementação NTFS de IPropertySetStorage**

1.  Chame [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) e especifique **o \_ arquivo STGFMT** no parâmetro *grfFlags* para criar um novo arquivo.
2.  Chame [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) e especifique o **\_ arquivo STGFMT** ou **STGFMT \_ qualquer** valor de enumeração no parâmetro *grfFlags* para abrir um arquivo existente.

No entanto, você não pode obter a implementação NTFS de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) para um arquivo composto. Ao abrir um arquivo composto com [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage), especificar o valor de enumeração do **\_ arquivo STGFMT** resultará em um erro.

Além disso, os conjuntos de propriedades simples não podem ser transacionados. Ou seja, você não pode **especificar STGM \_ transacionado** no parâmetro *grfMode* dos métodos [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) e [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) , a menos que você também especifique **PROPSETFLAG não \_ simples** no parâmetro *grfFlags* . O objeto de armazenamento do conjunto de propriedades em si não dá suporte ao processamento de transações.

## <a name="when-to-use"></a>Quando usar

Chame os métodos [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) para criar, abrir ou excluir conjuntos de propriedades no armazenamento atual definido do conjunto de propriedades NTFS. Há também um método, [**IPropertySetStorage:: enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum), que fornece um ponteiro para um enumerador que pode ser usado para enumerar os conjuntos de propriedades no armazenamento.

## <a name="compatibility"></a>Compatibilidade

As implementações de NTFS do [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) e do [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) estão disponíveis a partir do Windows 2000. As versões anteriores não podem acessar esses conjuntos de propriedades.

A implementação do NTFS armazena conjuntos de propriedades em fluxos alternativos de um arquivo NTFS. Os fluxos alternativos devem ser copiados quando o arquivo principal é copiado.

> [!Caution]  
> Nem todos os sistemas de arquivos dão suporte a esses fluxos. Se um arquivo NTFS com conjuntos de Propriedades for copiado para um volume FAT, somente os dados no arquivo serão copiados; o conjunto de propriedades é perdido. A função [**CopyFile**](/windows/desktop/api/winbase/nf-winbase-copyfile) não retorna um erro nesse caso.

 

> [!Caution]  
> Se o computador que executa a cópia do arquivo não for um computador executando no Windows 2000 ou posterior, os conjuntos de propriedades poderão ser perdidos. Por exemplo, se um computador executando no sistema operacional Windows 95 copiar um arquivo NTFS, o conjunto de propriedades será perdido mesmo que o arquivo de destino também esteja em um volume NTFS.

 

## <a name="methods"></a>Métodos

A implementação do sistema de arquivos NTFS do [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) dá suporte aos métodos a seguir.

<dl> <dt>

<span id="IPropertySetStorage__Create"></span><span id="ipropertysetstorage__create"></span><span id="IPROPERTYSETSTORAGE__CREATE"></span>[**IPropertySetStorage:: criar**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)
</dt> <dd>

Cria um novo conjunto de propriedades no armazenamento de arquivos NTFS atual e, no retorno, fornece um ponteiro de interface para a implementação do arquivo NTFS [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) . O modo de compartilhamento especificado no parâmetro *grfMode* deve ser **\_ \_ exclusivo para compartilhamento de STGM**.

</dd> <dt>

<span id="IPropertySetStorage__Open"></span><span id="ipropertysetstorage__open"></span><span id="IPROPERTYSETSTORAGE__OPEN"></span>[**IPropertySetStorage:: abrir**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)
</dt> <dd>

Abre um conjunto de propriedades existente no armazenamento de propriedade atual. No retorno, ele fornece um ponteiro de interface para a implementação do arquivo NTFS de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage). O modo de compartilhamento especificado no parâmetro *grfMode* deve ser **\_ \_ exclusivo para compartilhamento de STGM**.

</dd> <dt>

<span id="IPropertySetStorage__Delete"></span><span id="ipropertysetstorage__delete"></span><span id="IPROPERTYSETSTORAGE__DELETE"></span>[**IPropertySetStorage::D excluir**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-delete)
</dt> <dd>

Exclui um conjunto de propriedades no armazenamento de propriedade atual.

</dd> <dt>

<span id="IPropertySetStorage__Enum"></span><span id="ipropertysetstorage__enum"></span><span id="IPROPERTYSETSTORAGE__ENUM"></span>[**IPropertySetStorage:: enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum)
</dt> <dd>

Cria um objeto usado para enumerar estruturas [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) . Cada estrutura **STATPROPSETSTG** fornece dados sobre um único conjunto de propriedades.

</dd> </dl>

## <a name="remarks"></a>Comentários

As implementações NTFS de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) e [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) armazenam conjuntos de propriedades em um arquivo sem afetar o conteúdo desse arquivo. Por exemplo, se você criar um conjunto de propriedades em um arquivo HTML chamado Default.htm, esse arquivo ainda será exibido corretamente em um navegador da Web. Ou seja, as alterações em um arquivo usando essas duas interfaces não são detectáveis ao acessar um arquivo com a função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .

A implementação NTFS do [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) fornece uma implementação segura quando usada para gravar conjuntos de propriedades em um arquivo em um volume NTFS versão 5,0. Esses conjuntos de propriedades não podem ser corrompidos pela implementação mesmo no caso de uma falha do sistema. Por exemplo, se a potência de um sistema falhar durante uma chamada para [**IPropertyStorage:: Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) enquanto o conjunto de Propriedades for liberado para o disco, o conjunto de propriedades nunca será deixado em um estado intermediário. A versão anterior do conjunto de propriedades permanece ou todas as atualizações são salvas.

A implementação NTFS do [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) difere da implementação do arquivo composto das seguintes maneiras:

-   Uma estrutura [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) obtida da interface [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) contém um membro **CLSID** cujo valor é sempre zero (**CLSID \_ NULL**). Com a implementação do arquivo composto, o membro **CLSID** correto é retornado para conjuntos de propriedades não simples (consulte [armazenamento e fluxo de objetos para um conjunto de propriedades](storage-vs--stream-for-a-property-set.md)).
-   Ao obter uma implementação NTFS do ponteiro de interface [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) usando a função [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) ou [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) , o parâmetro *grfMode* deve seguir as mesmas regras que para a implementação do arquivo composto.

    Além disso, os seguintes sinalizadores não podem ser usados:

    **STGM \_ SIMPLES**, **STGM \_ transacionada**, **STGM \_ Convert**, **\_ prioridade de STGM** e **STGM \_ DELETEONRELEASE**.

-   Quando uma interface [**IPROPERTYSETSTORAGE**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) NTFS é obtida pelas funções [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) ou [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) , os modos de compartilhamento se aplicam principalmente a outras instâncias dessa interface e não a instâncias de abertura do próprio arquivo. Por exemplo, se uma interface **IPropertySetStorage** do NTFS for aberta chamando a função **StgOpenStorageEx** , com o parâmetro *grfMode* definido como **STGM \_ ReadWrite \| STGM \_ compartilhado \_ exclusivo**, será possível abrir o arquivo com a função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .

    Essas instâncias simultâneas de abrir esta interface estão sujeitas às seguintes restrições: o parâmetro *dwShareMode* na função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) deve especificar o sinalizador de **\_ \_ leitura de compartilhamento de arquivos** e o parâmetro *dwAccess* não deve especificar o sinalizador de **exclusão** . Além disso, as funções [**DeleteFile**](/windows/desktop/api/fileapi/nf-fileapi-deletefilea) e [**MoveFile**](/windows/desktop/api/winbase/nf-winbase-movefile) não devem ser chamadas em um arquivo para o qual essas interfaces de conjunto de propriedades estão abertas, pois essas funções exigem acesso de **exclusão** ao arquivo.

-   Se um método [**IPROPERTYSETSTORAGE**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) NTFS for aberto como somente leitura e o arquivo não tiver conjuntos de propriedades no momento, o objeto retornado não manterá a abertura do arquivo. Consequentemente, outras aberturas desse arquivo terão sucesso, mesmo se o modo de compartilhamento da operação aberta original, caso contrário, o rejeitaria.

    Exemplo se um [**IPROPERTYSETSTORAGE**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) NTFS for aberto no modo **STGM \_ ler \| STGM \_ compartilhamento \_ exclusivo** e o arquivo não tiver conjuntos de propriedades, será possível abrir simultaneamente o arquivo **STGM \_ ReadWrite \| STGM \_ compartilhamento \_ exclusivo**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[IPropertyStorage-implementação do sistema de arquivos NTFS](ipropertystorage-ntfs-file-system-implementation.md)
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

 

 