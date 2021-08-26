---
description: A propriedade \_ GUID de AudioEndpoint \_ PKEY fornece o identificador de dispositivo DirectSound que corresponde ao dispositivo de ponto de extremidade de áudio.
ms.assetid: d3119504-9b6a-47b8-b3c6-15cb329929cb
title: PKEY_AudioEndpoint_GUID (Mmdeviceapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 357531a76316381e9ae39f867a5b6cfa0a055a04f41b0cba5fab95fcccbcc7fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104356"
---
# <a name="pkey_audioendpoint_guid"></a>GUID do \_ ponto de vista de áudio \_ PKEY

A **propriedade GUID de \_ AudioEndpoint \_ PKEY** fornece o identificador de dispositivo DirectSound que corresponde ao dispositivo de ponto de extremidade de áudio. O valor da propriedade é um GUID que o cliente pode fornecer como o identificador de dispositivo para a função **DirectSoundCreate** ou **DirectSoundCaptureCreate** na API directSound. Esse valor identifica exclusivamente o dispositivo de ponto de extremidade de áudio em todos os dispositivos de ponto de extremidade de áudio no sistema. Para obter mais informações sobre o DirectSound, consulte a documentação do SDK do DirectX.

O **membro vt** da estrutura **PROPVARIANT** é definido como VT \_ LPWSTR.

O **membro pwszVal** da estrutura **PROPVARIANT** aponta para uma cadeia de caracteres largos terminada em nulo que contém um GUID que identifica o dispositivo de ponto de extremidade de áudio no DirectSound.

Conforme explicado anteriormente, a [API MMDevice dá](mmdevice-api.md) suporte a [funções de dispositivo](device-roles.md). Embora o DirectSound não dá suporte diretamente a funções de dispositivo, um cliente DirectSound pode usar a propriedade GUID de AudioEndpoint PKEY para selecionar um dispositivo de renderização ou captura DirectSound com base em sua função \_ \_ de dispositivo.

Por exemplo, um aplicativo DirectSound executa as seguintes etapas para criar um dispositivo DirectSound que corresponde ao dispositivo de ponto de extremidade de renderização ao que o usuário atribuiu a função eMultimedia:

1.  Chame o método [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) para obter a interface [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) do dispositivo de ponto de extremidade de renderização que tem a função eMultimedia.
2.  Chame o [**método IMMDevice::OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) para obter a interface **IPropertyStore** do dispositivo eMultimedia. Para obter mais informações sobre **o IPropertyStore,** consulte a documentação Windows SDK.
3.  Chame o **método IPropertyStore::GetValue** para obter o valor da propriedade \_ GUID de AudioEndpoint \_ PKEY.
4.  Converta o valor da propriedade de um GUID no formato de cadeia de caracteres em uma estrutura GUID de 16 byte.
5.  Chame a **função DirectSoundCreate** com o GUID para criar o dispositivo com a função eMultimedia.

> [!Note]  
> **PKEY \_ O GUID do \_ AudioEndpoint** é uma propriedade somente leitura, independentemente do modo de acesso de armazenamento solicitado pelo aplicativo [**no IMMDevice::OpenPropertyStore.**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) Se um aplicativo tentar definir um valor usando **IPropertyStore::SetValue**, essa chamada falhará com o código de erro E \_ ACCESSDENIED.

 

Observe que o GUID de 16 byte gerado na etapa 4 corresponde ao GUID do dispositivo que identifica o dispositivo durante a enumeração do dispositivo DirectSound. A **função DirectSoundEnumerate** enumera dispositivos de ponto de extremidade de renderização e a **função DirectSoundCaptureEnumerate** enumera dispositivos de ponto de extremidade de captura. Em ambos os casos, o GUID do dispositivo é o primeiro parâmetro passado para a função de retorno de chamada de enumeração. Para obter mais informações sobre a enumeração DirectSound, consulte a documentação do SDK do DirectX.

Para ver um exemplo de código que usa a propriedade \_ GUID de AudioEndpoint \_ PKEY, consulte Funções de dispositivo para [aplicativos DirectSound](device-roles-for-directsound-applications.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                     |
| Cabeçalho<br/>                   | <dl> <dt>Mmdeviceapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades do ponto de extremidade de áudio**](audio-endpoint-properties.md)
</dt> <dt>

[Propriedades de áudio principais](core-audio-properties.md)
</dt> </dl>

 

 




