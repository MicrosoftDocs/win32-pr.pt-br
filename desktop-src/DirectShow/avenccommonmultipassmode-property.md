---
description: Especifica o número de passagens de codificação compatíveis com o codificador.
ms.assetid: 8b476164-fd44-4277-89bd-ba9929bf93a2
title: Propriedade AVEncCommonMultipassMode (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6fb909e58dbdfd5d1431d0101365db78efa83fd68e9299b8578f19770787fb7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118159791"
---
# <a name="avenccommonmultipassmode-property"></a>Propriedade AVEncCommonMultipassMode

Especifica o número de passagens de codificação compatíveis com o codificador.

Esta propriedade é somente para leitura.

## <a name="data-type"></a>Tipo de dados

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncCommonMultipassMode**

## <a name="property-value"></a>Valor da propriedade

Essa propriedade é retornada como um intervalo de valores. Para obter o intervalo com suporte, chame [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).

## <a name="remarks"></a>Comentários

A latência de decodificação é definida como a quantidade de dados que o decodificador deve ter em buffer. Por exemplo, definir essa propriedade como **VARIANT \_ TRUE** em um codificador de vídeo MPEG limita os tipos de estruturas GOP que o codificador pode usar.

Para definir a passagem de codificação atual, de definir a [**propriedade AVEncCommonPassStart.**](avenccommonpassstart-property.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional aplicativos \[ UWP da área de \| trabalho\]<br/>                     |
| Servidor mínimo com suporte<br/> | Windows aplicativos da área de trabalho do servidor 2000 \[ \| aplicativos UWP\]<br/>                           |
| Cabeçalho<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades da API do Codec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI Interface**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




