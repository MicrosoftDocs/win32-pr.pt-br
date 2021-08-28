---
description: A interface IAMTimelineTrans fornece métodos para manipular transições no DES (Serviços de DirectShow de Edição).
ms.assetid: e29ff0cc-0e48-4a72-8a1b-051ed62c8130
title: Interface IAMTimelineTrans (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 28d7fd409c3ab377393f6c70359d0f6a0a07a3e14c64a77acb2912d9863c6d13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117998719"
---
# <a name="iamtimelinetrans-interface"></a>Interface IAMTimelineTrans

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

A `IAMTimelineTrans` interface fornece métodos para manipular transições DirectShow [DES (Serviços](directshow-editing-services.md) de Edição). Uma transição é uma progressão entre uma camada de vídeo e a composição renderizada de todas as camadas de vídeo com uma prioridade mais baixa. Uma transição pode ser adicionada a qualquer objeto de linha do tempo que expõe a interface [**IAMTimelineTransable.**](iamtimelinetransable.md) Para definir propriedades em uma transição, use a interface [**IPropertySetter.**](ipropertysetter.md)

O objeto de transição de DES é, na verdade, um wrapper para um objeto Transformação DirectX. Qualquer objeto transformação DirectX de duas entradas pode ser usado para implementar o efeito visual para a transição. A Microsoft não dá mais suporte ao desenvolvimento de objetos de Transformação DirectX de terceiros. Para especificar o objeto Transformação DirectX para uma transição, chame o [**método IAMTimelineObj::SetSubObjectGUID.**](iamtimelineobj-setsubobjectguid.md)

Para criar um objeto de transição, chame [**IAMTimeline::CreateEmptyNode com**](iamtimeline-createemptynode.md) o valor TIMELINE \_ MAJOR TYPE \_ \_ TRANSITION. Você pode consultar o ponteiro [**IAMTimelineObj**](iamtimelineobj.md) retornado para a `IAMTimelineTrans` interface.

## <a name="members"></a>Membros

A interface **IAMTimelineTrans** herda da interface [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IAMTimelineTrans** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IAMTimelineTrans** tem esses métodos.



| Método                                                  | Descrição                                                                            |
|:--------------------------------------------------------|:---------------------------------------------------------------------------------------|
| [**GetCutPoint**](iamtimelinetrans-getcutpoint.md)     | Recupera o ponto de corte.<br/>                                                    |
| [**GetCutPoint2**](iamtimelinetrans-getcutpoint2.md)   | Recupera o ponto de corte, como um [**valor REFTIME.**](reftime.md)<br/>             |
| [**GetCutsOnly**](iamtimelinetrans-getcutsonly.md)     | Determina se a transição é renderizada como um corte.<br/>                     |
| [**GetSwapInputs**](iamtimelinetrans-getswapinputs.md) | Recupera um valor que indica se as entradas de transição são trocadas.<br/> |
| [**SetCutPoint**](iamtimelinetrans-setcutpoint.md)     | Define o ponto de corte.<br/>                                                         |
| [**SetCutPoint2**](iamtimelinetrans-setcutpoint2.md)   | Define o ponto de corte, como um [**valor REFTIME.**](reftime.md)<br/>                  |
| [**SetCutsOnly**](iamtimelinetrans-setcutsonly.md)     | Especifica se a transição é renderizada como um corte.<br/>                      |
| [**SetSwapInputs**](iamtimelinetrans-setswapinputs.md) | Especifica se as entradas de transição são trocadas.<br/>                        |



 

## <a name="remarks"></a>Comentários

> [!Note]  
> O arquivo de título Qedit.h não é compatível com os headers direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o Qedit.h, baixe [o Microsoft Windows SDK Update para Windows Vista e .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O Qedit.h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Trabalhando com efeitos e transições](working-with-effects-and-transitions.md)
</dt> </dl>

 

 
