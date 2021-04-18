---
title: WM/MCDI
description: O atributo WM/MCDI contém o identificador de CD de música. Este é um despejo binário do Sumário do CD que é usado para identificar exclusivamente o CD.
ms.assetid: cb16c62b-b9e0-4676-b1bb-ff26a2e09cb7
keywords:
- Formato de mídia do Windows do WM/MCDI
topic_type:
- apiref
api_name:
- WM/MCDI
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2da5c629bcef9ca2072d0ddda433fde97932e97e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105785249"
---
# <a name="wmmcdi"></a>WM/MCDI

O atributo **WM/MCDI** contém o identificador de CD de música. Este é um despejo binário do Sumário do CD que é usado para identificar exclusivamente o CD.

## <a name="global-constant"></a>Constante global

g \_ wszWMMCDI

## <a name="data-type"></a>Tipo de Dados

**WMT \_ tipo \_ binário**

## <a name="remarks"></a>Comentários

Esse atributo é compatível com o quadro ID3, MCDI. A especificação ID3 para o quadro MCDI requer que apenas um desses quadros exista por arquivo e que exista um quadro TRCK válido. O editor de metadados não executa nenhuma validação para essas regras. Além disso, o tamanho do WM/MCDI não está limitado a 804 bytes, assim como o quadro ID3 MCDI.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> </dl>

 

 




