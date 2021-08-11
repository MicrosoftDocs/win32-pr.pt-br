---
description: Contém o CLSID (identificador de classe) de uma transformação Media Foundation (MFT).
ms.assetid: 99ee6f50-1de7-41ea-be5b-135730138d5d
title: MFT_TRANSFORM_CLSID_Attribute atributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0122b783d8b321aa2a5c7788a589e19625b6a2bde8e37b0b659b0a1192f8c7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118240194"
---
# <a name="mft_transform_clsid_attribute-attribute"></a>Atributo \_ \_ CLSID MFT TRANSFORM \_

Contém o CLSID (identificador de classe) de uma transformação Media Foundation (MFT).

## <a name="data-type"></a>Tipo de dados

**GUID**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes::GetGUID.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)

Para definir esse atributo, chame [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).

## <a name="remarks"></a>Comentários

Esse atributo é definido nos ponteiros [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) retornados pela [**função MFTEnumEx.**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)

Esse atributo é usado internamente pelo objeto de ativação quando cria o MFT. Os aplicativos não devem usar essa CLSID diretamente para criar o MFT, porque o objeto de ativação pode precisar inicializar o MFT. Portanto, para criar uma instância do MFT, chame [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) no objeto de ativação.

Observe que a [**função MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) se comporta de maneira diferente da [**função MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) nesse sentido. A **função MFTEnum** retorna CLSIDs, que o aplicativo passa para a **função CoCreateInstance.** A **função MFTEnumEx** retorna objetos de ativação em vez de CLSIDs.

A constante GUID para esse atributo é exportada de mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows aplicativos UWP de 7 \[ \| áreas de trabalho\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Aplicativos \[ UWP de aplicativos da área de trabalho do Server 2008 R2 \|\]<br/>                           |
| parâmetro<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Veja também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Transformar atributos](transform-attributes.md)
</dt> </dl>

 

 




