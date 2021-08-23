---
description: A classe CRenderedInputPin é uma classe base para implementar um pino de entrada em um renderador.
ms.assetid: 644dc6ef-eefa-4dfa-a27e-cab690b6e1db
title: Classe CRenderedInputPin (Amextra.h)
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
ms.openlocfilehash: 139b0ebd887dc81efd19953d48f3caa8fd6377acde8723de23178ee7a0278c8b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119585287"
---
# <a name="crenderedinputpin-class"></a>Classe CRenderedInputPin

![Hierarquia de classes crenderedinputpin](images/rbase04.png)

A **classe CRenderedInputPin** é uma classe base para implementar um pino de entrada em um renderador. Essa classe foi projetada para filtros de renderização que não derivam da [**classe CBaseRenderer.**](cbaserenderer.md) (Filtros derivados **de CBaseRenderer** devem usar a [**classe CRendererInputPin**](crendererinputpin.md) para o pino de entrada.)

Para usar essa classe, você deve fazer pelo menos o seguinte:

-   Declare uma nova classe de pino que herda **CRenderedInputPin.**
-   Na classe pin, declare um objeto de seção crítico para manter o bloqueio de streaming. Você pode usar a [**classe CCritSec**](ccritsec.md) para essa finalidade. Para obter mais informações, [consulte Threads e seções críticas.](threads-and-critical-sections.md)
-   Substitua [**CRenderedInputPin::EndOfStream**](crenderedinputpin-endofstream.md) para manter o bloqueio de streaming.
-   Implemente [**os métodos IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive), [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md)e [**CBasePin::GetMediaType.**](cbasepin-getmediatype.md)
-   No filtro, implemente [**CBaseFilter::GetPin**](cbasefilter-getpin.md) para retornar uma instância da classe de pino.

Você pode usar essa classe em um renderador que tenha mais de um pino de entrada. Essa classe herda a [**classe CBaseInputPin.**](cbaseinputpin.md)



| Variáveis de membro protegidas                                            | Descrição                                                                                                  |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**m \_ bAtEndOfStream**](crenderedinputpin-m-batendofstream.md)       | Indica se o final do fluxo foi atingido.                                                         |
| [**m \_ bCompleteNotified**](crenderedinputpin-m-bcompletenotified.md) | Indica se o pin enviou um evento [**EC \_ COMPLETE**](ec-complete.md) para o Gerenciador Graph Filtro. |
| Métodos públicos                                                        | Descrição                                                                                                  |
| [**Ativo**](crenderedinputpin-active.md)                            | Notifica o pino de que o filtro agora está ativo.                                                              |
| [**CRenderedInputPin**](crenderedinputpin-crenderedinputpin.md)      | Método do construtor.                                                                                          |
| [**Executar**](crenderedinputpin-run.md)                                  | Notifica o pino de que o filtro agora está em execução.                                                             |
| Métodos IPin                                                          | Descrição                                                                                                  |
| [**Endflush**](crenderedinputpin-endflush.md)                        | Encerra uma operação de liberação.                                                                                      |
| [**Endofstream**](crenderedinputpin-endofstream.md)                  | Notifica o pino de que nenhum dado adicional é esperado até que o filtro receba um novo comando de executar.            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amextra.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



 

 




