---
description: A classe CImageSample implementa um exemplo de mídia que gerencia um bitmap independente de dispositivo (DIB) GDI.
ms.assetid: 620ea791-458e-441e-8f0c-2184c44c742e
title: Classe CImageSample (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: afd19b6aba7546ec420985adf6d58d3f7acc7546913ec8f1c168c80ad3b7ffda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118402399"
---
# <a name="cimagesample-class"></a>Classe CImageSample

![hierarquia de classe cimagesample](images/wutil03.png)

A `CImageSample` classe implementa um exemplo de mídia que gerencia um bitmap independente de dispositivo (DIB) do GDI. Essa classe deriva da classe [**CMediaSample**](cmediasample.md) . Ele se destina a ser usado com a classe [**CImageAllocator**](cimageallocator.md) . A classe **CImageAllocator** fornece um alocador que cria `CImageSample` objetos.



| Variáveis de membro protegido                        | Descrição                                                       |
|---------------------------------------------------|-------------------------------------------------------------------|
| [**\_DibData m**](cimagesample-m-dibdata.md)      | Contém informações sobre o DIB que esse objeto está gerenciando.  |
| [**\_bInit m**](cimagesample-m-binit.md)          | Indica se o objeto foi inicializado.                |
| Métodos públicos                                    | Descrição                                                       |
| [**CImageSample**](cimagesample-cimagesample.md) | Método de construtor.                                               |
| [**GetDIBData**](cimagesample-getdibdata.md)     | Recupera informações sobre o DIB que esse objeto está gerenciando. |
| [**SetDIBData**](cimagesample-setdibdata.md)     | Define informações sobre o DIB que esse objeto está gerenciando.      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




