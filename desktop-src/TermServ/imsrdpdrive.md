---
title: Interface IMsRdpDrive
description: Contém informações sobre um objeto de unidade.
ms.assetid: 25e76657-a898-4581-a866-d66008540f50
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IMsRdpDrive
- Serviços de Área de Trabalho Remota da interface IMsRdpDrive, descrita
topic_type:
- apiref
api_name:
- IMsRdpDrive
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 032e62ca54d6adccce9b27c8f7e95160c800759b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644272"
---
# <a name="imsrdpdrive-interface"></a>Interface IMsRdpDrive

Contém informações sobre um objeto de unidade.

## <a name="members"></a>Membros

A interface **IMsRdpDrive** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IMsRdpDrive** também tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A interface **IMsRdpDrive** tem essas propriedades.



| Propriedade                                                            | Tipo de acesso           | Description                                              |
|:--------------------------------------------------------------------|:----------------------|:---------------------------------------------------------|
| [**Name**](imsrdpdrive-name.md)<br/>                         | Somente leitura<br/>  | Recupera o nome da unidade.<br/>              |
| [**De redirecionamento**](imsrdpdrive-redirectionstate.md)<br/> | Leitura/gravação<br/> | Indica o estado de redirecionamento da unidade.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpDrive é definido como d28b5458-f694-47a8-8e61-40356a767e46<br/>         |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Referência de Conexão Web de Área de Trabalho Remota](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**IMsRdpDriveCollection**](imsrdpdrivecollection.md)
</dt> </dl>

 

