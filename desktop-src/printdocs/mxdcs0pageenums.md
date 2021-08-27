---
description: A enumeração ENUMS MXDC S0 PAGE é usada para especificar tipos de recursos que podem ser associados a páginas em documentos XPS e que podem ser processados ou passados não processados pelo \_ \_ \_ MXDC (Conversor de Documentos) do Microsoft XPS para sua saída.
ms.assetid: e111d92e-5102-4b39-b311-f9ff1d1a96f1
title: MXDC_S0_PAGE_ENUMS enumeração (Winspool.h)
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
ms.openlocfilehash: 3aa6622ea65e00c1447e6042a41c998e9ab30a29d1172d43e1a1da81feb34c54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118471310"
---
# <a name="mxdc_s0_page_enums-enumeration"></a>\_ \_ Enumeração ENUMS de PÁGINA \_ S0 MXDC

A enumeração **\_ \_ \_ ENUMS MXDC S0 PAGE** é usada para especificar tipos de recursos que podem ser associados a páginas em documentos XPS e que podem ser processados ou passados não processados pelo MXDC (Conversor de Documentos) do Microsoft XPS para sua saída.

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

<span id="MXDC_RESOURCE_TTF"></span><span id="mxdc_resource_ttf"></span>**MXDC \_ RESOURCE \_ TTF**
</dt> <dd>

Fonte TrueType ou OpenType.

</dd> <dt>

<span id="MXDC_RESOURCE_JPEG"></span><span id="mxdc_resource_jpeg"></span>**MXDC \_ RESOURCE \_ JPEG**
</dt> <dd>

Imagem JPEG

</dd> <dt>

<span id="MXDC_RESOURCE_PNG"></span><span id="mxdc_resource_png"></span>**MXDC \_ RESOURCE \_ PNG**
</dt> <dd>

Imagem PNG.

</dd> <dt>

<span id="MXDC_RESOURCE_TIFF"></span><span id="mxdc_resource_tiff"></span>**MXDC \_ RESOURCE \_ TIFF**
</dt> <dd>

Imagem TIFF.

</dd> <dt>

<span id="MXDC_RESOURCE_WDP"></span><span id="mxdc_resource_wdp"></span>**MXDC \_ RESOURCE \_ WDP**
</dt> <dd>

Windows Imagem da Foto de Mídia.

</dd> <dt>

<span id="MXDC_RESOURCE_DICTIONARY"></span><span id="mxdc_resource_dictionary"></span>**DICIONÁRIO DE RECURSOS \_ MXDC \_**
</dt> <dd>

Dicionário de recursos remotos que deve ser passado para a saída do MXDC não processada.

</dd> <dt>

<span id="MXDC_RESOURCE_ICC_PROFILE"></span><span id="mxdc_resource_icc_profile"></span>**PERFIL \_ ICC DO RECURSO \_ MXDC \_**
</dt> <dd>

Perfil ICC que deve ser passado para a saída do MXDC não processada.

</dd> <dt>

<span id="MXDC_RESOURCE_JPEG_THUMBNAIL"></span><span id="mxdc_resource_jpeg_thumbnail"></span>**MINIATURA JPEG DO RECURSO MXDC \_ \_ \_**
</dt> <dd>

Miniatura JPEG que deve ser passada para a saída do MXDC não processada.

</dd> <dt>

<span id="MXDC_RESOURCE_PNG_THUMBNAIL"></span><span id="mxdc_resource_png_thumbnail"></span>**MINIATURA \_ PNG DO \_ RECURSO MXDC \_**
</dt> <dd>

Miniatura PNG que deve ser passada para a saída do MXDC não processada.

</dd> <dt>

<span id="MXDC_RESOURCE_MAX"></span><span id="mxdc_resource_max"></span>**MXDC \_ RESOURCE \_ MAX**
</dt> <dd>

A contagem máxima de recursos para validação.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa enumeração é usada principalmente como o **membro dwResourceType** da estrutura [**MXDC \_ XPS \_ S0PAGE \_ RESOURCE \_ T.**](mxdcxpss0pageresource.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |



 

 




