---
title: Propriedade IMsRdpDriveV2 DriveLetterIndex
description: Contém o índice da letra da unidade.
ms.assetid: 9091d1c4-b97e-4e4c-9563-5a0b881ec250
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade DriveLetterIndex
- Propriedade DriveLetterIndex Serviços de Área de Trabalho Remota, interface IMsRdpDriveV2
- Serviços de Área de Trabalho Remota de interface IMsRdpDriveV2, Propriedade DriveLetterIndex
topic_type:
- apiref
api_name:
- IMsRdpDriveV2.DriveLetterIndex
- IMsRdpDriveV2.get_DriveLetterIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39284a94950935e2d273483db871a9b08f7daf36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919203"
---
# <a name="imsrdpdrivev2driveletterindex-property"></a>IMsRdpDriveV2: Propriedade riveLetterIndex de:D

Contém o índice da letra da unidade.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_DriveLetterIndex(
  [out, retval] ULONG *pDriveLetterIndex
);
```



## <a name="property-value"></a>Valor da propriedade

O índice da letra da unidade. 0 = "A", 1 = "B" e assim por diante.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 com SP1<br/>                                                          |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/>                                                      |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpDriveV2**](imsrdpdrivev2.md)
</dt> </dl>

 

 





