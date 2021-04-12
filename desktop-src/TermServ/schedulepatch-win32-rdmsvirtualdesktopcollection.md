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
ms.openlocfilehash: 7d9585e3d13ea1f02115506741c153d62c33fcc8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455048"
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

[**\_RDMSVirtualDesktopCollection Win32**](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





