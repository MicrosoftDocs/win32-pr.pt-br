---
description: Especifica para uma topologia de transcodificar se o carregador de topologia carregará as transformação baseadas em hardware.
ms.assetid: 33db8621-114a-4531-908f-f30034441973
title: MF_TRANSCODE_TOPOLOGYMODE atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36e8715c135e074956af2280b8474172e94e69e1cca20cd01b020fc6dc79076c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663836"
---
# <a name="mf_transcode_topologymode-attribute"></a>Atributo MF \_ TRANSCODE \_ TOPOLOGYMODE

Especifica para uma topologia de transcodificar se o carregador de topologia carregará as transformação baseadas em hardware.

O modo de topologia especifica se as transformaçãos de hardware (como codecs de hardware) podem ser usadas na topologia de transcódigo. O aplicativo pode armazenar esse atributo em um perfil de transcódigo chamando [**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes).

## <a name="data-type"></a>Tipo de dados

**[**MF \_ SINALIZADORES \_ TRANSCODE TOPOLOGYMODE \_ armazenados**](/windows/desktop/api/mfidl/ne-mfidl-mf_transcode_topologymode_flags)** como **UINT32**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Comentários

Esse atributo é opcional. Ele deve ter um dos valores a seguir.



| Valor                                              | Descrição                                                                                                                                                                                                                                                                       |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MF \_ TRANSCODE \_ TOPOLOGYMODE \_ HARDWARE \_ ALLOWED** | O Carregador de Topologia carregará MFTs baseados em hardware, como decodificadores de hardware, quando disponíveis.<br/> O Carregador de Topologia retornará automaticamente à decodificação de software se nenhum decodificador de hardware for encontrado ou se um decodificador de hardware falhar ao se conectar por algum motivo.<br/> |
| **MF \_ TRANSCODE \_ TOPOLOGYMODE \_ SOFTWARE \_ ONLY**    | O Carregador de Topologia carregará apenas MFTs de software, incluindo decodificadores de software.                                                                                                                                                                                                    |



 

O valor padrão é **MF \_ TRANSCODE \_ TOPOLOGYMODE \_ SOFTWARE \_ ONLY**.

Se o Carregador de Topologia inserir um MFT de hardware na topologia, ele define o atributo Atributo de URL de [ \_ \_ \_ \_ HARDWARE MFT ENUM](mft-enum-hardware-url-attribute.md) no nó de topologia. Para verificar se um MFT de hardware está presente, enumere os nós na topologia resolvida e verifique se esse atributo está presente.

A constante GUID para esse atributo é exportada de mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                            |
| Cabeçalho<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[API de transcodificar](transcode-api.md)
</dt> <dt>

[**IMFTranscodeProfile::GetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getcontainerattributes)
</dt> <dt>

[**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)
</dt> </dl>

 

 




