---
description: Especifica para uma topologia de transcodificação se o carregador de topologia carregar transformações baseadas em hardware.
ms.assetid: 33db8621-114a-4531-908f-f30034441973
title: Atributo MF_TRANSCODE_TOPOLOGYMODE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f700397914faf7fee35e7f82027d8f8771e8b099
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827415"
---
# <a name="mf_transcode_topologymode-attribute"></a>\_Atributo topologymode de transcodificação MF \_

Especifica para uma topologia de transcodificação se o carregador de topologia carregar transformações baseadas em hardware.

O modo de topologia especifica se as transformações de hardware (como codecs de hardware) podem ser usadas na topologia de transcodificação. O aplicativo pode armazenar esse atributo em um perfil de transcodificação chamando [**IMFTranscodeProfile:: Setcontêinerattributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes).

## <a name="data-type"></a>Tipo de dados

**[**MF \_ Transcodificar \_ \_ sinalizadores topologymode**](/windows/desktop/api/mfidl/ne-mfidl-mf_transcode_topologymode_flags)** armazenados como **UINT32**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Comentários

Esse atributo é opcional. Ele deve ter um dos valores a seguir.



| Valor                                              | Descrição                                                                                                                                                                                                                                                                       |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **HARDWARE do MF \_ transcodificar \_ topologymode \_ \_ permitido** | O carregador de topologia carregará MFTs baseadas em hardware, como decodificadores de hardware, quando disponível.<br/> O carregador de topologia voltará automaticamente para a decodificação de software se nenhum decodificador de hardware for encontrado ou se um decodificador de hardware não conseguir se conectar por algum motivo.<br/> |
| **\_somente software MF transcodificar \_ topologymode \_ \_**    | O carregador de topologia carregará apenas MFTs de software, incluindo os decodificadores de software.                                                                                                                                                                                                    |



 

O valor padrão é **MF \_ transcodificar \_ topologymode \_ \_ somente software**.

Se o carregador de topologia inserir uma MFT de hardware na topologia, ele definirá o atributo de atributo de URL de hardware de enumeração de MFT no nó de topologia. [ \_ \_ \_ \_ ](mft-enum-hardware-url-attribute.md) Para verificar se um MFT de hardware está presente, enumere os nós na topologia resolvida e verifique se esse atributo está presente.

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                            |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[API de transcodificação](transcode-api.md)
</dt> <dt>

[**IMFTranscodeProfile:: getcontainerattributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getcontainerattributes)
</dt> <dt>

[**IMFTranscodeProfile:: setcontainerattributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)
</dt> </dl>

 

 




