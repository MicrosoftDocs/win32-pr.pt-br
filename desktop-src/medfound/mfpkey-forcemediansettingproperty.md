---
description: Especifica se o codec deve usar a filtragem mediana durante a codificação.
ms.assetid: adfca033-4679-4f36-a802-6dd5df7100c8
title: Propriedade MFPKEY_FORCEMEDIANSETTING (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 722fca2f73f2114cf17664f228e00a12f46e5a399f54b8dc6990940f5c18d979
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953946"
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
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




