---
title: IStorage-Compound de arquivos
description: A implementação de arquivo composto do IStorage permite que você crie e gerencie substorages e fluxos em um objeto de armazenamento que reside em um objeto de arquivo composto.
ms.assetid: 2a2253f6-d3d3-403e-a9ba-53a541c7a31e
keywords:
- IStorage Strctd Stg, implementação de arquivo composto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab243189d5a8cfb3e053c66bcd752d05bb65ab965657778a3bc3250c30ef8e75
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992406"
---
# <a name="istorage-compound-file-implementation"></a>IStorage-Compound de arquivos

A implementação de arquivo composto [**do IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) permite que você crie e gerencie substorages e fluxos em um objeto de armazenamento que reside em um objeto de arquivo composto. Para criar um objeto de arquivo composto e obter um ponteiro **IStorage,** chame a função de API [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex). Para abrir um objeto de arquivo composto existente e obter seu ponteiro **IStorage** raiz, chame [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex).

Os aplicativos que usam armazenamento composto devem ser registrados em HKEY \_ CLASSES \_ ROOT \\ SystemFileAssociations e devem fornecer seus próprios manipuladores de propriedade. Para obter mais informações, consulte a seção "Registrando verbos e outras informações de associação de arquivo" de [Registro de aplicativo.](/windows/desktop/shell/app-registration)

## <a name="when-to-use"></a>Quando usar

A maioria dos aplicativos usa essa implementação para criar e gerenciar armazenamentos e fluxos.

## <a name="methods"></a>Métodos

<dl> <dt>

<span id="IStorage__CreateStream"></span><span id="istorage__createstream"></span><span id="ISTORAGE__CREATESTREAM"></span>[**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream)
</dt> <dd>

Cria e abre um objeto de fluxo com o nome especificado contido neste objeto de armazenamento. O nome não deve exceder 31 caracteres de comprimento (não incluindo o terminador de cadeia de caracteres). Os caracteres 000 a 01f, que servem como o primeiro caractere do nome de fluxo/armazenamento, são reservados para uso pelo OLE. Essa é uma restrição de arquivo composta, não uma restrição de armazenamento estruturado. A implementação de arquivo composto fornecida pelo COM do [**método IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) não dá suporte aos seguintes comportamentos:

-   Não há suporte para o sinalizador \_ STGM DELETEONRELEASE.
-   Não há suporte para o modo transacionado (STGM \_ TRANSACTED) para objetos de fluxo.
-   Não há suporte para abrir o mesmo fluxo mais de uma vez do mesmo armazenamento. O sinalizador de modo de compartilhamento EXCLUSIVO DO COMPARTILHAMENTO STGM \_ deve ser especificado no parâmetro \_ *grfMode.*

</dd> <dt>

<span id="IStorage__OpenStream"></span><span id="istorage__openstream"></span><span id="ISTORAGE__OPENSTREAM"></span>[**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream)
</dt> <dd>

Abre um objeto de fluxo existente dentro desse objeto de armazenamento usando os modos de acesso especificados no *parâmetro grfMode.* Os caracteres 000 a 01f, que servem como o primeiro caractere do nome de fluxo/armazenamento, são reservados para uso pelo OLE. Essa é uma restrição de arquivo composta, não uma restrição de armazenamento estruturado. A implementação de arquivo composto fornecida pelo COM do [**método IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) não dá suporte ao seguinte comportamento:

-   O sinalizador STGM \_ DELETEONRELEASE.
-   Modo transacionado (STGM \_ TRANSACTED) para objetos de fluxo.
-   Abrir o mesmo fluxo mais de uma vez do mesmo armazenamento. O sinalizador STGM \_ SHARE EXCLUSIVE deve ser \_ especificado.

</dd> <dt>

<span id="IStorage__CreateStorage"></span><span id="istorage__createstorage"></span><span id="ISTORAGE__CREATESTORAGE"></span>[**IStorage::CreateStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage)
</dt> <dd>

Cria e abre um novo objeto de armazenamento com o nome especificado no modo de acesso especificado. O nome não deve exceder 31 caracteres de comprimento (não incluindo o terminador de cadeia de caracteres). Os caracteres 000 a 01f, que servem como o primeiro caractere do nome de fluxo/armazenamento, são reservados para uso pelo OLE. Essa é uma restrição de arquivo composta, não uma restrição de armazenamento estruturado. A implementação de arquivo composto fornecida pelo COM do [**método IStorage::CreateStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage) não dá suporte ao seguinte comportamento:

