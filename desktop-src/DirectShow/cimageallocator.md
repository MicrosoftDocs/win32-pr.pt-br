---
description: A classe CImageAllocator implementa um alocador que gerencia DIBs (bitmaps independentes de dispositivo) GDI. Essa classe deriva da classe CBaseAllocator. Ele cria exemplos de mídia que são implementados usando a classe CImageSample.
ms.assetid: edda34a5-3916-4a41-9e2f-a19f12df0947
title: Classe CImageAllocator (Winutil.h)
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
ms.openlocfilehash: 383b9c2ca992db66e7bf397e42dcb8aaaa4bdb66251ddfd67f4b5175d87058aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118402574"
---
# <a name="cimageallocator-class"></a>Classe CImageAllocator

![Hierarquia de classes cimageallocator](images/wutil04.png)

A `CImageAllocator` classe implementa um alocador que gerencia DIBs (bitmaps independentes de dispositivo) GDI. Essa classe deriva da [**classe CBaseAllocator.**](cbaseallocator.md) Ele cria exemplos de mídia que são implementados usando a [**classe CImageSample.**](cimagesample.md)

Um alocador é compartilhado por dois pinos conectados, mas sempre pertence a um dos filtros na conexão. Um filtro que usa deve controlar se o alocador foi fornecido por si mesmo `CImageAllocator` ou pelo outro filtro. Se o alocador foi fornecido por si só, o filtro de propriedade pode contar com o fato de que todos os exemplos de mídia do alocador são **objetos CImageSample.** Portanto, ele pode usar o **objeto CImageSample** para obter informações sobre o DIB, que é armazenado em uma [**estrutura DIBDATA.**](dibdata.md)

O filtro de propriedade deve chamar **NotifyMediaType** sempre que o tipo de mídia mudar.



| Variáveis de membro protegidas                                     | Descrição                                                              |
|----------------------------------------------------------------|--------------------------------------------------------------------------|
| [**m \_ pFilter**](cimageallocator-m-pfilter.md)                | Ponteiro para o filtro de propriedade.                                            |
| [**m \_ pMediaType**](cimageallocator-m-pmediatype.md)          | Ponteiro para o tipo de mídia atual.                                       |
| Métodos Protegidos                                              | Descrição                                                              |
| [**Alloc**](cimageallocator-alloc.md)                         | Aloca memória para os buffers.                                        |
| [**CheckSizes**](cimageallocator-checksizes.md)               | Verifica as propriedades do alocador em relação ao tipo de mídia atual.              |
| [**CreateDIB**](cimageallocator-createdib.md)                 | Cria um DIB.                                                           |
| [**CreateImageSample**](cimageallocator-createimagesample.md) | Cria um exemplo de mídia. Virtual.                                         |
| [**Gratuito**](cimageallocator-free.md)                           | Libera toda a memória do buffer.                                       |
| Métodos públicos                                                 | Descrição                                                              |
| [**CImageAllocator**](cimageallocator-cimageallocator.md)     | Método do construtor.                                                      |
| [**NotifyMediaType**](cimageallocator-notifymediatype.md)     | Informa o objeto do tipo de mídia atual.                            |
| Métodos IMemAllocator                                          | Descrição                                                              |
| [**SetProperties**](cimageallocator-setproperties.md)         | Especifica o número de buffers a alocar e o tamanho de cada buffer. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CDrawImage**](cdrawimage.md)
</dt> </dl>

 

 




