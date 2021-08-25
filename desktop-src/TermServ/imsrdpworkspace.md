---
title: Interface IMsRdpWorkspace
description: Expõe métodos que gerenciam credenciais de Conexão de RemoteApp e Área de Trabalho e conexões.
ms.assetid: cddcdfc2-b30a-4d00-84c2-ad036ab6288f
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
ms.openlocfilehash: 1489690632b0ef1bf05a529d84ed5c96afb6c442c82744f964c9a89e9286299d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125526"
---
# <a name="imsrdpworkspace-interface"></a>Interface IMsRdpWorkspace

Expõe métodos que gerenciam credenciais de Conexão de RemoteApp e Área de Trabalho e conexões. Essa interface é implementada pelo controle de Acesso via Web de Serviços de Área de Trabalho Remota. Esse controle é um wrapper em volta do cliente de Conexão de Área de Trabalho Remota (MsTscAx.dll) e o proxy de tempo de execução de conexões de RemoteApp e área de trabalho (Tswbprxy.exe).

## <a name="members"></a>Membros

A interface **IMsRdpWorkspace** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IMsRdpWorkspace** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IMsRdpWorkspace** tem esses métodos.



| Método                                                                                   | Descrição                                                                                                                                                           |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ClearWorkspaceCredential**](/previous-versions/windows/desktop/legacy/ee351596(v=vs.85))             | Exclui as credenciais de usuário associadas à ID de conexão especificada.<br/>                                                                                  |
| [**DisconnectWorkspace**](/previous-versions/windows/desktop/legacy/ee351597(v=vs.85))                       | Desconecta todas as conexões existentes associadas à ID de conexão especificada e exclui as credenciais de usuário correspondentes do repositório de credenciais.<br/> |
| [**IsWorkspaceCredentialSpecified**](/previous-versions/windows/desktop/legacy/ee351598(v=vs.85)) | Determina se as credenciais do usuário existem para a ID de conexão especificada.<br/>                                                                                 |
| [**IsWorkspaceSSOEnabled**](/previous-versions/windows/desktop/legacy/ee351599(v=vs.85))                   | Determina se o SSO (logon único) está habilitado para Conexão de RemoteApp e Área de Trabalho.<br/>                                                                   |
| [**Onautenticado**](/previous-versions/windows/desktop/legacy/ee351600(v=vs.85))                               | Marca a autenticação de credenciais do usuário para a ID de conexão e, posteriormente, mostra a notificação de conexão na área de notificação da barra de tarefas. <br/>     |
| [**StartWorkspace**](/previous-versions/windows/desktop/legacy/ee351601(v=vs.85))                                 | Associa credenciais de usuário e certificados com uma ID de conexão.<br/>                                                                                         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7<br/>                                                                          |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/>                                                             |
| DLL<br/>                      | <dl> <dt>MsRdpWebAccess.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpWorkspace é definido como 145D0621-04CF-4FC2-A766-A81A9069CDF8<br/>            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClientShell2**](imsrdpclientshell2.md)
</dt> </dl>

 

