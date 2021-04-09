---
description: Especifica se o codificador executa o telecineon inverso.
ms.assetid: 3467b0c8-c27d-448a-8cbf-971307e4c408
title: Propriedade AVEncVideoInverseTelecineEnable (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31eac80651eb80d933c4f40ef22303c4858783d2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087764"
---
# <a name="avencvideoinversetelecineenable-property"></a>Propriedade AVEncVideoInverseTelecineEnable

Especifica se o codificador executa o telecineon inverso.

Esta propriedade é de leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**Variante \_ BOOL** (**VT \_ bool**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncVideoInverseTelecineEnable**

## <a name="remarks"></a>Comentários

Se o valor for **Variant \_ true**, o codificador executará o telecineon inverso. Se o telecineon inverso não for necessário, defina essa propriedade como **Variant \_ false**. Para executar o telecineon inverso fora do codificador, defina essa propriedade como **Variant \_ false** e defina a propriedade [**AVEncVideoOutputScanType**](avencvideooutputscantype-property.md) como eAVEncVideoOutputScan \_ SameAsInput.

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

 

 




