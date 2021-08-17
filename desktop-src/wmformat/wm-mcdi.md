---
title: WM/MCDI
description: O atributo WM/MCDI contém o identificador de CD de música. Esse é um despejo binário do conteúdo do CD usado para identificar exclusivamente o CD.
ms.assetid: cb16c62b-b9e0-4676-b1bb-ff26a2e09cb7
keywords:
- Formato de mídia do Windows WM/MCDI
topic_type:
- apiref
api_name:
- WM/MCDI
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bccf4a081141c1902fe93680937a3196e015e6690acf76d69f3a3d8a016c092e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963745"
---
# <a name="wmmcdi"></a>WM/MCDI

O **atributo WM/MCDI** contém o identificador de CD de música. Esse é um despejo binário do conteúdo do CD usado para identificar exclusivamente o CD.

## <a name="global-constant"></a>Constante global

g \_ wszWMMCDI

## <a name="data-type"></a>Tipo de Dados

**TIPO WMT \_ \_ BINARY**

## <a name="remarks"></a>Comentários

Esse atributo é compatível com o quadro ID3, MCDI. A especificação ID3 para o quadro MCDI requer que apenas um quadro desse tipo exista por arquivo e que exista um quadro TRCK válido. O editor de metadados não executa nenhuma validação para essas regras. Além disso, o tamanho do WM/MCDI não é limitado a 804 bytes, assim como o quadro MCDI ID3.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> </dl>

 

 




