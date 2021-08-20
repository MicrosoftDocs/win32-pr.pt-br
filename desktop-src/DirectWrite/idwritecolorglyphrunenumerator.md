---
title: Interface IDWriteColorGlyphRunEnumerator
description: Essa interface permite que o aplicativo enumere por meio das execuções de glifos de cores.
ms.assetid: 649AD648-32BB-4BF4-A82F-075E93505E33
keywords:
- Gravação direta da interface IDWriteColorGlyphRunEnumerator
- Gravação direta da interface IDWriteColorGlyphRunEnumerator, descrita
topic_type:
- apiref
api_name:
- IDWriteColorGlyphRunEnumerator
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fa665f7000ffaada5bc14f97671fb6e52266c712ef6081b956184653d1f1c95
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119536136"
---
# <a name="idwritecolorglyphrunenumerator-interface"></a>Interface IDWriteColorGlyphRunEnumerator

Essa interface permite que o aplicativo enumere por meio das execuções de glifos de cores. O enumerador enumera as camadas de volta ao front Order para a disposição em camadas apropriada.

## <a name="members"></a>Membros

A interface **IDWriteColorGlyphRunEnumerator** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IDWriteColorGlyphRunEnumerator** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IDWriteColorGlyphRunEnumerator** tem esses métodos.



| Método                                                                | Descrição                                                 |
|:----------------------------------------------------------------------|:------------------------------------------------------------|
| [**GetCurrentRun**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritecolorglyphrunenumerator-getcurrentrun) | Retorna a execução de glifo atual do enumerador.<br/> |
| [**MoveNext**](idwritecolorglyphrunenumerator-movenext.md)           | Mover para a próxima execução de glifo no enumerador.<br/>    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ aplicativos UWP de aplicativos de desktop \|\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[Aplicativos de aplicativos UWP da área de trabalho R2 \|\]<br/>                          |
| Número mínimo de telefone com suporte<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]<br/> |
| Biblioteca<br/>                  | <dl> <dt>Dwrite. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



 

