---
title: Métodos getvalordapropriedades IDWriteFontSet (Dwrite \_ 3. h)
description: Retorna valores de propriedade para o conjunto de fontes.
ms.assetid: 3c3fd5b7-88dd-d434-0b62-f365b407c379
keywords:
- Métodos getvalordapropriedades Direct Write
topic_type:
- apiref
api_location:
- dwrite_3.h
api_type:
- HeaderDef
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 3d135a63be987a4999d898c8e9c7d84251c8ece3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755129"
---
# <a name="idwritefontsetgetpropertyvalues-methods"></a>Métodos IDWriteFontSet:: getvalordapropriedades

Retorna valores de propriedade para o conjunto de fontes.

### <a name="overload-list"></a>Lista de sobrecargas



| Método                                                                                                                                   | Descrição                                                                                                                                                                                                                                                                                                   |
|:-----------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Getvalordapropriedades ( \_ ID da propriedade da fonte DWRITE \_ \_ , IDWriteStringList \* \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist))                       | Retorna todos os valores de propriedade exclusivos no conjunto, que pode ser usado para fins como exibir uma lista de família ou uma nuvem de marca. Todos os valores são retornados independentemente do idioma, incluindo todos os nomes localizados. <br/>                                                                                       |
| [**Getvalordapropriedades ( \_ ID da propriedade da fonte DWRITE \_ \_ , const WCHAR \* , IDWriteStringList \* \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_wcharconst_idwritestringlist))        | Retorna todos os valores de propriedade exclusivos no conjunto, que pode ser usado para fins como exibir uma lista de família ou uma nuvem de marca. Os valores são retornados em ordem de prioridade de acordo com a lista de idiomas, de modo que, se uma fonte contiver mais de um nome localizado, o preferencial será retornado. <br/> |
| [**Getvalordapropriedades (UINT32, \_ ID de \_ propriedade de fonte DWRITE \_ , bool \* , IDWriteLocalizedStrings \* \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist)) | Retorna os valores de propriedade de um índice de item de fonte específico.<br/>                                                                                                                                                                                                                                         |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Dwrite \_ 3. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDWriteFontSet**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset)
</dt> </dl>

�

�
