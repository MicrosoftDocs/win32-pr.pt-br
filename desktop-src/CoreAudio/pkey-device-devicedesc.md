---
description: A propriedade PKEY do \_ dispositivo \_ DeviceDesc contém a descrição do dispositivo do ponto de extremidade (por exemplo, &\# 0034; Alto-falantes&\# 0034;).
ms.assetid: 23715497-a74d-4dab-aade-c7779fe80aa6
title: PKEY_Device_DeviceDesc (Functiondiscoverykeys \_ devpkey. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5eb68f874979e660fec0cd563db9bcaceb7d5b74
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826102"
---
# <a name="pkey_device_devicedesc"></a>PKEY \_ dispositivo \_ DeviceDesc

A propriedade **PKEY do \_ dispositivo \_ DeviceDesc** contém a descrição do dispositivo do ponto de extremidade (por exemplo, "alto-falantes").

O membro **VT** da estrutura **PROPVARIANT** é definido como VT \_ LPWSTR.

O membro **pwszVal** da estrutura **PROPVARIANT** aponta para uma cadeia de caracteres largos terminada em nulo que contém a descrição do dispositivo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                        |
| parâmetro<br/>                   | <dl> <dt>Functiondiscoverykeys \_ devpkey. h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Propriedades de áudio de núcleo](core-audio-properties.md)
</dt> <dt>

[Propriedades do Dispositivo](device-properties.md)
</dt> </dl>

 

 




