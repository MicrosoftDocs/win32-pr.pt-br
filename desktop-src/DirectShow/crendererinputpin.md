---
description: A classe CBaseRendererInputPin implementa um pino de entrada para a classe CBaseRenderer. Exceto quando indicado, os métodos nesta classe delegam os métodos correspondentes na classe CBaseRenderer.
ms.assetid: da3e6aba-c2cc-4fd4-b382-fc4bc7fef774
title: Classe CRendererInputPin (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ec48b31170b2233f211e7e72de81d8792ae9160
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752488"
---
# <a name="crendererinputpin-class"></a>Classe CRendererInputPin

![hierarquia de classe crendererinput PIN](images/rbase01.png)

A classe **CBaseRendererInputPin** implementa um pino de entrada para a classe [**CBaseRenderer**](cbaserenderer.md) . Exceto quando indicado, os métodos nesta classe delegam os métodos correspondentes na classe **CBaseRenderer** .



| Variáveis de membro protegido                                       | Descrição                                                                            |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**\_pRenderer m**](crendererinputpin-m-prenderer.md)            | Ponteiro para o filtro.                                                                 |
| Métodos públicos                                                   | Descrição                                                                            |
| [**CRendererInputPin**](crendererinputpin-crendererinputpin.md) | Método de construtor.                                                                    |
| [**BreakConnect**](crendererinputpin-breakconnect.md)           | Adiciona código personalizado na interrupção de uma conexão.                                       |
| [**CompleteConnect**](crendererinputpin-completeconnect.md)     | Conclui a conexão.                                                              |
| [**CheckMediaType**](crendererinputpin-checkmediatype.md)       | Determina se o PIN pode dar suporte a um tipo de mídia específico.                               |
| [**Activo**](crendererinputpin-active.md)                       | Alterna o PIN para o modo ativo (em pausa ou em execução).                               |
| [**Inativo**](crendererinputpin-inactive.md)                   | Alterna o PIN para um estado inativo e libera a memória do alocador.        |
| [**SetMediaType**](crendererinputpin-setmediatype.md)           | Define o tipo de mídia do PIN.                                                        |
| [**Alocador**](crendererinputpin-allocator.md)                 | Recupera um ponteiro para o alocador de memória padrão.                                   |
| Métodos IPin                                                     | Descrição                                                                            |
| [**QueryId**](crendererinputpin-queryid.md)                     | Recupera um identificador para o PIN.                                                   |
| [**EndOfStream**](crendererinputpin-endofstream.md)             | Informa ao PIN que nenhum dado adicional é esperado até que um novo comando de execução seja emitido. |
| [**BeginFlush**](crendererinputpin-beginflush.md)               | Informa o PIN para iniciar uma operação de liberação.                                            |
| [**EndFlush**](crendererinputpin-endflush.md)                   | Informa o PIN para finalizar uma operação de liberação.                                              |
| Métodos IMemInputPin                                             | Descrição                                                                            |
| [**Recebe**](crendererinputpin-receive.md)                     | Recupera o próximo bloco de dados do fluxo.                                      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




