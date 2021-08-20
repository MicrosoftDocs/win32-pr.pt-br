---
title: Métodos IDWriteFontSet GetPropertyValues (Dwrite \_ 3.h)
description: Retorna valores de propriedade para o conjunto de fontes.
ms.assetid: 3c3fd5b7-88dd-d434-0b62-f365b407c379
keywords:
- Métodos GetPropertyValues Direct Write
topic_type:
- apiref
api_location:
- dwrite_3.h
api_type:
- HeaderDef
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: cffc669d71bf7f78087fe3c105c182ca86b4ebf5a689bcdb6c2807dfae3c0f21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117816357"
---
# <a name="idwritefontsetgetpropertyvalues-methods"></a>Métodos IDWriteFontSet::GetPropertyValues

Retorna valores de propriedade para o conjunto de fontes.

### <a name="overload-list"></a>Lista de sobrecargas



| Método                                                                                                                                   | Descrição                                                                                                                                                                                                                                                                                                   |
|:-----------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetPropertyValues(DWRITE \_ FONT \_ PROPERTY \_ ID, IDWriteStringList \* \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist))                       | Retorna todos os valores de propriedade exclusivos no conjunto, que podem ser usados para fins como exibir uma lista de família ou uma nuvem de marcação. Todos os valores são retornados independentemente do idioma, incluindo todos os nomes localizados. <br/>                                                                                       |
| [**GetPropertyValues(DWRITE \_ FONT \_ PROPERTY \_ ID, const WCHAR \* , IDWriteStringList \* \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_wcharconst_idwritestringlist))        | Retorna todos os valores de propriedade exclusivos no conjunto, que podem ser usados para fins como exibir uma lista de família ou uma nuvem de marcação. Os valores são retornados em ordem de prioridade de acordo com a lista de idiomas, de modo que, se uma fonte contiver mais de um nome localizado, o preferencial será retornado. <br/> |
| [**GetPropertyValues(UINT32, DWRITE \_ FONT \_ PROPERTY \_ ID, \* BOOL, IDWriteLocalizedStrings \* \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist)) | Retorna os valores de propriedade de um índice de item de fonte específico.<br/>                                                                                                                                                                                                                                         |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Dwrite \_ 3.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDWriteFontSet**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset)
</dt> </dl>

�

�
