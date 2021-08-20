---
title: Método CancelPatch da classe Win32_RDMSVirtualDesktopCollection
description: Cancela um trabalho de provisionamento de atualização de software para as máquinas virtuais em uma coleção de áreas de trabalho virtuais.
ms.assetid: fb0d6831-5c69-4017-b725-1a5038ad69f5
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método CancelPatch
- Método CancelPatch Serviços de Área de Trabalho Remota, classe Win32_RDMSVirtualDesktopCollection
- Classe Win32_RDMSVirtualDesktopCollection Serviços de Área de Trabalho Remota, método CancelPatch
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.CancelPatch
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04e355051fd1ef9ceca2925ab3e499824dabe605670ee9e732a08809e474f5ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118131325"
---
# <a name="cancelpatch-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Método CancelPatch da classe Win32 \_ RDMSVirtualDesktopCollection

Cancela um trabalho de provisionamento de atualização de software para as máquinas virtuais em uma coleção de áreas de trabalho virtuais.

## <a name="syntax"></a>Sintaxe


```mof
uint32 CancelPatch();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

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

[**\_RDMSVirtualDesktopCollection Win32**](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





