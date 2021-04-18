---
description: A interface IRenderEngine2 permite que o aplicativo substitua o filtro de redimensionamento de vídeo padrão usado pelos serviços de edição do DirectShow (DES). O mecanismo de renderização básico e o mecanismo de processamento inteligente dão suporte a essa interface.
ms.assetid: 37603c73-e199-431a-9a1e-a40c77755c70
title: Interface IRenderEngine2 (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ed7802cf3d47d745b4e4733bb1fb60c61130b44a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779520"
---
# <a name="irenderengine2-interface"></a>Interface IRenderEngine2

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

A `IRenderEngine2` interface permite que o aplicativo substitua o filtro de redimensionamento de vídeo padrão usado pelos serviços de edição do DirectShow (des). O [mecanismo de renderização básico](basic-render-engine.md) e o [mecanismo de processamento inteligente](smart-render-engine.md) dão suporte a essa interface.

## <a name="members"></a>Membros

A interface **IRenderEngine2** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IRenderEngine2** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IRenderEngine2** tem esses métodos.



| Método                                                  | Descrição                                                                             |
|:--------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [**SetResizerGUID**](irenderengine2-setresizerguid.md) | Especifica o CLSID de um filtro de redimensionamento personalizado fornecido pelo aplicativo.<br/> |



 

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

 

 