-   O sinalizador STGM \_ PRIORITY para armazenamentos não ot.
-   Abrir o mesmo objeto de armazenamento mais de uma vez do mesmo armazenamento pai. O sinalizador STGM \_ SHARE EXCLUSIVE deve ser \_ especificado.
-   O sinalizador STGM \_ DELETEONRELEASE. Se esse sinalizador for especificado, a função retornará STG \_ E \_ INVALIDFLAG.

</dd> <dt>

<span id="IStorage__OpenStorage"></span><span id="istorage__openstorage"></span><span id="ISTORAGE__OPENSTORAGE"></span>[**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage)
</dt> <dd>

Abre um objeto de armazenamento existente com o nome especificado no modo de acesso especificado. Os caracteres 000 a 01f, que servem como o primeiro caractere do nome de fluxo/armazenamento, são reservados para uso pelo OLE. Essa é uma restrição de arquivo composta, não uma restrição de armazenamento estruturado. A implementação de arquivo composto fornecida pelo COM do [**método IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) não dá suporte ao seguinte comportamento:

-   O sinalizador STGM \_ PRIORITY para armazenamentos não ot.
-   Abrir o mesmo objeto de armazenamento mais de uma vez do mesmo armazenamento pai. O sinalizador STGM \_ SHARE EXCLUSIVE deve ser \_ especificado.
-   O sinalizador STGM \_ DELETEONRELEASE. Se esse sinalizador for especificado, a função retornará STG \_ E \_ INVALIDFUNCTION.

</dd> <dt>

<span id="IStorage__CopyTo"></span><span id="istorage__copyto"></span><span id="ISTORAGE__COPYTO"></span>[**IStorage::CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto)
</dt> <dd>

Copia apenas os substorages e fluxos desse objeto de armazenamento aberto em outro objeto de armazenamento. O *parâmetro rgiidExclude* pode ser definido como IID IStream para copiar apenas \_ substorages ou para \_ IID IStorage para copiar apenas fluxos.

</dd> <dt>

<span id="IStorage__MoveElementTo"></span><span id="istorage__moveelementto"></span><span id="ISTORAGE__MOVEELEMENTTO"></span>[**IStorage::MoveElementTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-moveelementto)
</dt> <dd>

Copia ou move um substorage ou fluxo desse objeto de armazenamento para outro objeto de armazenamento.

</dd> <dt>

<span id="IStorage__Commit"></span><span id="istorage__commit"></span><span id="ISTORAGE__COMMIT"></span>[**IStorage::Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit)
</dt> <dd>

Garante que todas as alterações feitas em um objeto de armazenamento abertas no modo transacionado sejam refletidas no armazenamento pai; para um armazenamento raiz, reflete as alterações no dispositivo real; por exemplo, um arquivo em disco. Para um objeto de armazenamento raiz aberto no modo direto, esse método não tem nenhum efeito, exceto para liberar todos os buffers de memória para o disco. Para objetos de armazenamento não armazenados no modo direto, esse método não tem nenhum efeito.

A implementação de arquivos compostos fornecidos pelo COM usa um processo de confirmação de duas fases, a menos que STGC OVERWRITE seja especificado no \_ *parâmetro grfCommitFlags.* Esse processo de duas fases garante a robustez dos dados, caso a operação de confirmação falhe. Primeiro, todos os novos dados são gravados em espaço nãoutilado no arquivo subjacente. Se necessário, o novo espaço será alocado para o arquivo. Depois que essa etapa for concluída, uma tabela no arquivo será atualizada usando uma operação de gravação de setor único para indicar que os novos dados devem ser usados no lugar do antigo. Os dados antigos se tornam espaço livre a ser usado na próxima operação de confirmação. Portanto, os dados antigos estarão disponíveis e poderão ser restaurados se ocorrer um erro ao fazer alterações. Se STGC \_ OVERWRITE for especificado, uma única operação de commit de fase será usada. Para obter mais informações sobre sinalizadores de modo transacionado, consulte [**enumeração STGC.**](/windows/win32/api/wtypes/ne-wtypes-stgc)

</dd> <dt>

<span id="IStorage__Revert"></span><span id="istorage__revert"></span><span id="ISTORAGE__REVERT"></span>[**IStorage::Revert**](/windows/desktop/api/Objidl/nf-objidl-istorage-revert)
</dt> <dd>

Descarta todas as alterações feitas no objeto de armazenamento desde a última operação de confirmação.

</dd> <dt>

<span id="IStorage__EnumElements"></span><span id="istorage__enumelements"></span><span id="ISTORAGE__ENUMELEMENTS"></span>[**IStorage::EnumElements**](/windows/desktop/api/Objidl/nf-objidl-istorage-enumelements)
</dt> <dd>

