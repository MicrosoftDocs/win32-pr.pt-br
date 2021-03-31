---
description: Contém o identificador de classe (CLSID) de uma Media Foundation de transformação (MFT).
ms.assetid: 99ee6f50-1de7-41ea-be5b-135730138d5d
title: Atributo MFT_TRANSFORM_CLSID_Attribute (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b5ca1aa6a9d7691200761509e1a5e407a6c7db6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921218"
---
# <a name="mft_transform_clsid_attribute-attribute"></a>\_Atributo de \_ atributo CLSID de transformação de MFT \_

Contém o identificador de classe (CLSID) de uma Media Foundation de transformação (MFT).

## <a name="data-type"></a>Tipo de dados

**GUID**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).

Para definir esse atributo, chame [**IMFAttributes:: SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).

## <a name="remarks"></a>Comentários

Esse atributo é definido nos ponteiros do [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) retornados pela função [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .

Esse atributo é usado internamente pelo objeto de ativação quando cria o MFT. Os aplicativos não devem usar esse CLSID diretamente para criar o MFT, pois o objeto de ativação pode precisar inicializar o MFT. Portanto, para criar uma instância do MFT, chame [**IMFActivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) no objeto Activation.

Observe que a função [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) se comporta de maneira diferente da função [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) nesse sentido. A função **MFTEnum** retorna CLSIDs, que o aplicativo passa para a função **CoCreateInstance** . A função **MFTEnumEx** retorna objetos de ativação em vez de CLSIDs.

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]<br/>                           |
| parâmetro<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de transformação](transform-attributes.md)
</dt> </dl>

 

 




