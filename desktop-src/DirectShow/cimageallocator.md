---
description: A classe CImageAllocator implementa um alocador que gerencia bitmaps independentes de dispositivo (DIBs) do GDI. Essa classe deriva da classe CBaseAllocator. Ele cria amostras de mídia que são implementadas usando a classe CImageSample.
ms.assetid: edda34a5-3916-4a41-9e2f-a19f12df0947
title: Classe CImageAllocator (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ea37dfe8cbbc7baf90e6065f0c54af1a60c3284b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758695"
---
# <a name="cimageallocator-class"></a>Classe CImageAllocator

![hierarquia de classe cimageallocator](images/wutil04.png)

A `CImageAllocator` classe implementa um alocador que gerencia bitmaps (DIBs) independentes de dispositivo GDI. Essa classe deriva da classe [**CBaseAllocator**](cbaseallocator.md) . Ele cria amostras de mídia que são implementadas usando a classe [**CImageSample**](cimagesample.md) .

Um alocador é compartilhado por dois Pins conectados, mas sempre é de propriedade de um dos filtros na conexão. Um filtro que o usa `CImageAllocator` deve controlar se o alocador foi fornecido por si próprio ou por outro filtro. Se o alocador tiver sido fornecido por si só, o filtro proprietário poderá contar com o fato de que todas as amostras de mídia do alocador são objetos **CImageSample** . Portanto, ele pode usar o objeto **CImageSample** para obter informações sobre o DIB, que é armazenado em uma estrutura [**DIBDATA**](dibdata.md) .

O filtro proprietário deve chamar **NotifyMediaType** sempre que o tipo de mídia for alterado.



| Variáveis de membro protegido                                     | Descrição                                                              |
|----------------------------------------------------------------|--------------------------------------------------------------------------|
| [**\_pFilter m**](cimageallocator-m-pfilter.md)                | Ponteiro para o filtro proprietário.                                            |
| [**\_pMediaType m**](cimageallocator-m-pmediatype.md)          | Ponteiro para o tipo de mídia atual.                                       |
| Métodos Protegidos                                              | Descrição                                                              |
| [**Alocação**](cimageallocator-alloc.md)                         | Aloca memória para os buffers.                                        |
| [**CheckSizes**](cimageallocator-checksizes.md)               | Verifica as propriedades de alocador no tipo de mídia atual.              |
| [**CreateDIB**](cimageallocator-createdib.md)                 | Cria um DIB.                                                           |
| [**CreateImageSample**](cimageallocator-createimagesample.md) | Cria um exemplo de mídia. VirtuaisLUNs.                                         |
| [**Gratuita**](cimageallocator-free.md)                           | Libera toda a memória do buffer.                                       |
| Métodos públicos                                                 | Descrição                                                              |
| [**CImageAllocator**](cimageallocator-cimageallocator.md)     | Método de construtor.                                                      |
| [**NotifyMediaType**](cimageallocator-notifymediatype.md)     | Informa o objeto do tipo de mídia atual.                            |
| Métodos IMemAllocator                                          | Descrição                                                              |
| [**SetProperties**](cimageallocator-setproperties.md)         | Especifica o número de buffers a serem alocados e o tamanho de cada buffer. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CDrawImage**](cdrawimage.md)
</dt> </dl>

 

 




