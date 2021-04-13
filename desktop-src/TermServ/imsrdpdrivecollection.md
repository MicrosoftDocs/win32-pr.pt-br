---
title: Interface IMsRdpDriveCollection
description: Representa uma coleção de objetos de unidade.
ms.assetid: 26926b85-021d-4678-845f-93ba62b2b4a3
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IMsRdpDriveCollection
- Serviços de Área de Trabalho Remota da interface IMsRdpDriveCollection, descrita
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
ms.openlocfilehash: e7b2588ddb0945ba1fcab8fbb4c5b9b078a1af9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455486"
---
# <a name="imsrdpdrivecollection-interface"></a>Interface IMsRdpDriveCollection

Representa uma coleção de objetos de unidade.

## <a name="members"></a>Membros

A interface **IMsRdpDriveCollection** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IMsRdpDriveCollection** também tem estes tipos de membros:

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

[Referência de Conexão Web de Área de Trabalho Remota](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**IMsRdpDrive**](imsrdpdrive.md)
</dt> </dl>

 

