---
title: Interface IDWriteFontFallbackBuilder
description: Permite que você crie mapeamentos de fallback de fonte Unicode e crie um objeto de retorno de fonte a partir desses mapeamentos.
ms.assetid: 462AC12E-C856-4D8F-83AF-FAC3221425C2
keywords:
- Gravação direta da interface IDWriteFontFallbackBuilder
- Gravação direta da interface IDWriteFontFallbackBuilder, descrita
topic_type:
- apiref
api_name:
- IDWriteFontFallbackBuilder
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38cd1770bdd9617f53bb48d725b55c466b12c263
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918685"
---
# <a name="idwritefontfallbackbuilder-interface"></a>Interface IDWriteFontFallbackBuilder

Permite que você crie mapeamentos de fallback de fonte Unicode e crie um objeto de retorno de fonte a partir desses mapeamentos.

## <a name="members"></a>Membros

A interface **IDWriteFontFallbackBuilder** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IDWriteFontFallbackBuilder** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IDWriteFontFallbackBuilder** tem esses métodos.



| Método                                                                      | Descrição                                                                                  |
|:----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**AddMapping**](idwritefontfallbackbuilder-addmapping.md)                 | Anexa um único mapeamento à lista. Chame isso uma vez para cada mapeamento adicional.<br/> |
| [**Addmapeamentos**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefontfallbackbuilder-addmappings)               | Adicione todos os mapeamentos de um objeto de fallback de fonte existente.<br/>                       |
| [**CreateFontFallback**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefontfallbackbuilder-createfontfallback) | Cria o objeto de fallback finalizado dos mapeamentos adicionados.<br/>                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]<br/>                          |
| Número mínimo de telefone com suporte<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]<br/> |
| Biblioteca<br/>                  | <dl> <dt>Dwrite. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



 

