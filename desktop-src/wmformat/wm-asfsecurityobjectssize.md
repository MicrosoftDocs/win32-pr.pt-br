---
title: WM/ASFSecurityObjectsSize
description: O atributo WM/ASFSecurityObjectsSize contém o tamanho, em bytes, dos objetos relacionados ao DRM no header do arquivo ASF.
ms.assetid: 40ea619a-1042-4d1b-a855-d80c93202765
keywords:
- WM/ASFSecurityObjectsSize formato de mídia do Windows
topic_type:
- apiref
api_name:
- WM/ASFSecurityObjectsSize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 309261b7c8ad0c91a50fa1e0f292c6785d18cdd222c5e463eb62ae3728b39b93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119584586"
---
# <a name="wmasfsecurityobjectssize"></a>WM/ASFSecurityObjectsSize

O **atributo WM/ASFSecurityObjectsSize** contém o tamanho, em bytes, dos objetos relacionados ao DRM no header do arquivo ASF.

## <a name="global-constant"></a>Constante global

g \_ wszWMASFSecurityObjectsSize

## <a name="data-type"></a>Tipo de Dados

**QWORD \_ DO \_ TIPO WMT**

## <a name="remarks"></a>Comentários

Esse atributo é somente leitura e se aplica a todo o arquivo (fluxo 0).

Você só pode recuperar esse atributo usando os métodos da interface [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) do objeto do editor de metadados.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> </dl>

 

 




