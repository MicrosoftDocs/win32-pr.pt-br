---
description: A classe CSeekingPassThru é um objeto auxiliar que cria objetos CPosPassThru e CRendererPosPassThru.
ms.assetid: a748ea5c-d93f-4f80-9d2f-bef5a5c1c2fb
title: Classe CSeekingPassThru (Seekpt. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSeekingPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3ffb8436623cb5ba5f415ceb8bbdafe00e22487da2bbfaba5d02ee4c8f189c10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953765"
---
# <a name="cseekingpassthru-class"></a>Classe CSeekingPassThru

A `CSeekingPassThru` classe é um objeto auxiliar que cria objetos [**CPosPassThru**](cpospassthru.md) e [**CRendererPosPassThru**](crendererpospassthru.md) .

As classes **CPosPassThru** e **CRendererPosPassThru** são objetos auxiliares que passam comandos de busca ascendentes, portanto, a `CSeekingPassThru` classe é um objeto auxiliar para criar objetos auxiliares.

Não é necessário usar essa classe diretamente. Em vez disso, use a função [**CreatePosPassThru**](createpospassthru.md) , que lida com todos os detalhes do uso dessa classe. Ele tem a maior vantagem de carregar o objeto de Quartz.dll, o que reduz um pouco o tamanho do código de seu filtro. Para obter mais informações, consulte [**CPosPassThru**](cpospassthru.md).

A `CSeekingPassThru` classe expõe a interface [**ISeekingPassThru**](/windows/desktop/api/Strmif/nn-strmif-iseekingpassthru) . O método [**ISeekingPassThru:: init**](/windows/desktop/api/Strmif/nf-strmif-iseekingpassthru-init) Inicializa o objeto. Depois que o objeto é inicializado, o filtro pode consultá-lo para as interfaces [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) e [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) .



| Métodos públicos                                                  | Descrição                        |
|-----------------------------------------------------------------|------------------------------------|
| [**CSeekingPassThru**](cseekingpassthru-cseekingpassthru.md)   | Método de construtor.                |
| [**~ CSeekingPassThru**](cseekingpassthru--cseekingpassthru.md) | Método destruidor.                 |
| [**CreateInstance**](cseekingpassthru-createinstance.md)       | Cria uma instância do objeto. |
| Métodos ISeekingPassThru                                        | Descrição                        |
| [**Init**](cseekingpassthru-init.md)                           | Inicializa o objeto.            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Seekpt. h (incluir Fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




