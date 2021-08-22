---
title: Interface IDWriteFont2
description: Representa uma fonte física em uma coleção de fontes.
ms.assetid: 4E3069AE-5882-4A26-A36D-BE7D7EE1B0C3
keywords:
- Gravação direta da interface IDWriteFont2
- Gravação direta da interface IDWriteFont2, descrita
topic_type:
- apiref
api_name:
- IDWriteFont2
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fea5956c14a203020106fe6ecafdffb1522810d8f56684bbeafd158045444e34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071680"
---
# <a name="idwritefont2-interface"></a>Interface IDWriteFont2

Representa uma fonte física em uma coleção de fontes.

Essa interface adiciona a capacidade de verificar se um caminho de renderização de cor é potencialmente necessário.

## <a name="members"></a>Membros

A interface **IDWriteFont2** herda de [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1). **IDWriteFont2** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IDWriteFont2** tem esses métodos.



| Método                                          | Descrição                                                                        |
|:------------------------------------------------|:-----------------------------------------------------------------------------------|
| [**IsColorFont**](idwritefont2-iscolorfont.md) | Permite determinar se um caminho de renderização de cor é potencialmente necessário.<br/> |



 

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

[**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1)
</dt> </dl>

 

