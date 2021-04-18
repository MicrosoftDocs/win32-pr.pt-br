---
title: Mídia. erro
description: A Propriedade Error recupera um objeto ErrorItem se o item de mídia tiver uma condição de erro.
ms.assetid: cd572688-12f9-4615-8f22-9442d615a2b6
keywords:
- Media. erro no Windows Media Player
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
ms.openlocfilehash: 5845252c817a424b0cbe414612fde47ed8b57328
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752217"
---
# <a name="mediaerror"></a>Mídia. erro

A propriedade **Error** recupera um objeto **ErrorItem** se o item de mídia tiver uma condição de erro.

## <a name="syntax"></a>Syntax

*Player*. *currentMedia*. **erro** do

## <a name="possible-values"></a>Valores possíveis

Esta propriedade é um objeto **ErrorItem** somente leitura.

## <a name="remarks"></a>Comentários

Se o item de mídia não puder ser reproduzido, essa propriedade recuperará um objeto **ErrorItem** que contém informações sobre o problema encontrado.

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

 

 





