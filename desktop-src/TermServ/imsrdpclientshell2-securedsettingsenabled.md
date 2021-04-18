---
title: Propriedade IMsRdpClientShell2 SecuredSettingsEnabled
description: Recupera um valor que indica se a página da Web atual está em uma zona de segurança de URL confiável do Internet Explorer.
ms.assetid: 51988473-fff7-4574-bd6e-d05ca452da54
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade SecuredSettingsEnabled
- Propriedade SecuredSettingsEnabled Serviços de Área de Trabalho Remota, interface IMsRdpClientShell2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientShell2, Propriedade SecuredSettingsEnabled
topic_type:
- apiref
api_name:
- IMsRdpClientShell2.SecuredSettingsEnabled
- IMsRdpClientShell2.get_SecuredSettingsEnabled
api_location:
- MsRdpWebAccess.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1009759051207db7e6b8d741c1dd91e3de1ffc36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753327"
---
# <a name="imsrdpclientshell2securedsettingsenabled-property"></a>Propriedade IMsRdpClientShell2:: SecuredSettingsEnabled

Recupera um valor que indica se a página da Web atual está em uma zona de segurança de URL confiável do Internet Explorer.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_SecuredSettingsEnabled(
  [out, retval] BOOL *pSecuredSettingsEnabled
);
```



## <a name="property-value"></a>Valor da propriedade

Um ponteiro para um valor booliano que indica se a página da Web atual está em uma zona de segurança de URL confiável do Internet Explorer.

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

 

 





