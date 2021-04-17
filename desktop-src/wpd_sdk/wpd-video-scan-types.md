---
description: O \_ tipo de enumeração de tipos de verificação de vídeo WPD \_ \_ descreve como os campos em um arquivo de vídeo são codificados.
ms.assetid: ea0dab57-6783-4d02-a43c-414e313f1e80
title: Enumeração de WPD_VIDEO_SCAN_TYPES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_VIDEO_SCAN_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: a636bc95fd3d25de20c2df413576a504c4fa1b96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749701"
---
# <a name="wpd_video_scan_types-enumeration"></a>\_Enumeração de \_ tipos de verificação de vídeo WPD \_

O tipo de enumeração de **\_ tipos de \_ verificação \_ de vídeo WPD** descreve como os campos em um arquivo de vídeo são codificados.

## <a name="syntax"></a>Syntax


```C++
typedef enum WPD_VIDEO_SCAN_TYPES { 
  WPD_VIDEO_SCAN_TYPE_UNUSED                           = 0,
  WPD_VIDEO_SCAN_TYPE_PROGRESSIVE                      = 1,
  WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_UPPER_FIRST    = 2,
  WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_LOWER_FIRST    = 3,
  WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_UPPER_FIRST         = 4,
  WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_LOWER_FIRST         = 5,
  WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE                  = 6,
  WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE_AND_PROGRESSIVE  = 7
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_UNUSED"></span><span id="wpd_video_scan_type_unused"></span>**\_tipo de exame de vídeo WPD \_ \_ \_ não utilizado**
</dt> <dd>

O tipo de verificação não foi definido para este arquivo de vídeo ou não é aplicável.

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_PROGRESSIVE"></span><span id="wpd_video_scan_type_progressive"></span>**\_tipo de exame de vídeo WPD \_ \_ \_ progressivo**
</dt> <dd>

Um arquivo de vídeo de verificação progressiva.

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_UPPER_FIRST"></span><span id="wpd_video_scan_type_field_interleaved_upper_first"></span>**\_campo de tipo de verificação de vídeo WPD \_ \_ \_ \_ intercalado \_ superior \_ primeiro**
</dt> <dd>

Um arquivo de vídeo intercalado no qual os campos são alternativos e o campo superior (com linha 1) é desenhado primeiro. Para obter mais informações, consulte a seção Comentários.

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_LOWER_FIRST"></span><span id="wpd_video_scan_type_field_interleaved_lower_first"></span>**\_campo de tipo de verificação de vídeo WPD \_ \_ \_ \_ intercalado \_ mais baixo \_ primeiro**
</dt> <dd>

Um arquivo de vídeo intercalado no qual os campos são alternativos e o campo inferior (com linha 2) é desenhado primeiro. Para obter mais informações, consulte comentários, seguindo esta seção.

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_UPPER_FIRST"></span><span id="wpd_video_scan_type_field_single_upper_first"></span>**campo de tipo de verificação de vídeo WPD- \_ \_ \_ \_ \_ único \_ superior \_ primeiro**
</dt> <dd>

Um arquivo de vídeo intercalado em que os campos são enviados como amostras contíguas e o campo superior (com a linha 1) é desenhado primeiro. Para obter mais informações, consulte comentários, seguindo esta seção.

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_LOWER_FIRST"></span><span id="wpd_video_scan_type_field_single_lower_first"></span>**campo de tipo de verificação de vídeo WPD- \_ \_ \_ \_ \_ \_ \_ primeiro inferior**
</dt> <dd>

Um arquivo de vídeo intercalado em que os campos são enviados como amostras contíguas e o campo inferior (com linha 2) é enviado primeiro.

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE"></span><span id="wpd_video_scan_type_mixed_interlace"></span>**\_exame de vídeo WPD \_ \_ tipo \_ \_ entrelaçado misto**
</dt> <dd>

Um arquivo de vídeo com uma combinação de modos de entrelaçamento.

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE_AND_PROGRESSIVE"></span><span id="wpd_video_scan_type_mixed_interlace_and_progressive"></span>**\_ \_ exame de vídeo \_ WPD \_ tipo \_ entrelaçado misto \_ e \_ progressivo**
</dt> <dd>

Um arquivo de vídeo com uma combinação de modos entrelaçados e progressivos.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa enumeração é usada pela propriedade [de \_ \_ \_ tipo de verificação de vídeo WPD](properties-and-attributes.md) .

Há dois tipos de formatos de arquivo intercalados que são especificados por essa enumeração. **WPD \_ O \_ campo de tipo de verificação de vídeo \_ \_ \_ intercalado** refere-se a um formato de arquivo em que os quadros são entregues, pois eles eram campos digitalizados e os dados são colocados em linha por linha, como mostrado aqui:

**Quadro 1**

Campo 1: linha 1

Campo 2: linha 1

Campo 1: linha 2

Campo 2: linha 2

Campo 1: linha 3

Campo 2: linha 3

...

**WPD \_ Campo de tipo de verificação de vídeo \_ \_ \_ \_ único** refere-se a um formato de arquivo em que cada campo é armazenado em um único bloco de linhas de varredura, e os campos são armazenados em sequência, como mostrado aqui:

**Quadro 1**

Campo 1: linha 1

Campo 1: linha 2

Campo 1: linha 3

...

Seguido por

Campo 2: linha 1

Campo 2: linha 2

Campo 2: linha 3

...

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Estruturas e tipos de enumeração**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




