---
title: IStream – Implementação de arquivo composto
description: A interface IStream dá suporte à leitura e à escrita de dados para transmitir objetos. Em um objeto de armazenamento estruturado, os objetos de fluxo contêm os dados e os armazenamentos fornecem a estrutura .
ms.assetid: 52474e37-0e14-4dcc-8e04-4442cfd26eb3
keywords:
- IStream Strctd Stg , implementação de arquivo composto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a57a974e44e66d8709a002f9635c41f751e80ab1d3f3875f8eb129cef2b14847
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117961204"
---
# <a name="istream---compound-file-implementation"></a>IStream – Implementação de arquivo composto

A interface [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) dá suporte à leitura e à escrita de dados para transmitir objetos. Em um objeto de armazenamento estruturado, os objetos de fluxo contêm os dados e os armazenamentos fornecem a estrutura . Dados simples podem ser gravados diretamente em um fluxo, mas, com mais frequência, os fluxos são elementos aninhados dentro de um objeto de armazenamento. Eles são semelhantes aos arquivos padrão.

A especificação [**de IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) define mais funcionalidade do que a implementação COM dá suporte. Por exemplo, a interface **IStream** define fluxos de até 2 bytes de comprimento que exigem um ponteiro de busca de 64 bits. No entanto, a implementação COM dá suporte apenas a fluxos de até 2 bytes de comprimento (4 GB) e as operações de leitura e gravação são sempre limitadas a 2 bytes de cada vez. A implementação COM também não dá suporte a transações de fluxo ou bloqueio de região.

Para criar um fluxo simples com base na memória global, obter um ponteiro [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) chamando a função de API [**CreateStreamOnHGlobal**](/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal). Para obter um **ponteiro IStream** dentro de um objeto de arquivo composto, chame [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) ou [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage). Essas funções recuperam um [**ponteiro IStorage,**](/windows/desktop/api/Objidl/nn-objidl-istorage) com o qual você pode chamar [**CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) ou [**OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) para um **ponteiro IStream.** Em ambos os casos, o mesmo **código de implementação de IStream** é usado.

