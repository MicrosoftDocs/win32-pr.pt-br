---
description: Especifica quais dispositivos de áudio o DSP de Captura de Voz usa para capturar e renderizar áudio.
ms.assetid: 42b6b82b-ac64-4a07-956c-473dd57a128d
title: MFPKEY_WMAAECMA_DEVICE_INDEXES propriedade (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c4e9fd9eae8d53f1fa19bd8b55d94d292b9cd6cbf214b7a71a6473f1af647f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117872976"
---
# <a name="mfpkey_wmaaecma_device_indexes-property"></a>Propriedade MFPKEY \_ WMAAECMA \_ DEVICE \_ INDEXES

Especifica quais dispositivos de áudio o DSP de Captura de Voz usa para capturar e renderizar áudio.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível somente usando [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo de Dados

VT \_ I4

## <a name="default-value"></a>Valor padrão

(-1, -1).

## <a name="applies-to"></a>Aplica-se A

-   [DSP de Captura de Voz](voicecapturedmo.md)

## <a name="remarks"></a>Comentários

De definir essa propriedade se você estiver usando o DSP no modo de origem. O DSP ignora essa propriedade no modo de filtro.

O valor da propriedade é dois **WORD** de 16 bits empacotados em um **DWORD.** Os 16 bits superiores especificam o dispositivo de renderização de áudio (normalmente um alto-falante) e os 16 bits inferiores especificam o dispositivo de captura (normalmente um microfone). Cada dispositivo é especificado como um índice na coleção de dispositivos de áudio. Se o índice for -1, o dispositivo padrão será usado.

O índice do dispositivo corresponde ao índice de coleção usado na interface [**IMMDeviceCollection.**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection) O aplicativo deve reproduzir a voz distante por meio do dispositivo de renderização selecionado. (A voz distante é a voz da pessoa na outra extremidade da linha telefônica, que é tocada por meio do locutor no computador do usuário.) Se o dispositivo de renderização selecionado não tiver um fluxo ativo, o DSP não poderá processar nenhuma saída.

O valor padrão dessa propriedade é (-1, -1).

O exemplo a seguir mostra como inicializar **o PROPVARIANT** para essa propriedade.


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
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation propriedades](media-foundation-properties.md)
</dt> <dt>

[DSP de Captura de Voz](voicecapturedmo.md)
</dt> </dl>

 

 
