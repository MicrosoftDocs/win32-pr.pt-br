---
description: A propriedade \_ OEMFormat PKEY AudioEngine especifica o formato padrão do dispositivo usado para \_ renderizar ou capturar um fluxo. Os valores são preenchidos pelo OEM em um arquivo .inf.
ms.assetid: 3a199ecf-642c-491c-a565-f0083783d180
title: PKEY_AudioEngine_OEMFormat (Mmdeviceapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ed43ee7a607bc7b97e6ce521c3c1f76356380d27b3471d16dde27cd021838e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053636"
---
# <a name="pkey_audioengine_oemformat"></a>PKEY \_ AudioEngine \_ OEMFormat

A propriedade \_ OEMFormat PKEY AudioEngine especifica o formato padrão do dispositivo usado para \_ renderizar ou capturar um fluxo. Os valores são preenchidos pelo OEM em um arquivo .inf.

O **membro vt** da estrutura **PROPVARIANT** é definido como \_ BLOB de VT.

O **membro de blob** da **estrutura PROPVARIANT** é uma estrutura do tipo **BLOB** que contém dois membros. **Blob.cbSize membro é** um **DWORD** que especifica o número de bytes na descrição do formato. **Blob.pBlobData de** membro aponta para uma estrutura **WAVEFORMATEX** que contém a descrição do formato. Para obter mais informações sobre o BLOB, consulte a documentação Windows SDK. Para obter mais informações sobre **WAVEFORMATEX,** consulte a documentação Windows DDK.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Mmdeviceapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades do ponto de extremidade de áudio**](audio-endpoint-properties.md)
</dt> <dt>

[Propriedades de áudio principais](core-audio-properties.md)
</dt> </dl>

 

 




