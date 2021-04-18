---
description: A interface IAMTimelineTrans fornece métodos para manipular transições em serviços de edição do DirectShow (DES).
ms.assetid: e29ff0cc-0e48-4a72-8a1b-051ed62c8130
title: Interface IAMTimelineTrans (QEdit. h)
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
ms.openlocfilehash: cd3c39d0a5434befdd5607b340fef936644bf48e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779234"
---
# <a name="iamtimelinetrans-interface"></a>Interface IAMTimelineTrans

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

A `IAMTimelineTrans` interface fornece métodos para manipular transições em [serviços de edição do DirectShow](directshow-editing-services.md) (des). Uma transição é uma progressão entre uma camada de vídeo e a composição renderizada de todas as camadas de vídeo com uma prioridade mais baixa. Uma transição pode ser adicionada a qualquer objeto de linha do tempo que expõe a interface [**IAMTimelineTransable**](iamtimelinetransable.md) . Para definir propriedades em uma transição, use a interface [**IPropertySetter**](ipropertysetter.md) .

O objeto de transição DES é, na verdade, um wrapper para um objeto de transformação do DirectX. Qualquer objeto de transformação DirectX de entrada 2 pode ser usado para implementar o efeito visual para a transição. A Microsoft não dá mais suporte ao desenvolvimento de objetos de transformação DirectX de terceiros. Para especificar o objeto de transformação DirectX para uma transição, chame o método [**IAMTimelineObj:: SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) .

Para criar um objeto de transição, chame [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) com o valor linha de tempo de \_ \_ tipo principal \_ TRANSITION. Você pode consultar o ponteiro [**IAMTimelineObj**](iamtimelineobj.md) retornado para a `IAMTimelineTrans` interface.

## <a name="members"></a>Membros

A interface **IAMTimelineTrans** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IAMTimelineTrans** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IAMTimelineTrans** tem esses métodos.



| Método                                                  | Descrição                                                                            |
|:--------------------------------------------------------|:---------------------------------------------------------------------------------------|
| [**GetCutPoint**](iamtimelinetrans-getcutpoint.md)     | Recupera o ponto de recorte.<br/>                                                    |
| [**GetCutPoint2**](iamtimelinetrans-getcutpoint2.md)   | Recupera o ponto de recorte, como um valor [**REFTIME**](reftime.md) .<br/>             |
| [**GetCutsOnly**](iamtimelinetrans-getcutsonly.md)     | Determina se a transição é renderizada como um recorte.<br/>                     |
| [**GetSwapInputs**](iamtimelinetrans-getswapinputs.md) | Recupera um valor que indica se as entradas de transição são trocadas.<br/> |
| [**SetCutPoint**](iamtimelinetrans-setcutpoint.md)     | Define o ponto de recorte.<br/>                                                         |
| [**SetCutPoint2**](iamtimelinetrans-setcutpoint2.md)   | Define o ponto de recorte, como um valor [**REFTIME**](reftime.md) .<br/>                  |
| [**SetCutsOnly**](iamtimelinetrans-setcutsonly.md)     | Especifica se a transição é renderizada como um recorte.<br/>                      |
| [**SetSwapInputs**](iamtimelinetrans-setswapinputs.md) | Especifica se as entradas de transição são trocadas.<br/>                        |



 

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



## <a name="see-also"></a>Confira também

<dl> <dt>

[Trabalhando com efeitos e transições](working-with-effects-and-transitions.md)
</dt> </dl>

 

 
