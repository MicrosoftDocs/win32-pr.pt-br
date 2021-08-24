---
description: A interface IResize deve ser suportada por qualquer filtro de resizer de vídeo personalizado para o DES (DirectShow Editing Services). Para definir um filtro de resizer personalizado, chame o método IRenderEngine2::SetResizerGUID no mecanismo de renderização.
ms.assetid: 4740dbff-0881-45e8-b382-98ed9d055403
title: Interface IResize (Qedit.h)
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
ms.openlocfilehash: 19aabd7c04cb5350ef3da87e1a20db6b75f6546f0fbcf5af3422c152bcafcf5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818065"
---
# <a name="iresize-interface"></a>Interface IResize

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

A interface deve ser suportada por qualquer filtro de resizer de vídeo personalizado `IResize` para DirectShow DES (Serviços de Edição). Para definir um filtro de resizer personalizado, chame o [**método IRenderEngine2::SetResizerGUID**](irenderengine2-setresizerguid.md) no mecanismo de renderização.

## <a name="members"></a>Membros

A interface **IResize** herda da interface [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IResize** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IResize** tem esses métodos.



| Método                                          | Descrição                                                  |
|:------------------------------------------------|:-------------------------------------------------------------|
| [**get \_ InputSize**](iresize-get-inputsize.md) | Retorna o tamanho de entrada atual do filtro do resizer.<br/>  |
| [**obter \_ MediaType**](iresize-get-mediatype.md) | Retorna o tipo de mídia de saída do filtro do resizer.<br/>   |
| [**obter \_ Tamanho**](iresize-get-size.md)           | Retorna o tamanho da saída atual e o modo de alongamento.<br/> |
| [**put \_ MediaType**](iresize-put-mediatype.md) | Define o tipo de mídia de saída.<br/>                       |
| [**put \_ Size**](iresize-put-size.md)           | Define o tamanho da saída e o modo de alongamento.<br/>            |



 

## <a name="remarks"></a>Comentários

> [!Note]  
> O arquivo de título Qedit.h não é compatível com os headers direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o Qedit.h, baixe [o Microsoft Windows SDK Update para Windows Vista e .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O Qedit.h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versão<br/> | DirectX 9.0 ou posterior<br/>                                                         |
| Cabeçalho<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Fornecendo um resizer de vídeo personalizado](providing-a-custom-video-resizer.md)
</dt> </dl>

 

 
