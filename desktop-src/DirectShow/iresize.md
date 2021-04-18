---
description: 'A interface IResize deve ter suporte de qualquer filtro personalizado de redimensionador de vídeo para os serviços de edição do DirectShow (DES). Para definir um filtro de redimensionador personalizado, chame o método IRenderEngine2:: SetResizerGUID no mecanismo de processamento.'
ms.assetid: 4740dbff-0881-45e8-b382-98ed9d055403
title: Interface IResize (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1b9684ed6f2d2901159dde5a79bb4563ca0b2bda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760736"
---
# <a name="iresize-interface"></a>Interface IResize

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

A `IResize` interface deve ter suporte de qualquer filtro personalizado de redimensionador de vídeo para os serviços de edição do DirectShow (des). Para definir um filtro de redimensionador personalizado, chame o método [**IRenderEngine2:: SetResizerGUID**](irenderengine2-setresizerguid.md) no mecanismo de processamento.

## <a name="members"></a>Membros

A interface **IResize** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IResize** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IResize** tem esses métodos.



| Método                                          | Descrição                                                  |
|:------------------------------------------------|:-------------------------------------------------------------|
| [**obter \_ Incolocar**](iresize-get-inputsize.md) | Retorna o tamanho de entrada atual do filtro de redimensionador.<br/>  |
| [**obter \_ MediaType**](iresize-get-mediatype.md) | Retorna o tipo de mídia de saída do filtro de redimensionador.<br/>   |
| [**obter \_ tamanho**](iresize-get-size.md)           | Retorna o tamanho de saída atual e o modo de ampliação.<br/> |
| [**colocar \_ MediaType**](iresize-put-mediatype.md) | Define o tipo de mídia de saída.<br/>                       |
| [**tamanho de Put \_**](iresize-put-size.md)           | Define o tamanho de saída e o modo de ampliação.<br/>            |



 

## <a name="remarks"></a>Comentários

> [!Note]  
> O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versão<br/> | DirectX 9,0 ou posterior<br/>                                                         |
| parâmetro<br/>  | <dl> <dt>QEdit. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Fornecendo um redimensionador de vídeo personalizado](providing-a-custom-video-resizer.md)
</dt> </dl>

 

 
