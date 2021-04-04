---
title: WM/ASFSecurityObjectsSize
description: O atributo WM/ASFSecurityObjectsSize contém o tamanho, em bytes, dos objetos relacionados ao DRM no cabeçalho do arquivo ASF.
ms.assetid: 40ea619a-1042-4d1b-a855-d80c93202765
keywords:
- Formato de mídia do Windows do WM/ASFSecurityObjectsSize
topic_type:
- apiref
api_name:
- WM/ASFSecurityObjectsSize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de28f2169e5ac854163854ac95959d941100aaae
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007090"
---
# <a name="wmasfsecurityobjectssize"></a>WM/ASFSecurityObjectsSize

O atributo **WM/ASFSecurityObjectsSize** contém o tamanho, em bytes, dos objetos relacionados ao DRM no cabeçalho do arquivo asf.

## <a name="global-constant"></a>Constante global

g \_ wszWMASFSecurityObjectsSize

## <a name="data-type"></a>Tipo de Dados

**WMT \_ tipo \_ QWORD**

## <a name="remarks"></a>Comentários

Esse atributo é somente leitura e se aplica a todo o arquivo (fluxo 0).

Você só pode recuperar esse atributo usando os métodos da interface [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) do objeto editor de metadados.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> </dl>

 

 




