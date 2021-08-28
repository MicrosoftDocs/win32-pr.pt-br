---
title: Interface IMsRdpWorkspace2
description: Expõe um método que associa Conexão de RemoteApp e Área de Trabalho credenciais a uma conexão.
ms.assetid: 7E09AF14-2D6C-4D6E-8033-C691D9DC8057
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IMsRdpWorkspace
- Serviços de Área de Trabalho Remota da interface IMsRdpWorkspace, descrita
topic_type:
- apiref
api_name:
- IMsRdpWorkspace
api_location:
- MsRdpWebAccess.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38b869d3ffc83d9a4b8f3d51df0b7b14658ec3f1c561797a62dee3a574bf2803
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125516"
---
# <a name="imsrdpworkspace2-interface"></a>Interface IMsRdpWorkspace2

Expõe um método que associa Conexão de RemoteApp e Área de Trabalho credenciais a uma conexão. Essa interface é implementada pelo controle de Acesso via Web de Serviços de Área de Trabalho Remota. Esse controle é um wrapper em volta do cliente de Conexão de Área de Trabalho Remota (MsTscAx.dll) e o proxy de tempo de execução de conexões de RemoteApp e área de trabalho (Tswbprxy.exe).

## <a name="members"></a>Membros

A interface **IMsRdpWorkspace** herda de [**IMsRdpWorkspace**](imsrdpworkspace.md). **IMsRdpWorkspace2** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IMsRdpWorkspace** tem esses métodos.



| Método                                                        | Descrição                                                                    |
|:--------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**StartWorkspaceEx**](/previous-versions/windows/desktop/legacy/dn123459(v=vs.85)) | Associa credenciais de usuário e certificados com uma ID de conexão. <br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                          |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                                |
| DLL<br/>                      | <dl> <dt>MsRdpWebAccess.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpWorkspace2 é definido como 145D0622-04CF-4FC3-A776-A82A9169CDF8<br/>           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClientShell2**](imsrdpclientshell2.md)
</dt> <dt>

[**IMsRdpWorkspace**](imsrdpworkspace.md)
</dt> </dl>

 

