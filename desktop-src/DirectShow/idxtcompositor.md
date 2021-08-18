---
description: A interface IDxtCompositor define propriedades na transição compositor. Essa interface é usada internamente DirectShow DES (Serviços de Edição) quando renderiza a transição compositora.
ms.assetid: 519f1e00-4b67-4014-906b-043f2478baa7
title: Interface IDxtCompositor (Qedit.h)
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
ms.openlocfilehash: dd59f62a4382ae6023a18792ce3547f67b49c9e8ae49e9de7c9c8409bccd788d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997686"
---
# <a name="idxtcompositor-interface"></a>Interface IDxtCompositor

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

A `IDxtCompositor` interface define propriedades na transição [compositor.](compositor-transition.md)

Essa interface é usada internamente DirectShow DES (Serviços de Edição) ao renderizar a transição compositora. Os aplicativos DES não têm que usar essa interface. Para definir as propriedades em uma transição no DES, use a interface [**IPropertySetter.**](ipropertysetter.md)

A transição compositor composição de uma imagem de primeiro plano em uma imagem de plano de fundo. O *retângulo de* origem define a seção da imagem de primeiro plano composta. O *retângulo de* destino define a seção da imagem de plano de fundo que recebe a imagem de primeiro plano. O diagrama a seguir ilustra esses retângulos.

![propriedades de transição do compositor](images/compmeasure.png)

## <a name="members"></a>Membros

A **interface IDxtCompositor** herda de **IDXEffect.** **O IDxtCompositor** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A **interface IDxtCompositor** tem esses métodos.



| Método                                                   | Descrição                                                         |
|:---------------------------------------------------------|:--------------------------------------------------------------------|
| [**obter \_ altura**](idxtcompositor-get-height.md)         | Recupera a altura do retângulo de destino.<br/>            |
| [**get \_ OffsetX**](idxtcompositor-get-offsetx.md)       | Recupera o deslocamento horizontal do retângulo de destino.<br/> |
| [**obter \_ OffsetY**](idxtcompositor-get-offsety.md)       | Recupera o deslocamento vertical do retângulo de destino.<br/>   |
| [**get \_ SrcHeight**](idxtcompositor-get-srcheight.md)   | Recupera a altura do retângulo de origem.<br/>            |
| [**get \_ SrcOffsetX**](idxtcompositor-get-srcoffsetx.md) | Recupera o deslocamento horizontal do retângulo de origem.<br/> |
| [**get \_ SrcOffsetY**](idxtcompositor-get-srcoffsety.md) | Recupera o deslocamento vertical do retângulo de origem.<br/>   |
| [**get \_ SrcWidth**](idxtcompositor-get-srcwidth.md)     | Recupera a largura do retângulo de origem.<br/>             |
| [**obter \_ Largura**](idxtcompositor-get-width.md)           | Recupera a largura do retângulo de destino.<br/>             |
| [**put \_ Height**](idxtcompositor-put-height.md)         | Especifica a altura do retângulo de destino.<br/>            |
| [**put \_ OffsetX**](idxtcompositor-put-offsetx.md)       | Especifica o deslocamento horizontal do retângulo de destino.<br/> |
| [**put \_ OffsetY**](idxtcompositor-put-offsety.md)       | Especifica o deslocamento vertical do retângulo de destino.<br/>   |
| [**put \_ SrcHeight**](idxtcompositor-put-srcheight.md)   | Especifica a altura do retângulo de origem.<br/>            |
| [**put \_ SrcOffsetX**](idxtcompositor-put-srcoffsetx.md) | Especifica o deslocamento horizontal do retângulo de origem.<br/> |
| [**put \_ SrcOffsetY**](idxtcompositor-put-srcoffsety.md) | Especifica o deslocamento vertical do retângulo de origem.<br/>   |
| [**put \_ SrcWidth**](idxtcompositor-put-srcwidth.md)     | Especifica a largura do retângulo de origem.<br/>             |
| [**put \_ Width**](idxtcompositor-put-width.md)           | Especifica a largura do retângulo de destino.<br/>             |



 

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



 

 




