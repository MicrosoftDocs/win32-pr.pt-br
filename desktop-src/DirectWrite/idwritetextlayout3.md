---
title: Interface IDWriteTextLayout3
description: Representa um bloco de texto após ter sido totalmente analisado e formatado. | Interface IDWriteTextLayout3
ms.assetid: a7741740-9524-caf0-650b-56808abcf328
keywords:
- Gravação direta da interface IDWriteTextLayout3
- Gravação direta da interface IDWriteTextLayout3, descrita
topic_type:
- apiref
api_name:
- IDWriteTextLayout3
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f3a6d441c3f7d8ac9bf356bd835f800e026f8c6e27cb083a57ced571ba68fe8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070646"
---
# <a name="idwritetextlayout3-interface"></a>Interface IDWriteTextLayout3

Representa um bloco de texto após ter sido totalmente analisado e formatado.

## <a name="members"></a>Membros

A interface **IDWriteTextLayout3** herda de [**IDWriteTextLayout2**](idwritetextlayout2.md). **IDWriteTextLayout3** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IDWriteTextLayout3** tem esses métodos.



| Método                                                          | Descrição                                                                                                                                                                                                                                                          |
|:----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetLineMetrics**](idwritetextlayout3-getlinemetrics.md)     | Recupera as propriedades de cada linha.<br/>                                                                                                                                                                                                                        |
| [**GetLineSpacing**](idwritetextlayout3-getlinespacing.md)     | Obtém informações de espaçamento de linha.<br/>                                                                                                                                                                                                                            |
| [**InvalidateLayout**](idwritetextlayout3-invalidatelayout.md) | Invalida o layout, forçando o layout a ser remedido antes de chamar as métricas ou as funções de desenho. Isso será útil se a localidade de uma fonte for alterada, e o layout deve ser redesenhado ou se o tamanho de um cliente implementado IDWriteInlineObject for alterado. <br/> |
| [**SetLineSpacing**](idwritetextlayout3-setlinespacing.md)     | Definir espaçamento de linha.<br/>                                                                                                                                                                                                                                         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ aplicativos UWP de aplicativos de desktop \|\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[Aplicativos de aplicativos UWP da área de trabalho R2 \|\]<br/>                          |
| Número mínimo de telefone com suporte<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]<br/> |
| Biblioteca<br/>                  | <dl> <dt>Dwrite. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDWriteTextLayout2**](idwritetextlayout2.md)
</dt> </dl>

 

 





