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
ms.openlocfilehash: e41831610f3ef564db55241267b75820cb9d87af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644834"
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
| Cliente mínimo com suporte<br/> | Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]<br/>                          |
| Número mínimo de telefone com suporte<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]<br/> |
| Biblioteca<br/>                  | <dl> <dt>Dwrite. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



 