Cria e recupera um ponteiro para um objeto enumerador que pode ser usado para enumerar os objetos de armazenamento e fluxo contidos nesse objeto de armazenamento. A implementação de arquivo composto fornecida pelo COM tira um instantâneo dessas informações. Portanto, as alterações nos fluxos e armazenamentos não são refletidas no enumerador até que um novo enumerador seja obtido.

</dd> <dt>

<span id="IStorage__DestroyElement"></span><span id="istorage__destroyelement"></span><span id="ISTORAGE__DESTROYELEMENT"></span>[**IStorage::D mentoelement**](/windows/desktop/api/Objidl/nf-objidl-istorage-destroyelement)
</dt> <dd>

Remove o elemento especificado (substorage ou fluxo) desse objeto de armazenamento.

</dd> <dt>

<span id="IStorage__RenameElement"></span><span id="istorage__renameelement"></span><span id="ISTORAGE__RENAMEELEMENT"></span>[**IStorage::RenameElement**](/windows/desktop/api/Objidl/nf-objidl-istorage-renameelement)
</dt> <dd>

Renomeia o substorage ou o fluxo especificado neste objeto de armazenamento. Os caracteres 000 a 01f, que servem como o primeiro caractere do nome de fluxo/armazenamento, são reservados para uso pelo OLE. Essa é uma restrição de arquivo composta, não uma restrição de armazenamento estruturado.

</dd> <dt>

<span id="IStorage__SetElementTimes"></span><span id="istorage__setelementtimes"></span><span id="ISTORAGE__SETELEMENTTIMES"></span>[**IStorage::SetElementTimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes)
</dt> <dd>

Define os tempos de modificação, acesso e criação do elemento de armazenamento especificado. A implementação de arquivo composto fornecida pelo COM mantém os tempos de modificação e alteração para objetos de armazenamento internos. Os objetos de armazenamento raiz são suportados pelo sistema de arquivos subjacente (ou [**por ILockBytes).**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) A implementação de arquivo composto não mantém nenhum carimbo de data/hora para fluxos internos. Os carimbos de data/hora sem suporte são relatados como zero, o que permite que o chamador teste o suporte.

</dd> <dt>

<span id="IStorage__SetClass"></span><span id="istorage__setclass"></span><span id="ISTORAGE__SETCLASS"></span>[**IStorage::SetClass**](/windows/desktop/api/Objidl/nf-objidl-istorage-setclass)
</dt> <dd>

Atribui o CLSID especificado a este objeto de armazenamento.

</dd> <dt>

<span id="IStorage__SetStateBits"></span><span id="istorage__setstatebits"></span><span id="ISTORAGE__SETSTATEBITS"></span>[**IStorage::SetStateBits**](/windows/desktop/api/Objidl/nf-objidl-istorage-setstatebits)
</dt> <dd>

Armazena até 32 bits de informações de estado neste objeto de armazenamento. O estado definido por esse método é apenas para uso externo. A implementação de arquivo composto fornecida pelo COM não executa nenhuma ação com base no estado .

</dd> <dt>

<span id="IStorage__Stat"></span><span id="istorage__stat"></span><span id="ISTORAGE__STAT"></span>[**IStorage::Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat)
</dt> <dd>

Recupera a estrutura [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) para este objeto de armazenamento aberto.

</dd> </dl>

## <a name="remarks"></a>Comentários

Se o objeto de armazenamento for aberto no modo simples, o uso dos métodos acima será restrito. Um armazenamento está no modo simples se ele é aberto com o elemento STGM SIMPLE especificado no parâmetro \_ *grfMode* da [**função StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) ou [**StgOpenStorageEx.**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) Para obter mais informações sobre armazenamentos de modo simples, consulte [**Constantes STGM**](stgm-constants.md). Se o objeto de armazenamento de modo simples tiver sido obtido da função **StgCreateStorageEx,** o método [**CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) poderá ser chamado, mas o [**método OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) não poderá. Se o objeto de armazenamento de modo simples tiver sido obtido da **função StgOpenStorageEx,** o método **OpenStream** poderá ser chamado, mas o **método CreateStream** não poderá.

Quando um objeto de armazenamento de modo simples é usado para criar um fluxo, o tamanho mínimo desse fluxo normalmente é de 4096 bytes. Se menos dados são gravados no fluxo, o tamanho é arredondado para até 4096 bytes.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Limites de implementação de arquivo composto](structured-storage-interfaces.md)
</dt> <dt>

[**Ifilllockbytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes)
</dt> <dt>

[**Ilockbytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)
</dt> <dt>

[**Irootstorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage)
</dt> <dt>

[**Istorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[**Istream**](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> <dt>

[**Stgcreatedocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)
</dt> <dt>

[**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex)
</dt> <dt>

[**Stgopenstorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)
</dt> <dt>

[**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)
</dt> </dl>

 

 