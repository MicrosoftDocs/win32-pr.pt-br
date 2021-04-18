---
title: IStream-implementação de arquivo composto
description: A interface IStream dá suporte à leitura e gravação de dados em objetos de fluxo. Em um objeto de armazenamento estruturado, os objetos de fluxo contêm os dados e os armazenamentos fornecem a estrutura.
ms.assetid: 52474e37-0e14-4dcc-8e04-4442cfd26eb3
keywords:
- Strctd de IStream STG, implementação de arquivo composto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16d15e671521f4a1e81b78579bc1225eccb48898
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/04/2021
ms.locfileid: "105756538"
---
# <a name="istream---compound-file-implementation"></a>IStream-implementação de arquivo composto

A interface [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) dá suporte à leitura e gravação de dados em objetos de fluxo. Em um objeto de armazenamento estruturado, os objetos de fluxo contêm os dados e os armazenamentos fornecem a estrutura. Dados simples podem ser gravados diretamente em um fluxo, mas com mais frequência, os fluxos são elementos aninhados em um objeto de armazenamento. Eles são semelhantes aos arquivos padrão.

A especificação de [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) define mais funcionalidade do que a implementação com dá suporte a. Por exemplo, a interface **IStream** define fluxos de até 2 ⁶ ⁴ bytes de comprimento que exigem um ponteiro de busca de 64 bits. No entanto, a implementação COM só dá suporte a fluxos de até 2 ³ ² bytes de comprimento (4 GB) e as operações de leitura e gravação são sempre limitadas a 2 ³ ² bytes por vez. A implementação COM também não oferece suporte a transacionamento de fluxo ou bloqueio de região.

Para criar um fluxo simples baseado na memória global, obtenha um ponteiro de [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) chamando a função de API [**CreateStreamOnHGlobal**](/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal). Para obter um ponteiro de **IStream** em um objeto de arquivo composto, chame [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) ou [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage). Essas funções recuperam um ponteiro [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) , com o qual você pode chamar [**CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) ou [**OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) para um ponteiro de **IStream** . Em ambos os casos, o mesmo código de implementação de **IStream** é usado.

