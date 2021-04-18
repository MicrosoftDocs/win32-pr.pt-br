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
ms.openlocfilehash: 78a7a9203245939e40b522e0ef5998be0764085a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105759003"
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
| Cliente mínimo com suporte<br/> | Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]<br/>                          |
| Número mínimo de telefone com suporte<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]<br/> |
| Biblioteca<br/>                  | <dl> <dt>Dwrite. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDWriteTextLayout2**](idwritetextlayout2.md)
</dt> </dl>

 

 





