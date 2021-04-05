---
description: Especifica o número de aprovações de codificação que o codificador suporta.
ms.assetid: 8b476164-fd44-4277-89bd-ba9929bf93a2
title: Propriedade AVEncCommonMultipassMode (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4302cf0a9524f16dee8e7b84060065a4c750e4e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825956"
---
# <a name="avenccommonmultipassmode-property"></a>Propriedade AVEncCommonMultipassMode

Especifica o número de aprovações de codificação que o codificador suporta.

Esta propriedade é somente para leitura.

## <a name="data-type"></a>Tipo de dados

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncCommonMultipassMode**

## <a name="property-value"></a>Valor da propriedade

Essa propriedade é retornada como um intervalo de valores. Para obter o intervalo com suporte, chame [**ICodecAPI:: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).

## <a name="remarks"></a>Comentários

A decodificação da latência é definida como a quantidade de dados que o decodificador deve armazenar em buffer. Por exemplo, definir essa propriedade como **Variant \_ true** em um codificador de vídeo MPEG limita os tipos de estruturas GOP que o codificador pode usar.

Para definir a passagem de codificação atual, defina a propriedade [**AVEncCommonPassStart**](avenccommonpassstart-property.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]<br/>                     |
| Servidor mínimo com suporte<br/> | Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]<br/>                           |
| parâmetro<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades da API do codec](codec-api-properties.md)
</dt> <dt>

[**Interface ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




