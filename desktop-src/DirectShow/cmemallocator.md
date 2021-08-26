---
description: Implementa um alocador que dá suporte à interface IMemAllocator.
ms.assetid: c40eccef-d915-4bf3-81b2-b20e000718fb
title: Classe CMemAllocator (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bb94d5fae92d7494a4ac347591e9d571a7765d2be88072559fd74687eea87e97
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915926"
---
# <a name="cmemallocator-class"></a>Classe CMemAllocator

![hierarquia de classe CMemAllocator](images/filter10.png)

Implementa um alocador que dá suporte à interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) .

Essa classe deriva de [**CBaseAllocator**](cbaseallocator.md). Para obter mais informações sobre os alocadores, consulte a documentação do [**CBaseAllocator**](cbaseallocator.md).



| Variáveis de membro protegido                              | Descrição                                                              |
|---------------------------------------------------------|--------------------------------------------------------------------------|
| [**\_pBuffer m**](cmemallocator-m-pbuffer.md)           | Ponteiro para o bloco de memória que contém os buffers.                   |
| Métodos Protegidos                                       | Descrição                                                              |
| [**Informações**](cmemallocator-free.md)                      | Método de espaço reservado; chamado durante uma operação de desconfirmação.                  |
| [**ReallyFree**](cmemallocator-reallyfree.md)          | Libera a memória para os buffers.                                     |
| [**Alocação**](cmemallocator-alloc.md)                    | Aloca memória para os buffers.                                        |
| Métodos públicos                                          | Descrição                                                              |
| [**CMemAllocator**](cmemallocator-cmemallocator.md)    | Método de construtor.                                                      |
| [**~ CMemAllocator**](cmemallocator--cmemallocator.md) | Método destruidor.                                                       |
| [**CreateInstance**](cmemallocator-createinstance.md)  | Cria uma nova instância da classe **CMemAllocator** .                   |
| Métodos IMemAllocator                                   | Descrição                                                              |
| [**SetProperties**](cmemallocator-setproperties.md)    | Especifica o número de buffers a serem alocados e o tamanho de cada buffer. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Fornecendo um alocador personalizado](providing-a-custom-allocator.md)
</dt> </dl>

 

 




