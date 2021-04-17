---
title: Implementação de arquivo de IStorage-Compound
description: A implementação do arquivo composto do IStorage permite criar e gerenciar subarmazenamentos e fluxos em um objeto de armazenamento que reside em um objeto de arquivo composto.
ms.assetid: 2a2253f6-d3d3-403e-a9ba-53a541c7a31e
keywords:
- IStorage Strctd STG, implementação de arquivo composto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bf37b24a7c68bbe357d99f94e666bfcb613c472
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105753704"
---
# <a name="istorage-compound-file-implementation"></a>Implementação de arquivo de IStorage-Compound

A implementação do arquivo composto do [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) permite criar e gerenciar subarmazenamentos e fluxos em um objeto de armazenamento que reside em um objeto de arquivo composto. Para criar um objeto de arquivo composto e obter um ponteiro **IStorage** , chame a função de API [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex). Para abrir um objeto de arquivo composto existente e obter seu ponteiro raiz **IStorage** , chame [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex).

Os aplicativos que usam o armazenamento composto devem ser registrados no HKEY \_ classes \_ root \\ SystemFileAssociations e devem fornecer seus próprios manipuladores de propriedade. Para obter mais informações, consulte a seção "registrando verbos e outras informações de associação de arquivo" do [registro do aplicativo](/windows/desktop/shell/app-registration).

## <a name="when-to-use"></a>Quando usar

A maioria dos aplicativos usa essa implementação para criar e gerenciar armazenamentos e fluxos.

## <a name="methods"></a>Métodos

<dl> <dt>

<span id="IStorage__CreateStream"></span><span id="istorage__createstream"></span><span id="ISTORAGE__CREATESTREAM"></span>[**IStorage:: CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream)
</dt> <dd>

Cria e abre um objeto de fluxo com o nome especificado contido neste objeto de armazenamento. O nome não deve exceder 31 caracteres de comprimento (não incluindo o terminador de cadeia de caracteres). Os caracteres de 000 a 01F, servindo como o primeiro caractere do nome de fluxo/armazenamento, são reservados para uso pelo OLE. Essa é uma restrição de arquivo composto, não uma restrição de armazenamento estruturada. A implementação de arquivo composto fornecido pelo COM do método [**IStorage:: CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) não oferece suporte aos seguintes comportamentos:

-   \_Não há suporte para o sinalizador STGM DELETEONRELEASE.
-   Não há suporte para o modo transacionado ( \_ transacionado STGM) para objetos de fluxo.
-   Não há suporte para a abertura do mesmo fluxo mais de uma vez no mesmo armazenamento. O \_ sinalizador de modo de compartilhamento exclusivo do STGM share \_ deve ser especificado no parâmetro *grfMode* .

</dd> <dt>

<span id="IStorage__OpenStream"></span><span id="istorage__openstream"></span><span id="ISTORAGE__OPENSTREAM"></span>[**IStorage:: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream)
</dt> <dd>

Abre um objeto de fluxo existente dentro desse objeto de armazenamento usando os modos de acesso especificados no parâmetro *grfMode* . Os caracteres de 000 a 01F, servindo como o primeiro caractere do nome de fluxo/armazenamento, são reservados para uso pelo OLE. Essa é uma restrição de arquivo composto, não uma restrição de armazenamento estruturada. A implementação do arquivo composto fornecido pelo COM do método [**IStorage:: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) não oferece suporte ao seguinte comportamento:

-   O \_ sinalizador STGM DELETEONRELEASE.
-   Modo transacionado (STGM \_ transacionado) para objetos de fluxo.
-   Abrindo o mesmo fluxo mais de uma vez do mesmo armazenamento. O \_ sinalizador exclusivo de compartilhamento de STGM \_ deve ser especificado.

</dd> <dt>

<span id="IStorage__CreateStorage"></span><span id="istorage__createstorage"></span><span id="ISTORAGE__CREATESTORAGE"></span>[**IStorage:: CreateStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage)
</dt> <dd>

Cria e abre um novo objeto de armazenamento com o nome especificado no modo de acesso especificado. O nome não deve exceder 31 caracteres de comprimento (não incluindo o terminador de cadeia de caracteres). Os caracteres de 000 a 01F, servindo como o primeiro caractere do nome de fluxo/armazenamento, são reservados para uso pelo OLE. Essa é uma restrição de arquivo composto, não uma restrição de armazenamento estruturada. A implementação do arquivo composto fornecido pelo COM do método [**IStorage:: CreateStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage) não oferece suporte ao seguinte comportamento:

