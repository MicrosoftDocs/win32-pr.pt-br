---
title: Estrutura de _WAVEFORMATEX
description: A estrutura \_WAVEFORMATEX define o formato dos dados de áudio em ondas.
ms.assetid: 2128f07a-4858-49b7-b031-16d4a84c9d32
keywords:
- Estrutura de _WAVEFORMATEX Windows Media Gerenciador de Dispositivos
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
ms.openlocfilehash: 8d1d0ede83e22033aee8f18d11b6230e471e0dfe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105800186"
---
# <a name="_waveformatex-structure"></a>\_Estrutura WAVEFORMATEX

A estrutura **\_ WAVEFORMATEX** define o formato dos dados de Wave-Audio.

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

**wFormatTag**
</dt> <dd>

Deve ser definido como um formato ou formatos com suporte pelo dispositivo. Observe que as versões anteriores do Windows Media Gerenciador de Dispositivos recomendadas usando \_ o \_ formato \_ de onda WMDM All para indicar suporte a todos os formatos. No entanto, isso não é mais recomendado, pois os media players diferentes interpretarão isso de maneiras diferentes, e poucos dispositivos podem realmente reproduzir qualquer formato de arquivo. Agora é recomendável que você use os \_ valores válidos da prop do SqlEnum \_ \_ \_ \_ qualquer valor da enumeração de [**\_ \_ \_ \_ \_ formato de valores válidos de prop do WMDM enum**](wmdm-enum-prop-valid-values-form.md) ou melhor ainda especifique um intervalo de formatos com a estrutura de [**\_ \_ \_ intervalo de valores prop**](wmdm-prop-values-range.md) . do WMDM.

</dd> <dt>

**nChannels**
</dt> <dd>

Número de canais nos dados de formato de onda-áudio. Os dados do monaural usam um canal e os dados estéreo usam dois canais.

</dd> <dt>

**nSamplesPerSec**
</dt> <dd>

Taxa de amostragem, em amostras por segundo (hertz), em que cada canal deve ser reproduzido ou registrado. Os valores comuns para **nSamplesPerSec** são 8,0 kilohertz (kHz), 11, 25 khz, 22, 5 khz e 44,1 kHz.

</dd> <dt>

**nAvgBytesPerSec**
</dt> <dd>

Taxa média de transferência de dados necessária para a marca de formato, em bytes por segundo. O software de reprodução e de gravação pode estimar tamanhos de buffer usando o membro **nAvgBytesPerSec** .

</dd> <dt>

**nBlockAlign**
</dt> <dd>

Alinhamento de bloco, em bytes. O alinhamento de bloco é a unidade atômica mínima de dados para o tipo de formato **wFormatTag** . O software de reprodução e gravação deve processar vários bytes de **nBlockAlign** de dados por vez. Os dados gravados e lidos de um dispositivo devem sempre ser iniciados no início de um bloco. Por exemplo, não é possível iniciar corretamente a reprodução de dados PCM no meio de um exemplo (ou seja, em um limite que não seja alinhado em bloco).

</dd> <dt>

**wBitsPerSample**
</dt> <dd>

Bits por amostra para o tipo de formato **wFormatTag** .

</dd> <dt>

**cbSize**
</dt> <dd>

Este membro é ignorado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMDSPDevice::GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getformatsupport)
</dt> <dt>

[**IMDSPStorage:: CreateStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-createstorage)
</dt> <dt>

[**IMDSPStorage:: GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getattributes)
</dt> <dt>

[**IWMDMDevice::GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport)
</dt> <dt>

[**IWMDMOperation:: getobjectattributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-getobjectattributes)
</dt> <dt>

[**IWMDMOperation:: setobjectattributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-setobjectattributes)
</dt> <dt>

[**IWMDMStorage:: GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes)
</dt> <dt>

[**Estruturas**](structures.md)
</dt> </dl>

 

 





