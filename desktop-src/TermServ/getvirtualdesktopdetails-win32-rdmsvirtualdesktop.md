---
title: Método GetVirtualDesktopDetails da classe Win32_RDMSVirtualDesktop
description: Recupera as informações adicionais sobre a área de trabalho virtual.
ms.assetid: 487e3a02-4306-4639-a44e-5b9519163a67
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método GetVirtualDesktopDetails
- Método GetVirtualDesktopDetails Serviços de Área de Trabalho Remota, classe Win32_RDMSVirtualDesktop
- Classe Win32_RDMSVirtualDesktop Serviços de Área de Trabalho Remota, método GetVirtualDesktopDetails
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
ms.openlocfilehash: f7382a7ea10b3e557cd7317bdf1ddb0c4bcea55d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455389"
---
# <a name="getvirtualdesktopdetails-method-of-the-win32_rdmsvirtualdesktop-class"></a>Método GetVirtualDesktopDetails da classe Win32 \_ RDMSVirtualDesktop

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

*RAMSizeInMB* \[ fora\]
</dt> <dd>

Recebe a quantidade de RAM atribuída à área de trabalho virtual, em bytes.

</dd> <dt>

*RemoteFXEnabled* \[ fora\]
</dt> <dd>

Recebe um valor que indica se o RemoteFX está habilitado na área de trabalho virtual. **True** se o RemoteFX estiver habilitado; caso contrário, **false**.

</dd> <dt>

*OSVersion* \[ fora\]
</dt> <dd>

Recebe a versão do sistema operacional da área de trabalho virtual.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                              |
| Namespace<br/>                | \\RDMs CIMv2 \\ raiz<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_RDMSVirtualDesktop Win32**](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





