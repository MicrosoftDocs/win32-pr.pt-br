---
description: Especifica se o codec deve usar a filtragem mediana durante a codificação.
ms.assetid: adfca033-4679-4f36-a802-6dd5df7100c8
title: Propriedade MFPKEY_FORCEMEDIANSETTING (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38d0aa154798e2ed42a7373a6e85a4b46f8eeb7b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103837657"
---
# <a name="mfpkey_forcemediansetting-property"></a>\_Propriedade MFPKEY FORCEMEDIANSETTING

Especifica se o codec deve usar a filtragem mediana durante a codificação.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCForceMedianSetting

## <a name="data-type"></a>Tipo de Dados

BOOL do VT \_

## <a name="default-value"></a>Valor padrão

FALSE

## <a name="remarks"></a>Comentários

A filtragem mediana informa o codec para ignorar o ruído e a granulação ao calcular o movimento entre os quadros. Isso pode melhorar a qualidade de vídeo muito ruidosa, mas pode levar a trilhas de movimento (também conhecidas como artefatos à direita) quando aplicado a um vídeo de origem limpo.

Por padrão, o codec usa a lógica interna para determinar se a filtragem mediana deve ser usada. Se você definir essa propriedade, essa lógica será substituída.

> [!Note]  
> Esse filtro não é o mesmo que os filtros de desfoque medianos encontrados em muitos aplicativos de processamento de vídeo e pós-processamento.

 

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

 

 




