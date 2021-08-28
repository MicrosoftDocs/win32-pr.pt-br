---
title: Interface IMsRdpDriveCollection
description: Representa uma coleção de objetos de unidade.
ms.assetid: 26926b85-021d-4678-845f-93ba62b2b4a3
ms.tgt_platform: multiple
keywords:
- Interface IMsRdpDriveCollection Serviços de Área de Trabalho Remota
- Interface IMsRdpDriveCollection Serviços de Área de Trabalho Remota , descrita
topic_type:
- apiref
api_name:
- IMsRdpDriveCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d9f85a491da97fe0093d9b02e8ceda59c3562f237d8678323078e2613250f28
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125626"
---
# <a name="imsrdpdrivecollection-interface"></a>Interface IMsRdpDriveCollection

Representa uma coleção de objetos de unidade.

## <a name="members"></a>Membros

A interface **IMsRdpDriveCollection** herda da interface [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IMsRdpDriveCollection** também tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A interface **IMsRdpDriveCollection** tem esses métodos.



| Método                                                     | Descrição                                                 |
|:-----------------------------------------------------------|:------------------------------------------------------------|
| [**RescanDrives**](imsrdpdrivecollection-rescandrives.md) | Atualiza a lista de objetos na coleção.<br/> |



 

### <a name="properties"></a>Propriedades

A interface **IMsRdpDriveCollection** tem essas propriedades.



| Propriedade                                                              | Tipo de acesso          | Descrição                                                  |
|:----------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------|
| [**DriveByIndex**](imsrdpdrivecollection-drivebyindex.md)<br/> | Somente leitura<br/> | Recupera a unidade no índice especificado.<br/>       |
| [**DriveCount**](imsrdpdrivecollection-drivecount.md)<br/>     | Somente leitura<br/> | Recupera a contagem de objetos na coleção.<br/> |



 

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

[Conexão Web de Área de Trabalho Remota referência](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**IMsRdpDrive**](imsrdpdrive.md)
</dt> </dl>

 

