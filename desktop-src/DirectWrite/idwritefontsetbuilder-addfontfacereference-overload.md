---
title: Métodos IDWriteFontSetBuilder AddFontFaceReference (Dwrite \_ 3. h)
description: Adiciona uma referência a uma fonte para o conjunto que está sendo compilado.
ms.assetid: 2543720f-1b5a-ca1d-9e24-3fcd61a4de37
keywords:
- Gravação direta de métodos AddFontFaceReference
topic_type:
- apiref
api_location:
- dwrite_3.h
api_type:
- HeaderDef
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: c9edfed7680b18ef9ffb271cb59de3a54d4b408ac5f194a7bead1bbb3fb9b2ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075576"
---
# <a name="idwritefontsetbuilderaddfontfacereference-methods"></a>Métodos IDWriteFontSetBuilder:: AddFontFaceReference

Adiciona uma referência a uma fonte para o conjunto que está sendo compilado.

### <a name="overload-list"></a>Lista de sobrecargas



| Método                                                                                                                                           | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|:-------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddFontFaceReference (IDWriteFontFaceReference \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference))                                         | Adiciona uma referência a uma fonte para o conjunto que está sendo compilado. Os metadados necessários serão extraídos automaticamente da fonte ao chamar createfontset.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**AddFontFaceReference (IDWriteFontFaceReference \* , const DWRITE \_ propriedade da fonte \_ \* , UINT32)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference_dwrite_font_propertyconst_uint32)) | Adiciona uma referência a uma fonte para o conjunto que está sendo compilado. O chamador fornece informações suficientes para pesquisar, evitando a necessidade de abrir a fonte potencialmente não local. Todas as propriedades não fornecidas pelo chamador estarão ausentes e essas propriedades não estarão disponíveis como filtros em GetMatchingFonts. Getvalordapropriedades para propriedades ausentes retornará uma lista de cadeias de caracteres vazia. As propriedades passadas devem geralmente ser consistentes com o conteúdo da fonte real, mas não precisam ser. Você poderia, por exemplo, alias de uma fonte usando um nome diferente ou identificador exclusivo, ou pode definir marcas personalizadas que não estão presentes na fonte real.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Dwrite \_ 3. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDWriteFontSetBuilder**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder)
</dt> </dl>

�

�
