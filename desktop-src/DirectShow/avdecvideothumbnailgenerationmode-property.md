---
description: Habilita ou desabilita o modo de geração de miniatura em um decodificador de vídeo.
ms.assetid: c640d915-585b-481d-aa49-0d4a559d291c
title: Propriedade AVDecVideoThumbnailGenerationMode (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5aa2a9c8b095c0fdb0d44a5a12fdfe954b89ba49
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103920054"
---
# <a name="avdecvideothumbnailgenerationmode-property"></a>Propriedade AVDecVideoThumbnailGenerationMode

Habilita ou desabilita o modo de geração de miniatura em um decodificador de vídeo.

Esta propriedade é de leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**Variante \_ BOOL** (**VT \_ bool**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVDecVideoThumbnailGenerationMode**

## <a name="remarks"></a>Comentários

Se o valor for **Variant \_ true**, o decodificador usará uma configuração otimizada para gerar imagens em miniatura rapidamente. (Por exemplo, ele pode ignorar os quadros B ou P.) Caso contrário, se o valor for **Variant \_ false**, o decodificador usará suas configurações de decodificação normais.

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

 

 




