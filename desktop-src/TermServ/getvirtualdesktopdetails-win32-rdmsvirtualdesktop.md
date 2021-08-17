---
title: Método GetVirtualDesktopDetails da Win32_RDMSVirtualDesktop classe
description: Recupera as informações adicionais sobre a área de trabalho virtual.
ms.assetid: 487e3a02-4306-4639-a44e-5b9519163a67
ms.tgt_platform: multiple
keywords:
- Método GetVirtualDesktopDetails Serviços de Área de Trabalho Remota
- Método GetVirtualDesktopDetails Serviços de Área de Trabalho Remota , Win32_RDMSVirtualDesktop classe
- Win32_RDMSVirtualDesktop classe Serviços de Área de Trabalho Remota , método GetVirtualDesktopDetails
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.GetVirtualDesktopDetails
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6ca1b552147623822ae007ca17abf8e4eaebfb149f5e80ac4760719f1ef7168
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059484"
---
# <a name="getvirtualdesktopdetails-method-of-the-win32_rdmsvirtualdesktop-class"></a>Método GetVirtualDesktopDetails da classe \_ Win32 RDMSVirtualDesktop

Recupera as informações adicionais sobre a área de trabalho virtual.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetVirtualDesktopDetails(
  [out] uint32  RAMSizeInMB,
  [out] boolean RemoteFXEnabled,
  [out] string  OSVersion
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*RAMSizeInMB* \[ out\]
</dt> <dd>

Recebe a quantidade de RAM atribuída à área de trabalho virtual, em bytes.

</dd> <dt>

*RemoteFXEnabled* \[ out\]
</dt> <dd>

Recebe um valor que indica se RemoteFX está habilitado na área de trabalho virtual. **TRUE** se RemoteFX estiver habilitado; caso contrário, **FALSE.**

</dd> <dt>

*OSVersion* \[ out\]
</dt> <dd>

Recebe a versão do sistema operacional da área de trabalho virtual.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                              |
| Namespace<br/>                | \\rdms CIMv2 \\ raiz<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ RDMSVirtualDesktop**](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





