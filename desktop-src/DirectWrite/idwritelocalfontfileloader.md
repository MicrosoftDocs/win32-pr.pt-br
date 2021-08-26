---
title: Interface IDWriteLocalFontFileLoader
description: Uma implementação interna da interface IDWriteFontFileLoader, que opera em arquivos de fonte locais e expõe informações de arquivo de fonte local da chave de referência do arquivo de fonte.
ms.assetid: acb777c8-24c6-452e-8f58-8fb2ad8c0b6c
keywords:
- Gravação direta da interface IDWriteLocalFontFileLoader
- Gravação direta da interface IDWriteLocalFontFileLoader, descrita
topic_type:
- apiref
api_name:
- IDWriteLocalFontFileLoader
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa073b0d39e5dfbcdb90f2cd67db5f09a04e21c3e36790d4d841e5719490c753
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048686"
---
# <a name="idwritelocalfontfileloader-interface"></a>Interface IDWriteLocalFontFileLoader

Uma implementação interna da interface [**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) , que opera em arquivos de fonte locais e expõe informações de arquivo de fonte local da chave de referência do arquivo de fonte. Referências de arquivo de fonte criadas usando [**CreateFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createfontfilereference) usam este carregador de arquivo de fonte.

## <a name="members"></a>Membros

A interface **IDWriteLocalFontFileLoader** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IDWriteLocalFontFileLoader** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IDWriteLocalFontFileLoader** tem esses métodos.



| Método                                                                                  | Descrição                                                                               |
|:----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [**GetFilePathFromKey**](idwritelocalfontfileloader-getfilepathfromkey.md)             | Obtém o caminho do arquivo de fonte absoluto da chave de referência do arquivo de fonte.<br/>          |
| [**GetFilePathLengthFromKey**](idwritelocalfontfileloader-getfilepathlengthfromkey.md) | Obtém o comprimento do caminho de arquivo absoluto da chave de referência do arquivo de fonte.<br/> |
| [**GetLastWriteTimeFromKey**](idwritelocalfontfileloader-getlastwritetimefromkey.md)   | Obtém a hora da última gravação do arquivo da chave de referência do arquivo de fonte.<br/>      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>Dwrite. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



 