> [!Note]  
> A implementação do arquivo composto do armazenamento estruturado não tem sucesso em um método [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para [**ISequentialStream**](/windows/desktop/api/Objidl/nn-objidl-isequentialstream), mas inclui os métodos de [**leitura**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read) e [**gravação**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write) por meio do ponteiro de interface [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) .

 

## <a name="when-to-use"></a>Quando usar

Chame os métodos de [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) para ler e gravar dados em um fluxo.

Como os objetos de fluxo podem ser empacotados para outros processos, os aplicativos podem compartilhar os dados em objetos de armazenamento sem precisar usar memória global. Na implementação de arquivo composto COM de objetos de fluxo, os recursos de marshaling personalizados em COM criam uma versão remota do objeto original no novo processo quando os dois processos têm acesso compartilhado à memória. Portanto, a versão remota não precisa se comunicar com o processo original para realizar suas funções.

A versão remota do objeto de fluxo compartilha o mesmo ponteiro de busca que o fluxo original. Se você não quiser compartilhar o ponteiro de busca, use o método [**IStream:: clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone) para fornecer uma cópia do objeto de fluxo para o processo remoto.

> [!Note]
> Se você estiver criando um objeto de fluxo maior do que o heap na memória do computador e estiver usando um identificador **HGLOBAL** para um objeto de memória global, o objeto de fluxo chamará o método [**GlobalRealloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc) internamente quando ele exigir mais memória. Como o **GlobalRealloc** sempre copia dados da origem para o destino, o aumento de um objeto de fluxo de 20 MB para 25 MB, por exemplo, requer grandes quantidades de tempo. Isso ocorre devido ao tamanho dos incrementos copiados e é worsened se houver menos de 45 MB de memória no computador devido à troca de disco.
>
> A solução preferida é implementar um método [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) que usa a memória alocada pelo [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc) em vez de [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc). Isso pode reservar uma grande parte do espaço de endereço virtual e, em seguida, confirmar a memória dentro desse espaço de endereço conforme necessário. Nenhuma cópia de dados ocorre e a memória é confirmada apenas conforme necessário.
>
> Uma alternativa para [**GlobalRealloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc) é chamar o método [**IStream:: SetSize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize) no objeto Stream para aumentar a alocação de memória com antecedência. No entanto, isso não é tão eficiente quanto usar o [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc), conforme descrito acima.

 

## <a name="methods"></a>Métodos

<dl> <dt>

<span id="ISequentialStream__Read"></span><span id="isequentialstream__read"></span><span id="ISEQUENTIALSTREAM__READ"></span>[**ISequentialStream:: ler**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read)
</dt> <dd>

Lê um número especificado de bytes do objeto de fluxo para a memória, a partir do ponteiro de busca atual. Essa implementação retornará S \_ OK se o final do fluxo for atingido durante a leitura. (Isso é o mesmo que o comportamento "fim do arquivo" encontrado no sistema de arquivos FAT do MS-DOS.)

</dd> <dt>

<span id="ISequentialStream__Write"></span><span id="isequentialstream__write"></span><span id="ISEQUENTIALSTREAM__WRITE"></span>[**ISequentialStream:: Write**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write)
</dt> <dd>

Grava um número especificado de bytes no objeto de fluxo a partir do ponteiro de busca atual. Nessa implementação, os objetos de fluxo não são esparsos. Todos os bytes de preenchimento são eventualmente alocados no disco e atribuídos ao fluxo.

</dd> <dt>

<span id="IStream__Seek"></span><span id="istream__seek"></span><span id="ISTREAM__SEEK"></span>[**IStream:: Seek**](/windows/desktop/api/Objidl/nf-objidl-istream-seek)
</dt> <dd>

Altera o ponteiro de busca para um novo local relativo ao início do fluxo, ao fim do fluxo ou ao ponteiro de busca atual.

</dd> <dt>

<span id="IStream__SetSize"></span><span id="istream__setsize"></span><span id="ISTREAM__SETSIZE"></span>[**IStream:: SetSize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize)
</dt> <dd>

Altera o tamanho do objeto de fluxo. Nessa implementação, não há nenhuma garantia de que o espaço alocado será contíguo.

</dd> <dt>

<span id="IStream__CopyTo"></span><span id="istream__copyto"></span><span id="ISTREAM__COPYTO"></span>[**IStream:: CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istream-copyto)
</dt> <dd>

Copia um número especificado de bytes do ponteiro de busca atual no fluxo para o ponteiro de busca atual em outro fluxo.

</dd> <dt>

<span id="IStream__Commit"></span><span id="istream__commit"></span><span id="ISTREAM__COMMIT"></span>[**IStream:: Commit**](/windows/desktop/api/Objidl/nf-objidl-istream-commit)
</dt> <dd>

A implementação do arquivo composto de [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) dá suporte à abertura de fluxos somente no modo direto, não no modo transacionado. Portanto, o método não tem nenhum efeito quando chamado que não libera todos os buffers de memória para o próximo nível de armazenamento.

Nessa implementação, não importa se você confirma as alterações em fluxos, só precisa confirmar as alterações para objetos de armazenamento.

</dd> <dt>

<span id="IStream__Revert"></span><span id="istream__revert"></span><span id="ISTREAM__REVERT"></span>[**IStream:: Revert**](/windows/desktop/api/Objidl/nf-objidl-istream-revert)
</dt> <dd>

Essa implementação não dá suporte a fluxos transacionados, portanto, uma chamada para esse método não tem nenhum efeito.

</dd> <dt>

<span id="IStream__LockRegion"></span><span id="istream__lockregion"></span><span id="ISTREAM__LOCKREGION"></span>[**IStream:: LockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-lockregion)
</dt> <dd>

O bloqueio de intervalo não tem suporte nesta implementação, portanto, uma chamada para esse método não tem nenhum efeito.

</dd> <dt>

<span id="IStream__UnlockRegion"></span><span id="istream__unlockregion"></span><span id="ISTREAM__UNLOCKREGION"></span>[**IStream:: UnlockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-unlockregion)
</dt> <dd>

Remove a restrição de acesso em um intervalo de bytes anteriormente restritos com [**IStream:: LockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-lockregion).

</dd> <dt>

<span id="IStream__Stat"></span><span id="istream__stat"></span><span id="ISTREAM__STAT"></span>[**IStream:: stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)
</dt> <dd>

Recupera a estrutura [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) para este fluxo

</dd> <dt>

<span id="IStream__Clone"></span><span id="istream__clone"></span><span id="ISTREAM__CLONE"></span>[**IStream:: clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone)
</dt> <dd>

Cria um novo objeto de fluxo com seu próprio ponteiro de busca que referencia os mesmos bytes como o fluxo original.

</dd> </dl>

Um [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) de modo simples está sujeito às restrições a seguir.

-   Um fluxo é modo simples se foi criado ou aberto a partir de um armazenamento de modo simples. Um armazenamento será modo simples se for criado ou aberto com o \_ sinalizador simples STGM definido no parâmetro *grfMode* .
-   Não há suporte para os métodos [**clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone) e [**CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istream-copyto) .
-   Há suporte para o método [**stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) , mas o \_ valor NoName de STATFLAG deve ser especificado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> <dt>

[**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[**CreateStreamOnHGlobal**](/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal)
</dt> <dt>

[**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)
</dt> <dt>

[**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)
</dt> </dl>

 

 