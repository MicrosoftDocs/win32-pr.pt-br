---
description: Obtém o tamanho da imagem decodificada, em pixels.
ms.assetid: 2F0DD10F-CF7A-4A6F-91A9-E3828DF2B947
title: Propriedade AVDecVideoImageSize (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba4c059dfb1b2aebad4da10e54a3ecc1224a00d9cffcdb13dc7c87f4e29d4e83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000186"
---
# <a name="avdecvideoimagesize-property"></a>Propriedade AVDecVideoImageSize

Obtém o tamanho da imagem decodificada, em pixels.

Esta propriedade é somente para leitura.

## <a name="data-type"></a>Tipo de dados

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVDecVideoImageSize**

## <a name="property-value"></a>Valor da propriedade

Os 16 bits altos contêm a largura e os 16 bits baixos contêm a altura.

## <a name="remarks"></a>Comentários

O número de canais inclui o canal LFE (efeito de baixa frequência), se presente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional aplicativos \[ UWP da área de \| trabalho\]<br/>                     |
| Servidor mínimo com suporte<br/> | Windows aplicativos da área de trabalho do servidor 2000 \[ \| aplicativos UWP\]<br/>                           |
| Cabeçalho<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades da API do Codec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI Interface**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




