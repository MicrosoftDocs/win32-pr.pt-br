---
description: Especifica se um exemplo de mídia é o primeiro exemplo após uma lacuna no fluxo.
ms.assetid: f9e1e700-9958-404d-8b83-08f846f5a1b0
title: MFSampleExtension_Discontinuity atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ac76b8e4d220ece7c34277bfac031213c1c042615d7ca48677839e54b77e5da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118241076"
---
# <a name="mfsampleextension_discontinuity-attribute"></a>Atributo MFSampleExtension \_ Discontinuity

Especifica se um exemplo de mídia é o primeiro exemplo após uma lacuna no fluxo.

## <a name="data-type"></a>Tipo de dados

**BOOL** armazenado como **UINT32**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Aplica-se a

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Comentários

Esse atributo se aplica a exemplos de mídia. Se esse atributo for **TRUE,** isso significa que houve uma descontinuidade no fluxo e esse exemplo é o primeiro a aparecer após a lacuna.

Se esse atributo não estiver definido, o valor padrão será **FALSE.**

A constante GUID para esse atributo é exportada de mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Aplicativos \| UWP de aplicativos da área de trabalho do Vista\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows Aplicativos \[ UWP de aplicativos da área de trabalho do Server 2008 \|\]<br/>                        |
| parâmetro<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Veja também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de exemplo](sample-attributes.md)
</dt> <dt>

[Exemplos de mídia](media-samples.md)
</dt> </dl>

 

 




