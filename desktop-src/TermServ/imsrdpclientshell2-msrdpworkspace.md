---
title: Propriedade MsRdpClientShell2 MsRdpWorkspace
description: Recupera um ponteiro para a interface IMsRdpWorkspace, que é usada para gerenciar Conexão de RemoteApp e Área de Trabalho credenciais e conexões.
ms.assetid: 5d505ce0-18cf-4e38-b1b8-026303f7069b
ms.tgt_platform: multiple
keywords:
- Propriedade MsRdpWorkspace Serviços de Área de Trabalho Remota
- Propriedade MsRdpWorkspace Serviços de Área de Trabalho Remota , interface IMsRdpClientShell2
- Interface IMsRdpClientShell2 Serviços de Área de Trabalho Remota , propriedade MsRdpWorkspace
topic_type:
- apiref
api_name:
- IMsRdpClientShell2.MsRdpWorkspace
- IMsRdpClientShell2.get_MsRdpWorkspace
api_location:
- MsRdpWebAccess.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6470f51ccae2efb6dc3d44a7b0a2a0310ad4230861d7d86262f34fd312fcfc5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118854430"
---
# <a name="imsrdpclientshell2msrdpworkspace-property"></a>Propriedade IMsRdpClientShell2::MsRdpWorkspace

Recupera um ponteiro para a interface [**IMsRdpWorkspace,**](imsrdpworkspace.md) que é usada para gerenciar Conexão de RemoteApp e Área de Trabalho credenciais e conexões.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_MsRdpWorkspace(
  [out, retval] IMsRdpWorkspace **pVal
);
```



## <a name="property-value"></a>Valor da propriedade

O endereço de um ponteiro para a interface [**IMsRdpWorkspace.**](imsrdpworkspace.md)

## <a name="remarks"></a>Comentários

A interface [**IMsRdpWorkspace**](imsrdpworkspace.md) não é exposta como uma interface personalizada. Ele só pode ser acessado por meio de métodos [IDispatch.](/windows/desktop/com/exposing-methods-through-idispatch)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7<br/>                                                                          |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/>                                                             |
| DLL<br/>                      | <dl> <dt>MsRdpWebAccess.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClientShell2**](imsrdpclientshell2.md)
</dt> </dl>

 

