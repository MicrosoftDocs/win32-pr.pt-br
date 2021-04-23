---
description: O filtro de renderizador nulo é um renderizador que descarta todas as amostras recebidas, sem exibir ou renderizar os dados de exemplo.
ms.assetid: 2954762d-2ae6-4e38-ac88-5390a081897e
title: Filtro de renderizador nulo (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Null Renderer Filter
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 64647cbcbcc836c400890fb173a29c76f8723029
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908804"
---
# <a name="null-renderer-filter"></a>Filtro de renderizador nulo

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O filtro de renderizador nulo é um renderizador que descarta todas as amostras recebidas, sem exibir ou renderizar os dados de exemplo.



| Label | Valor |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Filtrar interfaces                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) |
| Tipos de mídia de pino de entrada                    | Qualquer tipo de mídia                                                                                                       |
| Interfaces de pino de entrada                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)               |
| Tipos de mídia do pino de saída                   | Não aplicável.                                                                                                      |
| Interfaces de pino de saída                    | Não aplicável.                                                                                                      |
| CLSID do filtro                             | \_NULLRENDERER CLSID                                                                                                  |
| CLSID de página de propriedades                      | Nenhuma página de propriedades.                                                                                                    |
| Executável                               | Qedit.dll                                                                                                            |
| [Núcleo](merit.md)                       | MÉRITO \_ \_ não \_ use                                                                                                  |
| [Categoria do filtro](filter-categories.md) | \_LEGACYAMFILTERCATEGORY CLSID                                                                                        |



 

## <a name="remarks"></a>Comentários

Use esse filtro quando um pino de saída no grafo exigir uma conexão downstream, mas você não quiser renderizar os dados desse PIN. Conectando o pino de saída ao renderizador NULL, você conclui a conexão sem renderizar os dados.

Embora esse filtro não processe nenhum exemplo, ele aguarda o tempo de apresentação de cada amostra antes de descartar o exemplo. Portanto, o grafo será executado com a taxa normal. Se você quiser que o grafo seja executado o mais rapidamente possível, defina o relógio de referência como **nulo**. Para obter mais informações, consulte [definindo o relógio do grafo](setting-the-graph-clock.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>QEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de serviços de edição do DirectShow](directshow-editing-services-objects.md)
</dt> </dl>

 

 




