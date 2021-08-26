---
description: Especifica a compensação entre o movimento e as imagens ainda. Essa propriedade aplica-se somente ao modo de controle de taxa de bits constante (CBR).
ms.assetid: e657e971-4624-4c87-ad51-6bf0cd1f9246
title: Propriedade AVEncVideoCBRMotionTradeoff (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21d3db1f310de6468b57d469fbf699919ab86429e7242344622ca498b9e59f39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057936"
---
# <a name="avencvideocbrmotiontradeoff-property"></a>Propriedade AVEncVideoCBRMotionTradeoff

Especifica a compensação entre o movimento e as imagens ainda. Essa propriedade aplica-se somente ao modo de controle de taxa de bits constante (CBR).

Esta propriedade é de leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncVideoCBRMotionTradeoff**

## <a name="property-value"></a>Valor da propriedade

O valor dessa propriedade tem o seguinte intervalo.



| Valor | Descrição               |
|-------|---------------------------|
| 0     | Otimizar para imagens ainda |
| 100   | Otimizar para movimento.      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | aplicativos Windows 2000 Professional \[ desktop aplicativos \| UWP\]<br/>                     |
| Servidor mínimo com suporte<br/> | Windows \[ aplicativos da área de trabalho do servidor 2000 \| aplicativo UWP\]<br/>                           |
| Cabeçalho<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades da API do codec](codec-api-properties.md)
</dt> <dt>

[**Interface ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