-   O \_ sinalizador de prioridade STGM para armazenamentos não raiz.
-   Abrindo o mesmo objeto de armazenamento mais de uma vez do mesmo armazenamento pai. O \_ sinalizador exclusivo de compartilhamento de STGM \_ deve ser especificado.
-   O \_ sinalizador STGM DELETEONRELEASE. Se esse sinalizador for especificado, a função retornará STG \_ E \_ INVALIDFLAG.

</dd> <dt>

<span id="IStorage__OpenStorage"></span><span id="istorage__openstorage"></span><span id="ISTORAGE__OPENSTORAGE"></span>[**IStorage:: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage)
</dt> <dd>

Abre um objeto de armazenamento existente com o nome especificado no modo de acesso especificado. Os caracteres de 000 a 01F, servindo como o primeiro caractere do nome de fluxo/armazenamento, são reservados para uso pelo OLE. Essa é uma restrição de arquivo composto, não uma restrição de armazenamento estruturada. A implementação do arquivo composto fornecido pelo COM do método [**IStorage:: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) não oferece suporte ao seguinte comportamento:

-   O \_ sinalizador de prioridade STGM para armazenamentos não raiz.
-   Abrindo o mesmo objeto de armazenamento mais de uma vez do mesmo armazenamento pai. O \_ sinalizador exclusivo de compartilhamento de STGM \_ deve ser especificado.
-   O \_ sinalizador STGM DELETEONRELEASE. Se esse sinalizador for especificado, a função retornará STG \_ E \_ INVALIDFUNCTION.

</dd> <dt>

<span id="IStorage__CopyTo"></span><span id="istorage__copyto"></span><span id="ISTORAGE__COPYTO"></span>[**IStorage:: CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto)
</dt> <dd>

Copia apenas os subarmazenamentos e os fluxos deste objeto de armazenamento aberto em outro objeto de armazenamento. O parâmetro *rgiidExclude* pode ser definido para o \_ IStream de IID para copiar somente os subarmazenamentos ou para o IStorage de IID \_ para copiar somente os fluxos.

</dd> <dt>

<span id="IStorage__MoveElementTo"></span><span id="istorage__moveelementto"></span><span id="ISTORAGE__MOVEELEMENTTO"></span>[**IStorage:: MoveElementTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-moveelementto)
</dt> <dd>

Copia ou move um subarmazenamento ou fluxo deste objeto de armazenamento para outro objeto de armazenamento.

</dd> <dt>

<span id="IStorage__Commit"></span><span id="istorage__commit"></span><span id="ISTORAGE__COMMIT"></span>[**IStorage:: Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit)
</dt> <dd>

Garante que todas as alterações feitas em um objeto de armazenamento aberto no modo transacionado sejam refletidas no armazenamento pai; para um armazenamento raiz, reflete as alterações no dispositivo real; por exemplo, um arquivo em disco. Para um objeto de armazenamento raiz aberto no modo direto, esse método não tem efeito, exceto para liberar todos os buffers de memória para o disco. Para objetos de armazenamento não raiz no modo direto, esse método não tem efeito.

A implementação de arquivos compostos fornecidos pelo COM usa um processo de confirmação de duas fases, a menos que STGC \_ substitua seja especificado no parâmetro *grfCommitFlags* . Esse processo de duas fases garante a robustez dos dados, caso a operação de confirmação falhe. Primeiro, todos os novos dados são gravados no espaço não utilizado no arquivo subjacente. Se necessário, o novo espaço é alocado para o arquivo. Depois que essa etapa for concluída, uma tabela no arquivo será atualizada usando uma operação de gravação de setor único para indicar que os novos dados serão usados no lugar do antigo. Os dados antigos tornam-se espaço livre para serem usados na próxima operação de confirmação. Assim, os dados antigos estarão disponíveis e poderão ser restaurados se ocorrer um erro durante a confirmação das alterações. Se STGC \_ overwrite for especificado, uma única operação de confirmação de fase será usada. Para obter mais informações sobre sinalizadores de modo transacionado, consulte enumeração [**STGC**](/windows/win32/api/wtypes/ne-wtypes-stgc) .

</dd> <dt>

<span id="IStorage__Revert"></span><span id="istorage__revert"></span><span id="ISTORAGE__REVERT"></span>[**IStorage:: Revert**](/windows/desktop/api/Objidl/nf-objidl-istorage-revert)
</dt> <dd>

Descarta todas as alterações feitas no objeto de armazenamento desde a última operação de confirmação.

</dd> <dt>

<span id="IStorage__EnumElements"></span><span id="istorage__enumelements"></span><span id="ISTORAGE__ENUMELEMENTS"></span>[**IStorage:: EnumElements**](/windows/desktop/api/Objidl/nf-objidl-istorage-enumelements)
</dt> <dd>

