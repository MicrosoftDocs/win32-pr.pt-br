---
description: Especifica se o MFT do remux de vídeo H. 264 deve marcar I imagens como ponto de limpeza para melhor capacidade de busca. Isso tem o potencial de danos em buscas em arquivos MP4 finais em não conformidade.
ms.assetid: BB521E13-40A4-4643-B071-76B8CBC62074
title: Atributo MFT_REMUX_MARK_I_PICTURE_AS_CLEAN_POINT (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26c9fe8398507f6d7af5d0e4bf45a36a4454f220
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789250"
---
# <a name="mft_remux_mark_i_picture_as_clean_point-attribute"></a>MFT \_ remux \_ Marcar \_ \_ \_ como atributo de \_ \_ ponto limpo

Especifica se o MFT do remux de vídeo H. 264 deve marcar I imagens como ponto de limpeza para melhor capacidade de busca. Isso tem o potencial de danos em buscas em arquivos MP4 finais em não conformidade.

## <a name="data-type"></a>Tipo de dados

**Bool** armazenado como **UINT32**

## <a name="remarks"></a>Comentários

A imagem do ponto de limpeza deve ser compactada com imagens IDR por definição.

Isso não é recomendado para gravar ou remuxing arquivos MP4, a menos que esse exercício seja produzir alguns arquivos pseudo MP4 intermediários para edição de vídeo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]<br/>                             |
| parâmetro<br/>                   | <dl> <dt>Mftransform. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Mftransform. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




