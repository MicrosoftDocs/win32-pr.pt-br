---
description: a interface IAMTimelineEffect fornece métodos para manipular efeitos de áudio e vídeo em serviços de edição DirectShow (DES).
ms.assetid: 3cc8a5f8-3f57-4e2b-82dd-827e04c771f7
title: Interface IAMTimelineEffect (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffect
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f710693c967e1f0ac73c69534e8ac90a65d6603e749cd2aeae6a355ed8517415
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052756"
---
# <a name="iamtimelineeffect-interface"></a>Interface IAMTimelineEffect

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

a `IAMTimelineEffect` interface fornece métodos para manipular efeitos de áudio e vídeo em [serviços de edição DirectShow](directshow-editing-services.md) (DES). Um efeito pode ser adicionado a qualquer objeto de linha do tempo que expõe a interface [**IAMTimelineEffectable**](iamtimelineeffectable.md) . Para definir propriedades em um efeito, use a interface [**IPropertySetter**](ipropertysetter.md) .

O objeto de efeito DES é, na verdade, um wrapper para um dos dois outros objetos:

-   para efeitos de áudio, qualquer DirectShow filtro de efeito de áudio.
-   Para efeitos de vídeo, e um objeto de transformação DirectX de entrada.

A Microsoft não dá mais suporte ao desenvolvimento de objetos de transformação DirectX de terceiros.

Para especificar o filtro ou o objeto de transformação DirectX para um efeito, chame o método [**IAMTimelineObj:: SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) .

Para criar um objeto de efeito, chame [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) com o valor linha de tempo \_ principal \_ efeito de tipo \_ . Você pode consultar o ponteiro [**IAMTimelineObj**](iamtimelineobj.md) retornado para a `IAMTimelineEffect` interface.

## <a name="members"></a>Membros

A interface **IAMTimelineEffect** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IAMTimelineEffect** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IAMTimelineEffect** tem esses métodos.



| Método                                                           | Descrição                                       |
|:-----------------------------------------------------------------|:--------------------------------------------------|
| [**EffectGetPriority**](iamtimelineeffect-effectgetpriority.md) | Recupera o nível de prioridade do efeito.<br/> |



 

## <a name="remarks"></a>Comentários

> [!Note]  
> O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.

 

> [!Note]  
> para obter o Qedit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>QEdit. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Trabalhando com efeitos e transições](working-with-effects-and-transitions.md)
</dt> </dl>

 

 
