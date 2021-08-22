---
title: WM/WMShadowFileSourceDRMType (SDK Windows Media Format 11)
description: O atributo WM/WMShadowFileSourceDRMType contém o tipo de gerenciamento de direitos usado para proteger o arquivo original do qual o arquivo ASF é derivado.
ms.assetid: 58e7a383-6e80-42fc-bc75-5920dbe67a40
keywords:
- Formato de mídia do Windows WM/WMShadowFileSourceDRMType
topic_type:
- apiref
api_name:
- WM/WMShadowFileSourceDRMType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85c7ea97d2388b402bd05f67c1d8f7bf417c69a6853b3485e2cf0484cedcbc5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118698134"
---
# <a name="wmwmshadowfilesourcedrmtype-windows-media-format-11-sdk"></a>WM/WMShadowFileSourceDRMType (SDK Windows Media Format 11)

O **atributo WM/WMShadowFileSourceDRMType** contém o tipo de gerenciamento de direitos usado para proteger o arquivo original do qual o arquivo ASF é derivado.

## <a name="global-constant"></a>Constante global

g \_ wszWMWMShadowFileSourceDRMType

## <a name="data-type"></a>Tipo de Dados

**CADEIA DE CARACTERES DE \_ TIPO \_ WMT**

## <a name="remarks"></a>Comentários

O conteúdo que existe em um formato de arquivo diferente do ASF e é protegido com algum tipo de gerenciamento de direitos pode ser convertido em um arquivo de mídia do Windows protegido pelo DRM de Mídia Windows por meio de um processo chamado importação de licença. Esse arquivo ASF deve conter esse atributo, bem como WM/WMShadowFileSourceFileType para rastrear de onde o conteúdo veio.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> </dl>

 

 




