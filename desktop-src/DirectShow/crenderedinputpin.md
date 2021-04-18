---
description: A classe CRenderedInputPin é uma classe base para implementar um PIN de entrada em um processador.
ms.assetid: 644dc6ef-eefa-4dfa-a27e-cab690b6e1db
title: Classe CRenderedInputPin (Amextra. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3fc00b4aa0ce1fc6c8a93fb2fbda2118ad6bb40e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756187"
---
# <a name="crenderedinputpin-class"></a>Classe CRenderedInputPin

![hierarquia de classe crenderedinputpin](images/rbase04.png)

A classe **CRenderedInputPin** é uma classe base para implementar um PIN de entrada em um processador. Essa classe é projetada para filtros de processador que não derivam da classe [**CBaseRenderer**](cbaserenderer.md) . (Os filtros que derivam de **CBaseRenderer** devem usar a classe [**CRendererInputPin**](crendererinputpin.md) para o pino de entrada.)

Para usar essa classe, você deve fazer pelo menos o seguinte:

-   Declare uma nova classe de PIN que herde **CRenderedInputPin**.
-   Na sua classe PIN, declare um objeto de seção crítica para manter o bloqueio de streaming. Você pode usar a classe [**CCritSec**](ccritsec.md) para essa finalidade. Para obter mais informações, consulte [threads and Critical Sections](threads-and-critical-sections.md).
-   Substitua [**CRenderedInputPin:: EndOfStream**](crenderedinputpin-endofstream.md) para manter o bloqueio de streaming.
-   Implemente os métodos [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive), [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md)e [**CBasePin:: GetMediaType**](cbasepin-getmediatype.md) .
-   Em seu filtro, implemente [**CBaseFilter:: GetPin**](cbasefilter-getpin.md) para retornar uma instância da sua classe PIN.

Você pode usar essa classe em um processador que tem mais de um PIN de entrada. Essa classe herda a classe [**CBaseInputPin**](cbaseinputpin.md) .



| Variáveis de membro protegido                                            | Descrição                                                                                                  |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**\_bAtEndOfStream m**](crenderedinputpin-m-batendofstream.md)       | Indica se o fim do fluxo foi atingido.                                                         |
| [**\_bCompleteNotified m**](crenderedinputpin-m-bcompletenotified.md) | Indica se o PIN enviou um evento do [**EC \_ Complete**](ec-complete.md) para o Gerenciador do grafo de filtro. |
| Métodos públicos                                                        | Descrição                                                                                                  |
| [**Ativo**](crenderedinputpin-active.md)                            | Notifica o PIN de que o filtro está ativo agora.                                                              |
| [**CRenderedInputPin**](crenderedinputpin-crenderedinputpin.md)      | Método de construtor.                                                                                          |
| [**Executar**](crenderedinputpin-run.md)                                  | Notifica o PIN de que o filtro agora está em execução.                                                             |
| Métodos IPin                                                          | Descrição                                                                                                  |
| [**EndFlush**](crenderedinputpin-endflush.md)                        | Finaliza uma operação de liberação.                                                                                      |
| [**EndOfStream**](crenderedinputpin-endofstream.md)                  | Notifica o PIN de que nenhum dado adicional é esperado até que o filtro receba um novo comando de execução.            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amextra. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




