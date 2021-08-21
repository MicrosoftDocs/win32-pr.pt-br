---
title: Interface IMsRdpDrive
description: Contém informações sobre um objeto de unidade.
ms.assetid: 25e76657-a898-4581-a866-d66008540f50
ms.tgt_platform: multiple
keywords:
- Interface IMsRdpDrive Serviços de Área de Trabalho Remota
- Interface IMsRdpDrive Serviços de Área de Trabalho Remota , descrita
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
ms.openlocfilehash: 3efccf0459375e23375b3ac40067bcbd3965ed7f6c0b51ddb60f6362fb419688
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000726"
---
# <a name="imsrdpdrive-interface"></a>Interface IMsRdpDrive

Contém informações sobre um objeto de unidade.

## <a name="members"></a>Membros

A interface **IMsRdpDrive** herda da interface [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **O IMsRdpDrive** também tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A interface **IMsRdpDrive** tem essas propriedades.



| Propriedade                                                            | Tipo de acesso           | Descrição                                              |
|:--------------------------------------------------------------------|:----------------------|:---------------------------------------------------------|
| [**Nome**](imsrdpdrive-name.md)<br/>                         | Somente leitura<br/>  | Recupera o nome da unidade.<br/>              |
| [**RedirectionState**](imsrdpdrive-redirectionstate.md)<br/> | Leitura/gravação<br/> | Indica o estado de redirecionamento da unidade.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID IMsRdpDrive é definido como \_ d28b5458-f694-47a8-8e61-40356a767e46<br/>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Conexão Web de Área de Trabalho Remota referência](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**IMsRdpDriveCollection**](imsrdpdrivecollection.md)
</dt> </dl>

 

