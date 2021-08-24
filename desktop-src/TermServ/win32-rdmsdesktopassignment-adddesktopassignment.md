---
title: Método AddDesktopAssignment da classe Win32_RDMSDesktopAssignment classe
description: Adicione uma atribuição de área de trabalho.
ms.assetid: 3690f70e-d0c3-444a-a0b7-cec6994eb3b8
ms.tgt_platform: multiple
keywords:
- Método AddDesktopAssignment Serviços de Área de Trabalho Remota
- Método AddDesktopAssignment Serviços de Área de Trabalho Remota , Win32_RDMSDesktopAssignment classe
- Win32_RDMSDesktopAssignment classe Serviços de Área de Trabalho Remota , método AddDesktopAssignment
topic_type:
- apiref
api_name:
- Win32_RDMSDesktopAssignment.AddDesktopAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c0d8145318cfd749772d2dcf417b71c6a1862ee31ec363957554e06b3aa6257
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868216"
---
# <a name="adddesktopassignment-method-of-the-win32_rdmsdesktopassignment-class"></a>Método AddDesktopAssignment da classe \_ Win32 RDMSDesktopAssignment

Adicionar uma atribuição de área de trabalho

## <a name="syntax"></a>Sintaxe


```mof
uint32 AddDesktopAssignment(
  [in] string CollectionAlias,
  [in] string DesktopName,
  [in] string UserDomain,
  [in] string UserName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*CollectionAlias* \[ Em\]
</dt> <dd>

O alias da coleção.

</dd> <dt>

*DesktopName* \[ Em\]
</dt> <dd>

O nome da área de trabalho.

</dd> <dt>

*UserDomain* \[ Em\]
</dt> <dd>

O nome de domínio da conta de usuário.

</dd> <dt>

*UserName* \[ Em\]
</dt> <dd>

O nome da conta de usuário.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                              |
| Namespace<br/>                | Raiz \\ cimv2 \\ rdms<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ RDMSDesktopAssignment**](win32-rdmsdesktopassignment.md)
</dt> </dl>

 

 





