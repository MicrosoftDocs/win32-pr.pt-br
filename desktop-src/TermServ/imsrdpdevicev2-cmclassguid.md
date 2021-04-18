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
ms.openlocfilehash: 47a13a8ee706a1e6d2f512a9f6dca98928e3d8d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105757598"
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

 

 





