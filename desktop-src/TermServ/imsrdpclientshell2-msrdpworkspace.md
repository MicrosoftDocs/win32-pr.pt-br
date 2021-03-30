---
title: Propriedade IMsRdpClientShell2 MsRdpWorkspace
description: Recupera um ponteiro para a interface IMsRdpWorkspace, que é usada para gerenciar Conexão de RemoteApp e Área de Trabalho credenciais e conexões.
ms.assetid: 5d505ce0-18cf-4e38-b1b8-026303f7069b
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade MsRdpWorkspace
- Propriedade MsRdpWorkspace Serviços de Área de Trabalho Remota, interface IMsRdpClientShell2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientShell2, Propriedade MsRdpWorkspace
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
ms.openlocfilehash: 91eadd3f1b422e3da96d5bcd3a5178a2a0b0eb52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644874"
---
# <a name="imsrdpclientshell2msrdpworkspace-property"></a>Propriedade IMsRdpClientShell2:: MsRdpWorkspace

Recupera um ponteiro para a interface [**IMsRdpWorkspace**](imsrdpworkspace.md) , que é usada para gerenciar conexão de RemoteApp e área de trabalho credenciais e conexões.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_MsRdpWorkspace(
  [out, retval] IMsRdpWorkspace **pVal
);
```



## <a name="property-value"></a>Valor da propriedade

O endereço de um ponteiro para a interface [**IMsRdpWorkspace**](imsrdpworkspace.md) .

## <a name="remarks"></a>Comentários

A interface [**IMsRdpWorkspace**](imsrdpworkspace.md) não é exposta como uma interface personalizada. Ele só pode ser acessado por meio de métodos [IDispatch](/windows/desktop/com/exposing-methods-through-idispatch) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7<br/>                                                                          |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/>                                                             |
| DLL<br/>                      | <dl> <dt>MsRdpWebAccess.dll</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**IMsRdpClientShell2**](imsrdpclientshell2.md)
</dt> </dl>

 

