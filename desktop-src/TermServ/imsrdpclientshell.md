---
title: Interface IMsRdpClientShell
description: As configurações de cliente Conexão de Área de Trabalho Remota (RDC) que são usadas para iniciar o cliente do Acesso via Web à Área de Trabalho Remota (RD Acesso via Web) ou de outros portais da Web.
ms.assetid: 05ca2e90-656a-40a3-a438-29d7985e9feb
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IMsRdpClientShell
- Serviços de Área de Trabalho Remota da interface IMsRdpClientShell, descrita
topic_type:
- apiref
api_name:
- IMsRdpClientShell
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f8593a890097bbfaf6d9c9876bb56d92794ce204f38f349c72beb73b8d28403
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119621026"
---
# <a name="imsrdpclientshell-interface"></a>Interface IMsRdpClientShell

As configurações de cliente Conexão de Área de Trabalho Remota (RDC) que são usadas para iniciar o cliente do Acesso via Web à Área de Trabalho Remota (RD Acesso via Web) ou de outros portais da Web.

## <a name="members"></a>Membros

A interface **IMsRdpClientShell** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IMsRdpClientShell** também tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A interface **IMsRdpClientShell** tem esses métodos.



| Método                                                     | Descrição                                                  |
|:-----------------------------------------------------------|:-------------------------------------------------------------|
| [**GetRdpProperty**](/previous-versions/windows/desktop/legacy/aa381303(v=vs.85)) | Recupera uma única propriedade RDP.<br/>                  |
| [**Iniciar**](imsrdpclientshell-launch.md)                 | Inicia o conteúdo do arquivo remoto no portal da Web.<br/> |
| [**SetRdpProperty**](/previous-versions/windows/desktop/legacy/aa381312(v=vs.85)) | Define uma única propriedade RDP.<br/>                       |



 

### <a name="properties"></a>Propriedades

A interface **IMsRdpClientShell** tem essas propriedades.



| Propriedade                                                                                              | Tipo de acesso           | Descrição                                                                                               |
|:------------------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [**IsRemoteProgramClientInstalled**](imsrdpclientshell-isremoteprogramclientinstalled.md)<br/> | Somente leitura<br/>  | Recupera se o cliente de Conexão de Área de Trabalho Remota (RDC) dá suporte à funcionalidade do RemoteApp.<br/> |
| [**Públicomode**](imsrdpclientshell-publicmode.md)<br/>                                         | Leitura/gravação<br/> | Recupera se o modo público está habilitado.<br/>                                                      |
| [**RdpFileContents**](imsrdpclientshell-rdpfilecontents.md)<br/>                               | Leitura/gravação<br/> | Versão de fluxo do arquivo de configuração de RDP.<br/>                                                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClientShell é definido como d012ae6d-c19a-4bfe-B367-201f8911f134<br/>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[Referência de Conexão Web de Área de Trabalho Remota](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

