---
description: A \_ enumeração de \_ enumerações de página MXDC S0 \_ é usada para especificar tipos de recursos que podem ser associados a páginas em documentos XPS e que podem ser processados, ou passados não processados pelo conversor de documento XPS da Microsoft (MXDC) para sua saída.
ms.assetid: e111d92e-5102-4b39-b311-f9ff1d1a96f1
title: Enumeração de MXDC_S0_PAGE_ENUMS (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_S0_PAGE_ENUMS
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 1b4331210027f7fc23f36fb6b9d13a2c232ccbf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828309"
---
# <a name="mxdc_s0_page_enums-enumeration"></a>\_Enumeração de \_ enumerações de página MXDC S0 \_

A enumeração de **\_ \_ \_ enumerações de página MXDC S0** é usada para especificar tipos de recursos que podem ser associados a páginas em documentos XPS e que podem ser processados, ou passados não processados pelo conversor de documento XPS da Microsoft (MXDC) para sua saída.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagMxdcS0PageEnums { 
  MXDC_RESOURCE_TTF,
  MXDC_RESOURCE_JPEG,
  MXDC_RESOURCE_PNG,
  MXDC_RESOURCE_TIFF,
  MXDC_RESOURCE_WDP,
  MXDC_RESOURCE_DICTIONARY,
  MXDC_RESOURCE_ICC_PROFILE,
  MXDC_RESOURCE_JPEG_THUMBNAIL,
  MXDC_RESOURCE_PNG_THUMBNAIL,
  MXDC_RESOURCE_MAX
} MXDC_S0_PAGE_ENUMS;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MXDC_RESOURCE_TTF"></span><span id="mxdc_resource_ttf"></span>**MXDC do \_ recurso \_ ttf**
</dt> <dd>

Fonte TrueType ou OpenType.

</dd> <dt>

<span id="MXDC_RESOURCE_JPEG"></span><span id="mxdc_resource_jpeg"></span>**MXDC \_ recurso \_ JPEG**
</dt> <dd>

Imagem JPEG

</dd> <dt>

<span id="MXDC_RESOURCE_PNG"></span><span id="mxdc_resource_png"></span>**MXDC \_ png de recursos \_**
</dt> <dd>

Imagem PNG.

</dd> <dt>

<span id="MXDC_RESOURCE_TIFF"></span><span id="mxdc_resource_tiff"></span>**\_recurso \_ TIFF do MXDC**
</dt> <dd>

Imagem TIFF.

</dd> <dt>

<span id="MXDC_RESOURCE_WDP"></span><span id="mxdc_resource_wdp"></span>**MXDC de \_ recursos \_ WDP**
</dt> <dd>

Imagem de foto do Windows Media.

</dd> <dt>

<span id="MXDC_RESOURCE_DICTIONARY"></span><span id="mxdc_resource_dictionary"></span>**\_dicionário de recursos MXDC \_**
</dt> <dd>

Dicionário de recursos remotos que deve ser passado para a saída do MXDC não processado.

</dd> <dt>

<span id="MXDC_RESOURCE_ICC_PROFILE"></span><span id="mxdc_resource_icc_profile"></span>**\_ \_ perfil ICC do recurso MXDC \_**
</dt> <dd>

Perfil ICC que deve ser passado para a saída do MXDC não processada.

</dd> <dt>

<span id="MXDC_RESOURCE_JPEG_THUMBNAIL"></span><span id="mxdc_resource_jpeg_thumbnail"></span>**\_miniatura de \_ JPEG do recurso MXDC \_**
</dt> <dd>

Miniatura JPEG que deve ser passada para a saída do MXDC não processada.

</dd> <dt>

<span id="MXDC_RESOURCE_PNG_THUMBNAIL"></span><span id="mxdc_resource_png_thumbnail"></span>**\_miniatura do \_ png do recurso MXDC \_**
</dt> <dd>

Miniatura PNG que deve ser passada para a saída do MXDC não processada.

</dd> <dt>

<span id="MXDC_RESOURCE_MAX"></span><span id="mxdc_resource_max"></span>**MXDC \_ máximo do recurso \_**
</dt> <dd>

A contagem máxima de recursos para validação.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa enumeração é usada principalmente como o membro **dwResourceType** da estrutura [**MXDC \_ XPS \_ S0PAGE \_ Resource \_ T**](mxdcxpss0pageresource.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                      |
| parâmetro<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |



 

 




