---
title: _WAVEFORMATEX estrutura
description: A estrutura \_WAVEFORMATEX define o formato dos dados de áudio em ondas.
ms.assetid: 2128f07a-4858-49b7-b031-16d4a84c9d32
keywords:
- _WAVEFORMATEX estrutura windows Media Gerenciador de Dispositivos
topic_type:
- apiref
api_name:
- _WAVEFORMATEX
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e149608d740df6df40b39b64b09ac11837a721b5b4844f1a73eb52e1b5cea479
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118586741"
---
# <a name="_waveformatex-structure"></a>\_Estrutura WAVEFORMATEX

A **\_ estrutura WAVEFORMATEX** define o formato de dados waveform-audio.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _tWAVEFORMATEX {
  WORD  wFormatTag;
  WORD  nChannels;
  DWORD nSamplesPerSec;
  DWORD nAvgBytesPerSec;
  WORD  nBlockAlign;
  WORD  wBitsPerSample;
  WORD  cbSize;
} _WAVEFORMATEX;
```



## <a name="members"></a>Membros

<dl> <dt>

**Wformattag**
</dt> <dd>

Deve ser definido como um formato ou formatos com suporte pelo dispositivo. Observe que as versões anteriores do Windows Media Gerenciador de Dispositivos usar WMDM WAVE FORMAT ALL para indicar \_ suporte para todos os \_ \_ formatos. No entanto, isso não é mais recomendado, pois diferentes players de mídia interpretarão isso de maneiras diferentes e poucos dispositivos poderão realmente reproduzir qualquer formato de arquivo. Agora é recomendável que você use o valor WMDM ENUM PROP VALID VALUES ANY da \_ \_ \_ \_ \_ enumeração [**WMDM \_ ENUM \_ PROP VALUES \_ \_ \_ FORM**](wmdm-enum-prop-valid-values-form.md) [**\_ \_ \_**](wmdm-prop-values-range.md) ou especifique melhor ainda um intervalo de formatos com a estrutura INTERVALO DE VALORES DE PROP DO WMDM.

</dd> <dt>

**nChannels**
</dt> <dd>

Número de canais nos dados waveform-audio. Os dados de um canal usam um canal e os dados estéreos usam dois canais.

</dd> <dt>

**nSamplesPerSec**
</dt> <dd>

Taxa de exemplo, em amostras por segundo (Hertz), na qual cada canal deve ser tocado ou gravado. Os valores comuns para **nSamplesPerSec** são 8,0 quilohertz (kHz), 11,025 kHz, 22,05 kHz e 44,1 kHz.

</dd> <dt>

**nAvgBytesPerSec**
</dt> <dd>

Taxa média de transferência de dados necessária para a marca de formato, em bytes por segundo. O software de reprodução e gravação pode estimar tamanhos de buffer usando o **membro nAvgBytesPerSec.**

</dd> <dt>

**nBlockAlign**
</dt> <dd>

Alinhamento de bloco, em bytes. O alinhamento do bloco é a unidade atômica mínima de dados para o **tipo de formato wFormatTag.** A reprodução e a gravação de software devem processar vários bytes **nBlockAlign** de dados por vez. Os dados gravados e lidos de um dispositivo sempre devem começar no início de um bloco. Por exemplo, não é possível iniciar corretamente a reprodução de dados PCM no meio de um exemplo (ou seja, em um limite que não está alinhado a blocos).

</dd> <dt>

**wBitsPerSample**
</dt> <dd>

Bits por exemplo para o **tipo de formato wFormatTag.**

</dd> <dt>

**cbSize**
</dt> <dd>

Esse membro é ignorado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdm.idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMDSPDevice::GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getformatsupport)
</dt> <dt>

[**IMDSPStorage::CreateStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-createstorage)
</dt> <dt>

[**IMDSPStorage::GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getattributes)
</dt> <dt>

[**IWMDMDevice::GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport)
</dt> <dt>

[**IWMDMOperation::GetObjectAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-getobjectattributes)
</dt> <dt>

[**IWMDMOperation::SetObjectAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-setobjectattributes)
</dt> <dt>

[**IWMDMStorage::GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes)
</dt> <dt>

[**Estruturas**](structures.md)
</dt> </dl>

 

 





