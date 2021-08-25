---
title: Método SchedulePatch da classe Win32_RDMSVirtualDesktopCollection
description: Agenda um trabalho de provisionamento de atualização de software que instala atualizações de software nas máquinas virtuais em uma coleção de áreas de trabalho virtuais.
ms.assetid: 780d5709-9e7d-41d9-a4d0-b5d021615655
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SchedulePatch
- Método SchedulePatch Serviços de Área de Trabalho Remota, classe Win32_RDMSVirtualDesktopCollection
- Classe Win32_RDMSVirtualDesktopCollection Serviços de Área de Trabalho Remota, método SchedulePatch
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.SchedulePatch
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb29eb42f0f1d13ff1bf234c6fb41b8f414317a4b723af9a6d215cf25fa2ec95
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865506"
---
# <a name="schedulepatch-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Método SchedulePatch da classe Win32 \_ RDMSVirtualDesktopCollection

Agenda um trabalho de provisionamento de atualização de software que instala atualizações de software nas máquinas virtuais em uma coleção de áreas de trabalho virtuais.

## <a name="syntax"></a>Sintaxe


```mof
uint32 SchedulePatch(
  [in] DATETIME StartTime,
  [in] DATETIME ForceLogOffTime,
  [in] string   JobInputXml
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*StartTime* \[ no\]
</dt> <dd>

> [!Note]  
> O sistema não fará logoff dos usuários das máquinas virtuais até o tempo especificado no parâmetro *ForceLogOffTime* .

 

A data e a hora para instalar as atualizações.

</dd> <dt>

*ForceLogOffTime* \[ no\]
</dt> <dd>

A data e a hora em que o sistema fará logoff dos usuários das máquinas virtuais.

</dd> <dt>

*JobInputXml* \[ no\]
</dt> <dd>

Uma cadeia de caracteres formatada em XML que contém as informações do trabalho de atualização de software.

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

 

 





