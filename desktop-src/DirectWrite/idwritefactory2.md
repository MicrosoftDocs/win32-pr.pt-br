---
title: Interface IDWriteFactory2
description: a interface de fábrica raiz para todos os objetos de DirectWrite.
ms.assetid: 1D3EEC28-EAB3-4FA2-98E9-7A8FDAF6E6FE
keywords:
- Gravação direta da interface IDWriteFactory1
- Gravação direta da interface IDWriteFactory1, descrita
topic_type:
- apiref
api_name:
- IDWriteFactory1
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 370292387f2c42e3f749e24a063e05bb24280ec5c8e8941a430f996fe7f349da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902796"
---
# <a name="idwritefactory2-interface"></a>Interface IDWriteFactory2

a interface de fábrica raiz para todos os objetos de [DirectWrite](direct-write-portal.md) .

## <a name="members"></a>Membros

A interface **IDWriteFactory1** herda de [**IDWriteFactory1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1). **IDWriteFactory2** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IDWriteFactory1** tem esses métodos.



| Método                                                                             | Descrição                                                                                                |
|:-----------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**CreateCustomRenderingParams**](idwritefactory2-createcustomrenderingparams.md) | Cria um objeto de parâmetros de renderização com as propriedades especificadas.<br/>                            |
| [**CreateFontFallbackBuilder**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefactory2-createfontfallbackbuilder)     | Cria um objeto do construtor de fallback de fonte.<br/>                                                         |
| [**CreateGlyphRunAnalysis**](idwritefactory2-createglyphrunanalysis.md)           | Cria um objeto de análise de execução de glifos, que encapsula informações usadas para renderizar uma execução de glifo.<br/> |
| [**GetSystemFontFallback**](idwritefactory2-getsystemfontfallback.md)             | Cria um objeto de fallback de fonte da lista de fallback de fontes do sistema.<br/>                              |
| [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefactory2-translatecolorglyphrun)           | Esse método é chamado em uma execução de glifo para convertê-lo em várias execuções de glifos de cores.<br/>           |



 

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

[**IDWriteFactory1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1)
</dt> <dt>

[**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory)
</dt> </dl>

 

