---
description: A interface IAMTimelineEffectable fornece métodos para adicionar efeitos a um objeto de linha do tempo nos serviços de edição do DirectShow (DES) e para manipular os efeitos em um objeto.
ms.assetid: 70f2da64-e16a-4d4d-9522-042b5fa2855c
title: Interface IAMTimelineEffectable (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: bc67483f44515c2ce18825de5b6657d51e2c3826
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779537"
---
# <a name="iamtimelineeffectable-interface"></a>Interface IAMTimelineEffectable

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

A `IAMTimelineEffectable` interface fornece métodos para adicionar efeitos a um objeto de linha do tempo nos [serviços de edição do DirectShow](directshow-editing-services.md) (des) e para manipular os efeitos em um objeto. Todos os objetos que podem ter efeitos aplicados a eles implementam essa interface; Isso inclui fontes, faixas e composições.

Um objeto que implementa essa interface pode ter qualquer número de efeitos. Para cada objeto, o mecanismo de renderização aplica seus efeitos em ordem de prioridade, começando com o nível de prioridade 0.

## <a name="members"></a>Membros

A interface **IAMTimelineEffectable** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IAMTimelineEffectable** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IAMTimelineEffectable** tem esses métodos.



| Método                                                                     | Descrição                                                                   |
|:---------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**EffectGetCount**](iamtimelineeffectable-effectgetcount.md)             | Recupera o número de efeitos neste objeto.<br/>                    |
| [**EffectInsBefore**](iamtimelineeffectable-effectinsbefore.md)           | Insere um efeito no objeto no nível de prioridade especificado.<br/> |
| [**EffectSwapPriorities**](iamtimelineeffectable-effectswappriorities.md) | Alterna os níveis de prioridade de dois efeitos.<br/>                       |
| [**GetEffect**](iamtimelineeffectable-geteffect.md)                       | Recupera o efeito no nível de prioridade especificado.<br/>              |



 

## <a name="remarks"></a>Comentários

> [!Note]  
> O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>QEdit. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



 

 
