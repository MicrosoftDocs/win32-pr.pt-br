---
description: A classe CRendererPosPassThru manipula comandos de busca para filtros de processador, passando-os upstream para o próximo filtro.
ms.assetid: 7b532177-939c-4cb7-a6fa-c0133f65c768
title: Classe CRendererPosPassThru (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7154dde8adefdb3292107e9c33d7b6a2b54f6af0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757020"
---
# <a name="crendererpospassthru-class"></a>Classe CRendererPosPassThru

![hierarquia de classe CRendererPosPassThru](images/cutil14.png)

A `CRendererPosPassThru` classe lida com os comandos de busca para filtros de processador, passando-os upstream para o próximo filtro.

Essa classe deriva da classe [**CPosPassThru**](cpospassthru.md) . Ele adiciona suporte para armazenar em cache os carimbos de data/hora de exemplos à medida que eles chegam. Use essa classe da mesma maneira que a classe **CPosPassThru** . Consulte a documentação do **CPosPassThru** para obter detalhes.

O filtro de renderizador deve atualizar os `CRendererPosPassThru` carimbos de data/hora em cache do objeto, da seguinte maneira:

-   Para cada exemplo que o filtro recebe, chame o método [**CRendererPosPassThru:: RegisterMediaTime**](crendererpospassthru-registermediatime.md) .
-   Quando o filtro é interrompido ou recebe uma chamada **EndFlush** , chame o método [**CRendererPosPassThru:: ResetMediaTime**](crendererpospassthru-resetmediatime.md) .
-   Quando o filtro recebe uma notificação de fim de fluxo, chame o método [**CRendererPosPassThru:: EOS**](crendererpospassthru-eos.md) .

Para obter um exemplo de como usar essa classe, consulte o código-fonte [**CBaseRenderer**](cbaserenderer.md) .



| Métodos públicos                                                            | Descrição                                                         |
|---------------------------------------------------------------------------|---------------------------------------------------------------------|
| [**CRendererPosPassThru**](crendererpospassthru-crendererpospassthru.md) | Método de construtor.                                                 |
| [**GetMediaTime**](crendererpospassthru-getmediatime.md)                 | Recupera os carimbos de data/hora no exemplo atual.                    |
| [**RegisterMediaTime**](crendererpospassthru-registermediatime.md)       | Armazena em cache os carimbos de data/hora do exemplo atual.                     |
| [**ResetMediaTime**](crendererpospassthru-resetmediatime.md)             | Redefine os carimbos de data/hora em cache como zero.                              |
| [**Electric**](crendererpospassthru-eos.md)                                   | Atualiza os carimbos de data/hora em cache após uma notificação de fim de fluxo. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




