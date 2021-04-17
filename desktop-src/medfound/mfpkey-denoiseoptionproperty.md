---
description: Especifica se o codec usará o filtro de ruído durante a codificação.
ms.assetid: 9e099378-bb77-4dca-9171-7fe58e0139de
title: Propriedade MFPKEY_DENOISEOPTION (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7f318e294f69095758fe300fce19043c23cf376
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105747866"
---
# <a name="mfpkey_denoiseoption-property"></a>\_Propriedade MFPKEY DENOISEOPTION

Especifica se o codec usará o filtro de ruído durante a codificação.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCDenoiseOption

## <a name="data-type"></a>Tipo de Dados

BOOL do VT \_

## <a name="default-value"></a>Valor padrão

FALSE

## <a name="remarks"></a>Comentários

O filtro de ruído pode melhorar a qualidade de fontes de vídeo ruidosas, como filme que contém muitos refinamentos ou capturas de vídeo em baixa luz. Esse filtro pode ser usado em cenários de codificação ativa em que o pré-processamento externo não é uma opção.

Esse filtro deve ser desabilitado para fontes de vídeo limpas, pois ele pode reduzir a qualidade da imagem quando a qualidade é boa para começar.

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

 

 




