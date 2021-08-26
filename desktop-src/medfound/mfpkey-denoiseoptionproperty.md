---
description: Especifica se o codec usará o filtro de ruído durante a codificação.
ms.assetid: 9e099378-bb77-4dca-9171-7fe58e0139de
title: MFPKEY_DENOISEOPTION propriedade (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0483edbda1c2eb3ec929fb662fe4544cb09e7d43dfd1b30421d14eb06d2a365b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954066"
---
# <a name="mfpkey_denoiseoption-property"></a>Propriedade MFPKEY \_ DENOISEOPTION

Especifica se o codec usará o filtro de ruído durante a codificação.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCDenoiseOption

## <a name="data-type"></a>Tipo de Dados

BOOL da VT \_

## <a name="default-value"></a>Valor padrão

FALSE

## <a name="remarks"></a>Comentários

O filtro de ruído pode melhorar a qualidade de fontes de vídeo com ruído, como filmes contendo muita granulação ou uma gravação de vídeo com pouca luz. Esse filtro pode ser usado em cenários de codificação ao vivo em que o pré-processamento externo não é uma opção.

Esse filtro deve ser desabilitado para fontes de vídeo limpas, pois pode reduzir a qualidade da imagem quando a qualidade é boa para começar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation propriedades](media-foundation-properties.md)
</dt> </dl>

 

 




