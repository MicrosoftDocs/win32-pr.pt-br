---
description: A interface IDxtCompositor define propriedades na transição do compositor. Essa interface é usada internamente pelos serviços de edição do DirectShow (DES) quando ele renderiza a transição do compositor.
ms.assetid: 519f1e00-4b67-4014-906b-043f2478baa7
title: Interface IDxtCompositor (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c2e19f555fe01cbec3763bc1dc76d11aeb5f5ecb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759290"
---
# <a name="idxtcompositor-interface"></a>Interface IDxtCompositor

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

A `IDxtCompositor` interface define propriedades na transição do [compositor](compositor-transition.md) .

Essa interface é usada internamente pelos serviços de edição do DirectShow (DES) quando ele renderiza a transição do compositor. Os aplicativos DES não precisam usar essa interface. Para definir as propriedades em uma transição em DES, use a interface [**IPropertySetter**](ipropertysetter.md) .

A transição do compositor compõe uma imagem em primeiro plano em uma imagem de plano de fundo. O *retângulo de origem* define a seção da imagem em primeiro plano que é composta. O *retângulo de destino* define a seção da imagem de plano de fundo que recebe a imagem em primeiro plano. O diagrama a seguir ilustra esses retângulos.

![Propriedades de transição do compositor](images/compmeasure.png)

## <a name="members"></a>Membros

A interface **IDxtCompositor** herda de **IDXEffect**. **IDxtCompositor** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IDxtCompositor** tem esses métodos.



| Método                                                   | Descrição                                                         |
|:---------------------------------------------------------|:--------------------------------------------------------------------|
| [**obter \_ altura**](idxtcompositor-get-height.md)         | Recupera a altura do retângulo de destino.<br/>            |
| [**obter \_ OffsetX**](idxtcompositor-get-offsetx.md)       | Recupera o deslocamento horizontal do retângulo de destino.<br/> |
| [**obter \_ OffsetY**](idxtcompositor-get-offsety.md)       | Recupera o deslocamento vertical do retângulo de destino.<br/>   |
| [**obter \_ SrcHeight**](idxtcompositor-get-srcheight.md)   | Recupera a altura do retângulo de origem.<br/>            |
| [**obter \_ SrcOffsetX**](idxtcompositor-get-srcoffsetx.md) | Recupera o deslocamento horizontal do retângulo de origem.<br/> |
| [**obter \_ SrcOffsetY**](idxtcompositor-get-srcoffsety.md) | Recupera o deslocamento vertical do retângulo de origem.<br/>   |
| [**obter \_ SrcWidth**](idxtcompositor-get-srcwidth.md)     | Recupera a largura do retângulo de origem.<br/>             |
| [**obter \_ largura**](idxtcompositor-get-width.md)           | Recupera a largura do retângulo de destino.<br/>             |
| [**colocar \_ altura**](idxtcompositor-put-height.md)         | Especifica a altura do retângulo de destino.<br/>            |
| [**colocar \_ OffsetX**](idxtcompositor-put-offsetx.md)       | Especifica o deslocamento horizontal do retângulo de destino.<br/> |
| [**colocar \_ OffsetY**](idxtcompositor-put-offsety.md)       | Especifica o deslocamento vertical do retângulo de destino.<br/>   |
| [**colocar \_ SrcHeight**](idxtcompositor-put-srcheight.md)   | Especifica a altura do retângulo de origem.<br/>            |
| [**colocar \_ SrcOffsetX**](idxtcompositor-put-srcoffsetx.md) | Especifica o deslocamento horizontal do retângulo de origem.<br/> |
| [**colocar \_ SrcOffsetY**](idxtcompositor-put-srcoffsety.md) | Especifica o deslocamento vertical do retângulo de origem.<br/>   |
| [**colocar \_ SrcWidth**](idxtcompositor-put-srcwidth.md)     | Especifica a largura do retângulo de origem.<br/>             |
| [**colocar \_ largura**](idxtcompositor-put-width.md)           | Especifica a largura do retângulo de destino.<br/>             |



 

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



 

 




