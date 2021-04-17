---
description: A interface ISmartRenderEngine fornece métodos que dão suporte à recompactação inteligente nos serviços de edição do DirectShow (DES). O mecanismo de processamento inteligente expõe essa interface.
ms.assetid: 0e03708f-e471-4188-a212-ec5e951d20fa
title: Interface ISmartRenderEngine (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISmartRenderEngine
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4e82ba73764adc27ff366533c3b5cfdc2eebc7e3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759532"
---
# <a name="ismartrenderengine-interface"></a>Interface ISmartRenderEngine

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

A `ISmartRenderEngine` interface fornece métodos que dão suporte à recompactação inteligente nos [serviços de edição do DirectShow](directshow-editing-services.md) (des). O mecanismo de processamento inteligente expõe essa interface.

## <a name="members"></a>Membros

A interface **ISmartRenderEngine** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ISmartRenderEngine** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ISmartRenderEngine** tem esses métodos.



| Método                                                                | Descrição                                                                          |
|:----------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [**GetGroupCompressor**](ismartrenderengine-getgroupcompressor.md)   | Recupera o filtro de compactação para o grupo especificado.<br/>                 |
| [**SetFindCompressorCB**](ismartrenderengine-setfindcompressorcb.md) | Não implementado.<br/>                                                          |
| [**SetGroupCompressor**](ismartrenderengine-setgroupcompressor.md)   | Especifica um filtro de compactação a ser usado ao renderizar o grupo especificado.<br/> |



 

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

[Renderizando um projeto](rendering-a-project.md)
</dt> </dl>

 

 
