---
description: A \_ \_ Propriedade GUID PKEY AudioEndpoint fornece o identificador de dispositivo DirectSound que corresponde ao dispositivo de ponto de extremidade de áudio.
ms.assetid: d3119504-9b6a-47b8-b3c6-15cb329929cb
title: PKEY_AudioEndpoint_GUID (Mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45405cd2350777e535b50859e77aa56755d191fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749534"
---
# <a name="pkey_audioendpoint_guid"></a>PKEY \_ AudioEndpoint \_ GUID

A **propriedade \_ \_ GUID PKEY AudioEndpoint** fornece o identificador de dispositivo DirectSound que corresponde ao dispositivo de ponto de extremidade de áudio. O valor da propriedade é um GUID que o cliente pode fornecer como o identificador do dispositivo para a função **DirectSoundCreate** ou **DirectSoundCaptureCreate** na API do DirectSound. Esse valor identifica exclusivamente o dispositivo de ponto de extremidade de áudio em todos os dispositivos de ponto de extremidade de áudio no sistema. Para obter mais informações sobre o DirectSound, consulte a documentação do SDK do DirectX.

O membro **VT** da estrutura **PROPVARIANT** é definido como VT \_ LPWSTR.

O membro **pwszVal** da estrutura **PROPVARIANT** aponta para uma cadeia de caracteres largos terminada em nulo que contém um GUID que identifica o dispositivo de ponto de extremidade de áudio no DirectSound.

Conforme explicado anteriormente, a [API do MMDevice](mmdevice-api.md) dá suporte a funções de [dispositivo](device-roles.md). Embora o DirectSound não ofereça suporte direto a funções de dispositivo, um cliente DirectSound pode usar a \_ propriedade de GUID PKEY AudioEndpoint \_ para selecionar um dispositivo de captura ou processamento DirectSound com base em sua função de dispositivo.

Por exemplo, um aplicativo DirectSound executa as seguintes etapas para criar um dispositivo DirectSound que corresponde ao dispositivo de ponto de extremidade de renderização ao qual o usuário atribuiu a função eMultimedia:

1.  Chame o método [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) para obter a interface [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) do dispositivo de ponto de extremidade de renderização que tem a função eMultimedia.
2.  Chame o método [**IMMDevice:: OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) para obter a interface **IPropertyStore** do dispositivo eMultimedia. Para obter mais informações sobre o **IPropertyStore**, consulte a documentação do SDK do Windows.
3.  Chame o método **IPropertyStore:: GetValue** para obter o \_ valor da propriedade PKEY AudioEndpoint \_ GUID.
4.  Converta o valor da propriedade de um GUID no formato de cadeia de caracteres em uma estrutura de GUID de 16 bytes.
5.  Chame a função **DirectSoundCreate** com o GUID para criar o dispositivo com a função eMultimedia.

> [!Note]  
> **PKEY \_ AudioEndpoint \_ GUID** é uma propriedade somente leitura, independentemente do modo de acesso de armazenamento solicitado pelo aplicativo em [**IMMDevice:: OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore). Se um aplicativo tentar definir um valor usando **IPropertyStore:: SetValue**, essa chamada falhará com o código de \_ erro E ACCESSDENIED.

 

Observe que o GUID de 16 bytes gerado na etapa 4 corresponde ao GUID do dispositivo que identifica o dispositivo durante a enumeração do dispositivo DirectSound. A função **DirectSoundEnumerate** enumera os dispositivos de ponto de extremidade de renderização e a função **DirectSoundCaptureEnumerate** enumera os dispositivos de ponto de extremidade de captura. Em ambos os casos, o GUID do dispositivo é o primeiro parâmetro passado para a função de retorno de chamada de enumeração. Para obter mais informações sobre a enumeração do DirectSound, consulte a documentação do SDK do DirectX.

Para obter um exemplo de código que usa a \_ propriedade de GUID PKEY AudioEndpoint \_ , consulte [funções de dispositivo para aplicativos DirectSound](device-roles-for-directsound-applications.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Mmdeviceapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades do ponto de extremidade de áudio**](audio-endpoint-properties.md)
</dt> <dt>

[Propriedades de áudio de núcleo](core-audio-properties.md)
</dt> </dl>

 

 




