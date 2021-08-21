---
title: Media.error
description: A propriedade error recuperará um objeto ErrorItem se o item de mídia tiver uma condição de erro.
ms.assetid: cd572688-12f9-4615-8f22-9442d615a2b6
keywords:
- Media.error Windows Media Player
topic_type:
- apiref
api_name:
- Media.error
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 709e6318e125d515eb06d86147cb71f6a2601caf526b43416e5493c8aaef044d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118837159"
---
# <a name="mediaerror"></a>Media.error

A **propriedade** error recuperará um **objeto ErrorItem** se o item de mídia tiver uma condição de erro.

## <a name="syntax"></a>Syntax

*player*. *currentMedia*. **erro**

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é um objeto **ErrorItem somente** leitura.

## <a name="remarks"></a>Comentários

Se o item de mídia não puder ser tocado, essa propriedade recuperará um **objeto ErrorItem** que contém informações sobre o problema encontrado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player para Windows XP ou posterior.<br/>                           |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto ErrorItem**](erroritem-object.md)
</dt> <dt>

[**Objeto de mídia**](media-object.md)
</dt> </dl>

 

 





