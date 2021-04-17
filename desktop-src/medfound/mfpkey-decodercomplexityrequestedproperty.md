---
description: Especifica o modelo de conformidade do dispositivo que você deseja usar para a codificação de vídeo.
ms.assetid: cd2c068a-dbbc-42c5-bc92-bbb73f0259d1
title: Propriedade MFPKEY_DECODERCOMPLEXITYREQUESTED (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e017361d7e8267d33ecb2cfdbce2a6e79758fac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105790470"
---
# <a name="mfpkey_decodercomplexityrequested-property"></a>\_Propriedade MFPKEY DECODERCOMPLEXITYREQUESTED

Especifica o modelo de conformidade do dispositivo que você deseja usar para a codificação de vídeo.

## <a name="data-type"></a>Tipo de Dados

\_I4 VT

## <a name="default-value"></a>Valor padrão

1

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCDecoderComplexityRequested

## <a name="data-type-for-ipropertybag"></a>Tipo de dados para IPropertyBag

VT \_ BSTR

## <a name="default-value-for-ipropertybag"></a>Valor padrão para IPropertyBag

MP

## <a name="remarks"></a>Comentários

O codec tentará codificar o conteúdo usando o modelo de conformidade do dispositivo especificado por esse valor. O modelo real para o qual o conteúdo codificado está em conformidade pode ser recuperado da propriedade [MFPKEY \_ DECODERCOMPLEXITYPROFILE](mfpkey-decodercomplexityprofileproperty.md) após a codificação.

Essa propriedade deve ser um dos valores a seguir.



| Valor para IPropertyStore | Valor para IPropertyBag | Descrição         |
|--------------------------|------------------------|---------------------|
| 0                        | SP3                   | Perfil simples      |
| 1                        | MP                   | Perfil principal        |
| 2                        | CP                   | Não tem mais suporte |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                    |
| parâmetro<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




