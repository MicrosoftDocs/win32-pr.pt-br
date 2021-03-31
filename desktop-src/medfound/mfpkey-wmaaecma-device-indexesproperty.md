---
description: Especifica quais dispositivos de áudio o DSP de captura de voz usa para capturar e renderizar áudio.
ms.assetid: 42b6b82b-ac64-4a07-956c-473dd57a128d
title: Propriedade MFPKEY_WMAAECMA_DEVICE_INDEXES (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b377e4335e78e81c8e7d3c5a9a0c1d00b8f9bae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827549"
---
# <a name="mfpkey_wmaaecma_device_indexes-property"></a>\_Propriedade de \_ índices de dispositivo MFPKEY WMAAECMA \_

Especifica quais dispositivos de áudio o DSP de captura de voz usa para capturar e renderizar áudio.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de Dados

\_I4 VT

## <a name="default-value"></a>Valor padrão

(-1,-1).

## <a name="applies-to"></a>Aplica-se A

-   [DSP de captura de voz](voicecapturedmo.md)

## <a name="remarks"></a>Comentários

Defina essa propriedade se você estiver usando o DSP no modo de origem. O DSP ignora essa propriedade no modo de filtro.

O valor da propriedade é a **palavra** de 2 16 bits s empacotada em um **DWORD**. Os 16 bits superiores especificam o dispositivo de renderização de áudio (normalmente um palestrante) e os 16 bits inferiores especificam o dispositivo de captura (normalmente um microfone). Cada dispositivo é especificado como um índice na coleção de dispositivos de áudio. Se o índice for-1, o dispositivo padrão será usado.

O índice do dispositivo corresponde ao índice da coleção usado na interface [**IMMDeviceCollection**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection) . O aplicativo deve reproduzir a voz de extremidade final por meio do dispositivo de renderização selecionado. (A voz de ponta é a voz da pessoa na outra extremidade da linha telefônica, que é reproduzida pelo orador no computador do usuário.) Se o dispositivo de renderização selecionado não tiver um fluxo ativo, o DSP não poderá processar nenhuma saída.

O valor padrão dessa propriedade é (-1,-1).

O exemplo a seguir mostra como inicializar o **PROPVARIANT** para essa propriedade.


```
int iSpeakerIndex = -1;
int iMicrophoneIndex = -1;

// Find the device indexes to initialize iSpeakerIndex and 
// iMicrophone index (not shown).

PROPVARIANT varDeviceIndexes;
PropVariantInit(&varDeviceIndexes);
varDeviceIndexes.vt = VT_I4;
varDeviceIndexes.lVal = (unsigned long)(iSpeakerIndex << 16) + 
    (unsigned long)(0x0000ffff & iMicrophoneIndex);
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| parâmetro<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[DSP de captura de voz](voicecapturedmo.md)
</dt> </dl>

 

 
