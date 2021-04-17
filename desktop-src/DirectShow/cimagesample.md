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
ms.openlocfilehash: 2235d50c952ce1b76e4a70eda0341f0fe3c4167c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789975"
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
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




