---
description: A classe CBaseAllocator é uma classe base abstrata que implementa um alocador. Os alocadores expõem a interface IMemAllocator.
ms.assetid: 3c9003d8-f15c-4e85-9712-9aaa87dffdf3
title: Classe CBaseAllocator (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 068dd45ee3ffac5c3b915c3b0cdd8bc87756377e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105767688"
---
# <a name="cbaseallocator-class"></a>Classe CBaseAllocator

![hierarquia de classe CBaseAllocator](images/filter10.png)

A classe **CBaseAllocator** é uma classe base abstrata que implementa um alocador. Os alocadores expõem a interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) .

Um *alocador* é um objeto que aloca buffers de memória. O alocador mantém uma lista de buffers disponíveis. Quando um cliente (geralmente um filtro) solicita um buffer, o alocador recupera um da lista. O cliente preenche o buffer com os dados e pode passar o buffer para outro objeto. Eventualmente, o buffer é liberado e o alocador o retorna à lista de buffers disponíveis.

Cada buffer é encapsulado por um objeto chamado de *exemplo de mídia*. Exemplos de mídia são uma maneira de empacotar ponteiros para blocos de memória dentro da estrutura de Component Object Model (COM). Os exemplos de mídia expõem a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) e são implementados usando a classe [**CMediaSample**](cmediasample.md) . Um exemplo de mídia contém um ponteiro para o buffer associado, que pode ser acessado chamando o método [**IMediaSample:: Getapontarr**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) . Para obter mais informações, consulte [exemplos e alocadores](samples-and-allocators.md).

Para usar essa classe, execute as seguintes etapas:

1.  Chame o método [**CBaseAllocator:: SetProperties**](cbaseallocator-setproperties.md) para especificar os requisitos de buffer, incluindo o número de buffers e o tamanho de cada buffer.
2.  Chame o método [**CBaseAllocator:: Commit**](cbaseallocator-commit.md) para alocar os buffers.
3.  Chame o método [**CBaseAllocator:: GetBuffer**](cbaseallocator-getbuffer.md) para recuperar exemplos de mídia. Esse método é bloqueado até que a próxima amostra se torne disponível.
4.  Quando terminar cada exemplo, chame o método **IUnknown:: Release** no exemplo. O exemplo não é excluído quando sua contagem de referência chega a zero. Em vez disso, o exemplo retorna à lista gratuita do alocador.
5.  Quando você terminar de usar o alocador, chame o método [**CBaseAllocator::D ecommit**](cbaseallocator-decommit.md) para liberar a memória para os buffers.

O método [**Commit**](cbaseallocator-commit.md) chama o método virtual [**CBaseAllocator:: Alloc**](cbaseallocator-alloc.md), que aloca a memória para os buffers. O método [**decommit**](cbaseallocator-decommit.md) chama o método virtual puro [**CBaseAllocator:: Free**](cbaseallocator-free.md), que libera a memória. Classes derivadas devem substituir esses dois métodos.

A classe base [**CMemAllocator**](cmemallocator.md) deriva de **CBaseAllocator**. As classes base de filtro usam a classe **CMemAllocator** .



| Variáveis de membro protegido                                                   | Descrição                                                                                |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**\_lFree m**](cbaseallocator-m-lfree.md)                                   | Ponteiro para uma lista de amostras de mídia disponíveis (gratuita).                                       |
| [**\_hSem m**](cbaseallocator-m-hsem.md)                                     | Semáforo sinalizado quando um exemplo se torna disponível.                                |
| [**\_lWaiting m**](cbaseallocator-m-lwaiting.md)                             | Contagem de threads aguardando exemplos.                                                      |
| [**\_lCount m**](cbaseallocator-m-lcount.md)                                 | Número de buffers a serem fornecidos.                                                              |
| [**\_lAllocated m**](cbaseallocator-m-lallocated.md)                         | Número de buffers alocados no momento.                                                     |
| [**\_lSize m**](cbaseallocator-m-lsize.md)                                   | Tamanho de cada buffer.                                                                       |
| [**\_lAlignment m**](cbaseallocator-m-lalignment.md)                         | Alinhamento de cada buffer.                                                                  |
| [**\_lPrefix m**](cbaseallocator-m-lprefix.md)                               | Prefixo de cada buffer.                                                                     |
| [**\_bChanged m**](cbaseallocator-m-bchanged.md)                             | Sinalizador que indica se os requisitos de buffer foram alterados.                              |
| [**\_bCommitted m**](cbaseallocator-m-bcommitted.md)                         | Sinalizador que indica se o alocador foi confirmado.                                  |
| [**\_bDecommitInProgress m**](cbaseallocator-m-bdecommitinprogress.md)       | Sinalizador que indica se uma operação de desconfirmação está em andamento.                               |
| [**\_pNotify m**](cbaseallocator-m-pnotify.md)                               | Ponteiro para uma interface de retorno de chamada, que é chamada quando exemplos são liberados.                |
| [**\_fEnableReleaseCallback m**](cbaseallocator-m-fenablereleasecallback.md) | Sinalizador que indica se o retorno de chamada de versão está habilitado.                                   |
| Métodos Protegidos                                                            | Descrição                                                                                |
| [**Alocação**](cbaseallocator-alloc.md)                                        | Aloca memória para os buffers. VirtuaisLUNs.                                                 |
| Métodos públicos                                                               | Descrição                                                                                |
| [**CBaseAllocator**](cbaseallocator-cbaseallocator.md)                      | Método de construtor.                                                                        |
| [**~ CBaseAllocator**](cbaseallocator--cbaseallocator.md)                   | Método destruidor.                                                                         |
| [**Setnotificar**](cbaseallocator-setnotify.md)                                | Obsoleto.                                                                                  |
| [**GetFreeCount**](cbaseallocator-getfreecount.md)                          | Recupera o número de amostras de mídia que não estão em uso.                                 |
| [**NotifySample**](cbaseallocator-notifysample.md)                          | Libera todos os threads que estão aguardando exemplos.                                         |
| [**Deesperando**](cbaseallocator-setwaiting.md)                              | Incrementa a contagem de threads em espera.                                                   |
| Métodos virtuais puros                                                         | Descrição                                                                                |
| [**Informações**](cbaseallocator-free.md)                                          | Libera toda a memória do buffer.                                                         |
| Métodos IMemAllocator                                                        | Descrição                                                                                |
| [**SetProperties**](cbaseallocator-setproperties.md)                        | Especifica o número de buffers a serem alocados e o tamanho de cada buffer.                   |
| [**GetProperties**](cbaseallocator-getproperties.md)                        | Recupera o número de buffers que o alocador criará e as propriedades do buffer. |
| [**Compromisso**](cbaseallocator-commit.md)                                      | Aloca a memória para os buffers.                                                      |
| [**Anulação confirmação**](cbaseallocator-decommit.md)                                  | O desconfirma os buffers.                                                                     |
| [**GetBuffer**](cbaseallocator-getbuffer.md)                                | Recupera um exemplo de mídia que contém um buffer.                                           |
| [**ReleaseBuffer**](cbaseallocator-releasebuffer.md)                        | Retorna um exemplo de mídia para a lista de amostras de mídia gratuita.                                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Fornecendo um alocador personalizado](providing-a-custom-allocator.md)
</dt> </dl>

 

 




