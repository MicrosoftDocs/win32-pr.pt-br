---
title: Propriedade IMsRdpClientShell IsRemoteProgramClientInstalled
description: Recupera se o cliente Conexão de Área de Trabalho Remota (RDC) dá suporte Windows do RemoteApp server 2008 R2.
ms.assetid: ce2fec74-c567-48e1-91d6-655c539d1fb9
ms.tgt_platform: multiple
keywords:
- Propriedade IsRemoteProgramClientInstalled Serviços de Área de Trabalho Remota
- Propriedade IsRemoteProgramClientInstalled Serviços de Área de Trabalho Remota , interface IMsRdpClientShell
- Interface IMsRdpClientShell Serviços de Área de Trabalho Remota , propriedade IsRemoteProgramClientInstalled
topic_type:
- apiref
api_name:
- IMsRdpClientShell.IsRemoteProgramClientInstalled
- IMsRdpClientShell.get_IsRemoteProgramClientInstalled
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3073bb9a9e5890ff7a6a46bb9ea0c03964bf54f1c91550dbb2746385a11fa809
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118129759"
---
# <a name="imsrdpclientshellisremoteprogramclientinstalled-property"></a>Propriedade IMsRdpClientShell::IsRemoteProgramClientInstalled

Recupera se o cliente Conexão de Área de Trabalho Remota (RDC) dá suporte Windows do RemoteApp server 2008 R2.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_IsRemoteProgramClientInstalled(
  [out] VARIANT_BOOL *pbClientInstalled
);
```



## <a name="property-value"></a>Valor da propriedade

Recupera se o cliente Conexão de Área de Trabalho Remota (RDC) dá suporte à funcionalidade remoteApp.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClientShell é definido como d012ae6d-c19a-4bfe-b367-201f8911f134<br/>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClientShell**](imsrdpclientshell.md)
</dt> </dl>

 

 