> [!Note]  
> A implementação de arquivo composto do armazenamento estruturado não é bem-sucedida em um método [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para [**ISequentialStream,**](/windows/desktop/api/Objidl/nn-objidl-isequentialstream)mas inclui os métodos [**de**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read) Leitura e Gravação por meio do ponteiro da interface [**IStream.**](/windows/desktop/api/Objidl/nn-objidl-istream) [](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write)

 

## <a name="when-to-use"></a>Quando usar

Chame os métodos de [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) para ler e gravar dados em um fluxo.

Como os objetos de fluxo podem ser marshalados para outros processos, os aplicativos podem compartilhar os dados em objetos de armazenamento sem precisar usar a memória global. Na implementação de arquivo composto COM de objetos de fluxo, os recursos de marshaling personalizados em COM criam uma versão remota do objeto original no novo processo quando os dois processos têm acesso de memória compartilhada. Portanto, a versão remota não precisa se comunicar com o processo original para executar suas funções.

A versão remota do objeto de fluxo compartilha o mesmo ponteiro de busca que o fluxo original. Se você não quiser compartilhar o ponteiro seek, use o método [**IStream::Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone) para fornecer uma cópia do objeto de fluxo para o processo remoto.

> [!Note]
> Se estiver criando um objeto de fluxo maior que o heap na memória do computador e você estiver usando um identificador **HGLOBAL** para um objeto de memória global, o objeto de fluxo chamará o [**método GlobalRealloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc) internamente, o que exigirá mais memória. Como **GlobalRealloc** sempre copia dados da origem para o destino, aumentar um objeto de fluxo de 20 MB para 25 MB, por exemplo, requer grandes quantidades de tempo. Isso ocorre devido ao tamanho dos incrementos copiados e é piorado se houver menos de 45 MB de memória no computador devido à troca de disco.
>
> A solução preferencial é implementar um [**método IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) que usa a memória alocada por [**VirtualAlloc em**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc) vez de [**GlobalAlloc.**](/windows/desktop/api/winbase/nf-winbase-globalalloc) Isso pode reservar uma grande parte do espaço de endereço virtual e, em seguida, fazer commit da memória dentro desse espaço de endereço, conforme necessário. Nenhuma cópia de dados ocorre e a memória é comprometida apenas conforme necessário.
>
> Uma alternativa ao [**GlobalRealloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc) é chamar o [**método IStream::SetSize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize) no objeto de fluxo para aumentar a alocação de memória com antecedência. No entanto, isso não é tão eficiente quanto usar [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc), conforme descrito acima.

 

## <a name="methods"></a>Métodos

<dl> <dt>

<span id="ISequentialStream__Read"></span><span id="isequentialstream__read"></span><span id="ISEQUENTIALSTREAM__READ"></span>[**ISequentialStream::Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read)
</dt> <dd>

Lê um número especificado de bytes do objeto de fluxo para a memória, a partir do ponteiro de busca atual. Essa implementação retornará S \_ OK se o final do fluxo tiver sido atingido durante a leitura. (Isso é o mesmo que o comportamento de "fim do arquivo" encontrado no sistema de arquivos FAT do MS-DOS.)

</dd> <dt>

<span id="ISequentialStream__Write"></span><span id="isequentialstream__write"></span><span id="ISEQUENTIALSTREAM__WRITE"></span>[**ISequentialStream::Write**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write)
</dt> <dd>

Grava um número especificado de bytes no objeto de fluxo começando no ponteiro de busca atual. Nessa implementação, os objetos de fluxo não são esparsos. Todos os bytes de preenchimento são eventualmente alocados no disco e atribuídos ao fluxo.

</dd> <dt>

<span id="IStream__Seek"></span><span id="istream__seek"></span><span id="ISTREAM__SEEK"></span>[**IStream::Seek**](/windows/desktop/api/Objidl/nf-objidl-istream-seek)
</dt> <dd>

Altera o ponteiro de busca para um novo local relativo ao início do fluxo, ao fim do fluxo ou ao ponteiro de busca atual.

</dd> <dt>

<span id="IStream__SetSize"></span><span id="istream__setsize"></span><span id="ISTREAM__SETSIZE"></span>[**IStream::SetSize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize)
</dt> <dd>

Altera o tamanho do objeto de fluxo. Nesta implementação, não há nenhuma garantia de que o espaço alocado será contíguo.

</dd> <dt>

<span id="IStream__CopyTo"></span><span id="istream__copyto"></span><span id="ISTREAM__COPYTO"></span>[**IStream::CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istream-copyto)
</dt> <dd>

Copia um número especificado de bytes do ponteiro de busca atual no fluxo para o ponteiro de busca atual em outro fluxo.

</dd> <dt>

<span id="IStream__Commit"></span><span id="istream__commit"></span><span id="ISTREAM__COMMIT"></span>[**IStream::Commit**](/windows/desktop/api/Objidl/nf-objidl-istream-commit)
</dt> <dd>

A implementação de arquivo composto do [**IStream dá**](/windows/desktop/api/Objidl/nn-objidl-istream) suporte à abertura de fluxos somente no modo direto, não no modo transacionado. Portanto, o método não tem nenhum efeito quando chamado além de liberar todos os buffers de memória para o próximo nível de armazenamento.

Nessa implementação, não importa se você confirma alterações em fluxos, você precisa apenas de alterações de commit para objetos de armazenamento.

</dd> <dt>

<span id="IStream__Revert"></span><span id="istream__revert"></span><span id="ISTREAM__REVERT"></span>[**IStream::Revert**](/windows/desktop/api/Objidl/nf-objidl-istream-revert)
</dt> <dd>

Essa implementação não dá suporte a fluxos transacionados, portanto, uma chamada para esse método não tem nenhum efeito.

</dd> <dt>

<span id="IStream__LockRegion"></span><span id="istream__lockregion"></span><span id="ISTREAM__LOCKREGION"></span>[**IStream::LockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-lockregion)
</dt> <dd>

O bloqueio de intervalo não é suportado por essa implementação, portanto, uma chamada para esse método não tem nenhum efeito.

</dd> <dt>

<span id="IStream__UnlockRegion"></span><span id="istream__unlockregion"></span><span id="ISTREAM__UNLOCKREGION"></span>[**IStream::UnlockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-unlockregion)
</dt> <dd>

Remove a restrição de acesso em um intervalo de bytes anteriormente restrito com [**IStream::LockRegion.**](/windows/desktop/api/Objidl/nf-objidl-istream-lockregion)

</dd> <dt>

<span id="IStream__Stat"></span><span id="istream__stat"></span><span id="ISTREAM__STAT"></span>[**IStream::Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)
</dt> <dd>

Recupera a estrutura [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) para este fluxo

</dd> <dt>

<span id="IStream__Clone"></span><span id="istream__clone"></span><span id="ISTREAM__CLONE"></span>[**IStream::Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone)
</dt> <dd>

Cria um novo objeto de fluxo com seu próprio ponteiro de busca que referencia os mesmos bytes como o fluxo original.

</dd> </dl>

Um [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) de modo simples está sujeito às restrições a seguir.

-   Um fluxo será um modo simples se ele tiver sido criado ou aberto de um armazenamento de modo simples. Um armazenamento será o modo simples se ele for criado ou aberto com o sinalizador STGM \_ SIMPLE definido no parâmetro *grfMode.*
-   Não [**há**](/windows/desktop/api/Objidl/nf-objidl-istream-clone) suporte para os métodos Clone e [**CopyTo.**](/windows/desktop/api/Objidl/nf-objidl-istream-copyto)
-   Há [**suporte**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) para o método Stat, mas o valor STATFLAG \_ NONAME deve ser especificado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Istream**](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> <dt>

[**Istorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[**Createstreamonhglobal**](/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal)
</dt> <dt>

[**Stgcreatedocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)
</dt> <dt>

[**Stgopenstorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)
</dt> </dl>

 

 