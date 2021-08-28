---
title: Método getpatchproperties da classe Win32_RDMSVirtualDesktopCollection
description: Recupera as propriedades de um trabalho de provisionamento de atualização de software para as máquinas virtuais em uma coleção de áreas de trabalho virtuais.
ms.assetid: 9f228d89-0613-49c7-8169-48491c3a2d9b
ms.tgt_platform: multiple
keywords:
- Método getpatchproperties Serviços de Área de Trabalho Remota
- Método getpatchproperties Serviços de Área de Trabalho Remota, classe Win32_RDMSVirtualDesktopCollection
- Classe Win32_RDMSVirtualDesktopCollection Serviços de Área de Trabalho Remota, método getpatchproperties
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.GetPatchProperties
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 969a73e372dee430b280d4d16c267c6d8b75dda236c3ae7362d2392cb1bf8bf3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099506"
---
# <a name="getpatchproperties-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Método getpatchproperties da classe Win32 \_ RDMSVirtualDesktopCollection

Recupera as propriedades de um trabalho de provisionamento de atualização de software para as máquinas virtuais em uma coleção de áreas de trabalho virtuais.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetPatchProperties(
  [out] DATETIME StartTime,
  [out] DATETIME ForceLogOffTime,
  [out] string   JobGuid,
  [out] uint32   State
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*StartTime* \[ fora\]
</dt> <dd>

A data e a hora para instalar as atualizações.

</dd> <dt>

*ForceLogOffTime* \[ fora\]
</dt> <dd>

A data e a hora em que o sistema fará logoff dos usuários das máquinas virtuais.

</dd> <dt>

*JobGuid* \[ fora\]
</dt> <dd>

Um **GUID** que identifica exclusivamente o trabalho de provisionamento.

</dd> <dt>

*Estado* \[ fora\]
</dt> <dd>

O estado do trabalho de provisionamento.

</dd> </dl>

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

 

 





