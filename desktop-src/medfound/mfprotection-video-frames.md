---
description: Especifica se um aplicativo tem permissão para acessar quadros de vídeo descompactados.
ms.assetid: 7D2A9003-B36E-4082-877E-8AC7F5645E89
title: Atributo MFPROTECTION_VIDEO_FRAMES (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67a8ccfc56fb1c1b52b14e16d8e702111f3d8564
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763947"
---
# <a name="mfprotection_video_frames-attribute"></a>Atributo de quadros de \_ vídeo MFPROTECTION \_

Especifica se um aplicativo tem permissão para acessar quadros de vídeo descompactados.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

Um valor de 0 indica que o aplicativo tem permissão para acessar os quadros. Isso pode ser determinado como resultado de um contrato privado entre o aplicativo e o sistema de proteção de conteúdo específico em uso.

Um valor de 1 indica que o aplicativo tem permissão para acessar quadros se um certificado de aplicativo válido for fornecido pelo aplicativo (consulte [**IMFMediaEngineProtectedContent:: SetApplicationCertificate**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineprotectedcontent-setapplicationcertificate)).

Um valor de 0xFFFFFFFF, que é o valor padrão, indica que nenhum aplicativo tem permissão de acesso a quadros não compactados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos UWP do Windows 8\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Somente aplicativos UWP do Windows Server 2012 \[\]<br/>                                   |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo de mídia](media-type-attributes.md)
</dt> </dl>

 

 




