---
description: A \_ Propriedade PKEY AudioEngine \_ OEMFormat especifica o formato padrão do dispositivo que é usado para renderizar ou capturar um fluxo. Os valores são preenchidos pelo OEM em um arquivo. inf.
ms.assetid: 3a199ecf-642c-491c-a565-f0083783d180
title: PKEY_AudioEngine_OEMFormat (Mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be7ed65ae8a7bd717992b13dc7b5517a5725b241
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089510"
---
# <a name="pkey_audioengine_oemformat"></a>PKEY \_ AudioEngine \_ OEMFormat

A \_ Propriedade PKEY AudioEngine \_ OEMFormat especifica o formato padrão do dispositivo que é usado para renderizar ou capturar um fluxo. Os valores são preenchidos pelo OEM em um arquivo. inf.

O membro **VT** da estrutura **PROPVARIANT** é definido como blob VT \_ .

O membro de **blob** da estrutura **PROPVARIANT** é uma estrutura do tipo **blob** que contém dois membros. Member **BLOB. cbSize** é um **DWORD** que especifica o número de bytes na descrição do formato. Member **BLOB. pBlobData** aponta para uma estrutura **WAVEFORMATEX** que contém a descrição do formato. Para obter mais informações sobre BLOB, consulte a documentação do SDK do Windows. Para obter mais informações sobre o **WAVEFORMATEX**, consulte a documentação do Windows DDK.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                               |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Mmdeviceapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades do ponto de extremidade de áudio**](audio-endpoint-properties.md)
</dt> <dt>

[Propriedades de áudio de núcleo](core-audio-properties.md)
</dt> </dl>

 

 




