---
title: Propriedade IMsRdpDeviceV2 CmClassGuid
description: Contém o GUID da classe de instalação do Configuration Manager para o dispositivo.
ms.assetid: 29ebe2ca-d669-4cc1-8cc1-33490fbb9497
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade CmClassGuid
- Propriedade CmClassGuid Serviços de Área de Trabalho Remota, interface IMsRdpDeviceV2
- Serviços de Área de Trabalho Remota de interface IMsRdpDeviceV2, Propriedade CmClassGuid
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.CmClassGuid
- IMsRdpDeviceV2.get_CmClassGuid
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 372d30ad6dc906b421a6f4a125d3f6fddb88addead17ea27f43369ceee758465
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099386"
---
# <a name="imsrdpdevicev2cmclassguid-property"></a>Propriedade IMsRdpDeviceV2:: CmClassGuid

Contém o GUID da classe de instalação do Configuration Manager para o dispositivo.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_CmClassGuid(
  [out, retval] BSTR *pCmClassGuid
);
```



## <a name="property-value"></a>Valor da propriedade

O GUID da classe de instalação do Configuration Manager para o dispositivo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 com SP1<br/>                                                          |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2 com SP1<br/>                                             |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpDeviceV2 é definido como 5fb94466-7661-42a8-98b7-01904c11668f<br/>      |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpDeviceV2**](imsrdpdevicev2.md)
</dt> </dl>

 

 





