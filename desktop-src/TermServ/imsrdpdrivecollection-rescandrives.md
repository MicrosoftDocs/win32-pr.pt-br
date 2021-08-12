---
title: Método IMsRdpDriveCollection RescanDrives
description: Atualiza a lista de objetos na coleção. | Método IMsRdpDriveCollection RescanDrives
ms.assetid: 5997b76c-d130-4375-b6ff-5ea871f059cc
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método RescanDrives
- Método RescanDrives Serviços de Área de Trabalho Remota, interface IMsRdpDriveCollection
- Serviços de Área de Trabalho Remota de interface IMsRdpDriveCollection, método RescanDrives
topic_type:
- apiref
api_name:
- IMsRdpDriveCollection.RescanDrives
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2490e3879420701537cd36999ba33fde9ebfaf1e2f93d75550807e552fadacd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118606183"
---
# <a name="imsrdpdrivecollectionrescandrives-method"></a>Método IMsRdpDriveCollection:: RescanDrives

Atualiza a lista de objetos na coleção.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT RescanDrives(
  [in] VARIANT_BOOL vboolDynRedir
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*vboolDynRedir* \[ no\]
</dt> <dd>

O estado de redirecionamento padrão que será aplicado a quaisquer unidades ou dispositivos descobertos recentemente.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem sucedido, **S \_ OK** será retornado. Qualquer outro valor **HRESULT** indica que a chamada falhou.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                           |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IID \_ IMsRdpDriveCollection é definido como 7ff17599-da2c-4677-ad35-f60c04fe1585<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpDriveCollection**](imsrdpdrivecollection.md)
</dt> </dl>

 

 





