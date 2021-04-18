---
description: Especifica se um arquivo ASF (Advanced Systems Format) é difundido ou pesquisável. Esse valor corresponde ao campo Flags do objeto de propriedades File, definido na especificação do ASF.
ms.assetid: 427f0dca-f945-4c89-a87a-a7c86291b1c5
title: Atributo MF_PD_ASF_FILEPROPERTIES_FLAGS (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee294642188a0f2e22143feeca6791fea591cbb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751023"
---
# <a name="mf_pd_asf_fileproperties_flags-attribute"></a>\_Atributo de \_ \_ sinalizadores FileProperties do MF PD ASF \_

Especifica se um arquivo ASF (Advanced Systems Format) é difundido ou pesquisável. Esse valor corresponde ao campo Flags do objeto de propriedades File, definido na especificação do ASF.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

Esse atributo se aplica a descritores de apresentação para conteúdo ASF. O valor do atributo é uma operação OR dos seguintes sinalizadores:



| Sinalizador | Descrição                                                                                                                                                                                                                                                                                       |
|------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x01 | Sinalizador de difusão. O arquivo está em processo de criação.                                                                                                                                                                                                                                      |
| 0x02 | Sinalizador pesquisável. O arquivo é pesquisável.<br/> Um arquivo será pesquisável se um fluxo de áudio estiver presente e o tamanho máximo do pacote de dados for igual ao tamanho mínimo do pacote de dados. Ele também pode ser pesquisável se o arquivo tiver um fluxo de áudio e um fluxo de vídeo com um objeto de índice simples correspondente.<br/> |



 

O método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) gera esse atributo dos metadados do ASF.

Se o sinalizador de difusão for definido, os seguintes atributos no descritor de apresentação não serão válidos:

-   [**\_ID do \_ \_ arquivo FileProperties \_ do MF PD ASF \_**](mf-pd-asf-fileproperties-file-id-attribute.md)
-   [**\_hora de \_ \_ criação de FileProperties do \_ MF PD ASF \_**](mf-pd-asf-fileproperties-creation-time-attribute.md)
-   [**\_ \_ \_ pacotes FileProperties do MF PD ASF \_**](mf-pd-asf-fileproperties-packets-attribute.md)
-   [**\_duração da \_ \_ reprodução de FileProperties do \_ MF PD ASF \_**](mf-pd-asf-fileproperties-play-duration-attribute.md)
-   [**\_duração de \_ \_ envio de FileProperties do \_ MF PD ASF \_**](mf-pd-asf-fileproperties-send-duration-attribute.md)

Além disso, os valores de atributo de [**\_ \_ \_ \_ \_ \_ tamanho**](mf-pd-asf-fileproperties-min-packet-size-attribute.md) máximo de pacote FileProperties e MF PD ASF do [**MF \_ PD \_ \_ \_ \_ \_**](mf-pd-asf-fileproperties-max-packet-size-attribute.md) são definidos como o tamanho real do pacote.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Wmcontainer. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Atributos do descritor de apresentação](presentation-descriptor-attributes.md)
</dt> <dt>

[Objeto de cabeçalho ASF](asf-file-structure.md)
</dt> <dt>

[Descritores de apresentação](presentation-descriptors.md)
</dt> </dl>

 

 




