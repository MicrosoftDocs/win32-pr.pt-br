---
title: Is_Protected
description: O \_ atributo is Protected é um atributo de nível de arquivo que especifica se o conteúdo no arquivo foi protegido usando o DRM (gerenciamento de direitos digitais).
ms.assetid: 6fe63d9b-67ec-47a8-ba20-657434c7a15b
keywords:
- Is_Protected o formato Windows Media
topic_type:
- apiref
api_name:
- Is_Protected
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85ec24eb3e805f93bfd46e40954ce64da73ed774
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "105762485"
---
# <a name="is_protected"></a>É \_ protegido

O atributo **is \_ Protected** é um atributo de nível de arquivo que especifica se o conteúdo no arquivo foi protegido usando o DRM (gerenciamento de direitos digitais).

## <a name="global-constant"></a>Constante global

g \_ wszWMProtected

## <a name="data-type"></a>Tipo de Dados

**WMT \_ tipo \_ bool**

## <a name="remarks"></a>Comentários

Este é um atributo codificado. A recuperação dessa propriedade fornece as mesmas informações que chamam [**WMIsContentProtected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmiscontentprotected).

Este atributo não pode ser duplicado no nível do arquivo. Se esse atributo for usado para um fluxo individual, ele será tratado como metadados personalizados e não transmitirá seu significado normal para os objetos do SDK do Windows Media Format.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> </dl>

 

 




