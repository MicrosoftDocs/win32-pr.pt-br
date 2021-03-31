---
title: Interface IMsRdpClientShell2
description: Expõe as propriedades que iniciam o cliente do Conexão de Área de Trabalho Remota do Acesso via Web à Área de Trabalho Remota (RD Acesso via Web) ou de outros portais da Web.
ms.assetid: cc8ef78f-b7d6-42cd-bb67-8a8e1f33be08
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IMsRdpClientShell2
- Serviços de Área de Trabalho Remota da interface IMsRdpClientShell2, descrita
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
ms.openlocfilehash: bb93fd938602b195f60877be884dbe0bd458a598
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644412"
---
# <a name="imsrdpclientshell2-interface"></a>Interface IMsRdpClientShell2

Expõe as propriedades que iniciam o cliente do Conexão de Área de Trabalho Remota do Acesso via Web à Área de Trabalho Remota (RD Acesso via Web) ou de outros portais da Web.

Essa interface é implementada pelo controle de Acesso via Web de Serviços de Área de Trabalho Remota, que é um wrapper em volta do cliente Conexão de Área de Trabalho Remota (MsTscAx.dll) e o proxy de tempo de execução de conexões do RemoteApp e da área de trabalho (Tswbprxy.exe).

## <a name="members"></a>Membros

A interface **IMsRdpClientShell2** herda de **IMsRdpClientShell**. **IMsRdpClientShell2** também tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A interface **IMsRdpClientShell2** tem essas propriedades.



| Propriedade                                                                               | Tipo de acesso          | Descrição                                                                                                                                                                       |
|:---------------------------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MsRdpWorkspace**](imsrdpclientshell2-msrdpworkspace.md)<br/>                 | Somente leitura<br/> | Recupera um ponteiro para a interface [**IMsRdpWorkspace**](imsrdpworkspace.md) , que é usada para gerenciar conexão de RemoteApp e área de trabalho credenciais e conexões.<br/> |
| [**SecuredSettingsEnabled**](imsrdpclientshell2-securedsettingsenabled.md)<br/> | Somente leitura<br/> | Recupera um valor que indica se a página da Web atual está em uma zona de segurança de URL confiável do Internet Explorer.<br/>                                                      |



 

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

 

 