Cria e recupera um ponteiro para um objeto enumerador que pode ser usado para enumerar os objetos de armazenamento e de fluxo contidos neste objeto de armazenamento. A implementação do arquivo composto fornecido pelo COM tira um instantâneo dessas informações. Portanto, as alterações nos fluxos e armazenamentos não são refletidas no enumerador até que um novo enumerador seja obtido.

</dd> <dt>

<span id="IStorage__DestroyElement"></span><span id="istorage__destroyelement"></span><span id="ISTORAGE__DESTROYELEMENT"></span>[**IStorage::D estroyElement**](/windows/desktop/api/Objidl/nf-objidl-istorage-destroyelement)
</dt> <dd>

Remove o elemento especificado (subarmazenamento ou fluxo) deste objeto de armazenamento.

</dd> <dt>

<span id="IStorage__RenameElement"></span><span id="istorage__renameelement"></span><span id="ISTORAGE__RENAMEELEMENT"></span>[**IStorage:: renomeelement**](/windows/desktop/api/Objidl/nf-objidl-istorage-renameelement)
</dt> <dd>

Renomeia o subarmazenamento ou fluxo especificado neste objeto de armazenamento. Os caracteres de 000 a 01F, servindo como o primeiro caractere do nome de fluxo/armazenamento, são reservados para uso pelo OLE. Essa é uma restrição de arquivo composto, não uma restrição de armazenamento estruturada.

</dd> <dt>

<span id="IStorage__SetElementTimes"></span><span id="istorage__setelementtimes"></span><span id="ISTORAGE__SETELEMENTTIMES"></span>[**IStorage:: SetElementTimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes)
</dt> <dd>

Define a modificação, o acesso e os tempos de criação do elemento de armazenamento especificado. A implementação de arquivo composto fornecida pelo COM mantém tempos de modificação e alteração para objetos de armazenamento interno. Os objetos de armazenamento raiz dão suporte para qualquer suporte do sistema de arquivos subjacente (ou por [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)). A implementação do arquivo composto não mantém carimbos de data/hora para fluxos internos. Os carimbos de data/hora sem suporte são relatados como zero, o que permite que o chamador teste o suporte.

</dd> <dt>

<span id="IStorage__SetClass"></span><span id="istorage__setclass"></span><span id="ISTORAGE__SETCLASS"></span>[**IStorage:: SetClass**](/windows/desktop/api/Objidl/nf-objidl-istorage-setclass)
</dt> <dd>

Atribui o CLSID especificado a este objeto de armazenamento.

</dd> <dt>

<span id="IStorage__SetStateBits"></span><span id="istorage__setstatebits"></span><span id="ISTORAGE__SETSTATEBITS"></span>[**IStorage:: SetStateBits**](/windows/desktop/api/Objidl/nf-objidl-istorage-setstatebits)
</dt> <dd>

Armazena até 32 bits de informações de estado neste objeto de armazenamento. O estado definido por esse método é somente para uso externo. A implementação do arquivo composto fornecido pelo COM não executa nenhuma ação com base no estado.

</dd> <dt>

<span id="IStorage__Stat"></span><span id="istorage__stat"></span><span id="ISTORAGE__STAT"></span>[**IStorage:: stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat)
</dt> <dd>

Recupera a estrutura [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) para este objeto de armazenamento aberto.

</dd> </dl>

## <a name="remarks"></a>Comentários

Se o objeto de armazenamento for aberto no modo simples, o uso dos métodos acima será restrito. Um armazenamento estará no modo simples se for aberto com o \_ elemento simples STGM especificado no parâmetro *grfMode* da função [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) ou [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) . Para obter mais informações sobre armazenamentos de modo simples, consulte [**constantes STGM**](stgm-constants.md). Se o objeto de armazenamento de modo simples foi obtido da função **StgCreateStorageEx** , o método [**CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) pode ser chamado, mas o método [**OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) não pode. Se o objeto de armazenamento de modo simples foi obtido da função **StgOpenStorageEx** , o método **OpenStream** pode ser chamado, mas o método **CreateStream** não pode.

Quando um objeto de armazenamento de modo simples é usado para criar um fluxo, o tamanho mínimo desse fluxo normalmente é de 4096 bytes. Se menos dados forem gravados no fluxo, o tamanho será arredondado para até 4096 bytes.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Limites de implementação de arquivo composto](structured-storage-interfaces.md)
</dt> <dt>

[**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes)
</dt> <dt>

[**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)
</dt> <dt>

[**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage)
</dt> <dt>

[**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> <dt>

[**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)
</dt> <dt>

[**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex)
</dt> <dt>

[**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)
</dt> <dt>

[**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)
</dt> </dl>

 

 