---
title: Interface IMsRdpClientShell2
description: Expõe propriedades que iniciam o cliente Conexão de Área de Trabalho Remota de Acesso via Web à Área de Trabalho Remota (RD Acesso via Web) ou de outros portais da Web.
ms.assetid: cc8ef78f-b7d6-42cd-bb67-8a8e1f33be08
ms.tgt_platform: multiple
keywords:
- Interface IMsRdpClientShell2 Serviços de Área de Trabalho Remota
- Interface IMsRdpClientShell2 Serviços de Área de Trabalho Remota , descrita
topic_type:
- apiref
api_name:
- IMsRdpClientShell2
api_location:
- MsRdpWebAccess.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 561e9a63e631ca88575f4b632def5e47b29b68da414d48af95d42e757dcb2da6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138649"
---
# <a name="imsrdpclientshell2-interface"></a>Interface IMsRdpClientShell2

Expõe propriedades que iniciam o cliente Conexão de Área de Trabalho Remota de Acesso via Web à Área de Trabalho Remota (RD Acesso via Web) ou de outros portais da Web.

Essa interface é implementada pelo controle Serviços de Área de Trabalho Remota Acesso via Web, que é um wrapper em torno do cliente Conexão de Área de Trabalho Remota (MsTscAx.dll) e do proxy de runtime de Conexões de Área de Trabalho e RemoteApp (Tswbprxy.exe).

## <a name="members"></a>Membros

A interface **IMsRdpClientShell2** herda de **IMsRdpClientShell**. **IMsRdpClientShell2** também tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A interface **IMsRdpClientShell2** tem essas propriedades.



| Propriedade                                                                               | Tipo de acesso          | Descrição                                                                                                                                                                       |
|:---------------------------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MsRdpWorkspace**](imsrdpclientshell2-msrdpworkspace.md)<br/>                 | Somente leitura<br/> | Recupera um ponteiro para a interface [**IMsRdpWorkspace,**](imsrdpworkspace.md) que é usada para gerenciar Conexão de RemoteApp e Área de Trabalho credenciais e conexões.<br/> |
| [**SecuredSettingsEnabled**](imsrdpclientshell2-securedsettingsenabled.md)<br/> | Somente leitura<br/> | Recupera um valor que indica se a página da Web atual está em uma zona de segurança Internet Explorer URL confiável.<br/>                                                      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7<br/>                                                                          |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/>                                                             |
| DLL<br/>                      | <dl> <dt>MsRdpWebAccess.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpWorkspace**](imsrdpworkspace.md)
</dt> </dl>

 

 





