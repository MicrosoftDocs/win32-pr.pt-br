---
description: Representa o tipo de informação na estrutura de \_ informações do conjunto de CPU do sistema \_ \_ .
ms.assetid: B42CB8E8-0010-4B11-AB0D-6D196DCCC90A
title: Enumeração de CPU_SET_INFORMATION_TYPE (Processthreadapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPU_SET_INFORMATION_TYPE
api_type:
- HeaderDef
api_location:
- Processthreadapi.h
ms.openlocfilehash: 0283275856e8e68bf983aaeb9a7660a5a0a6bf59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759613"
---
# <a name="cpu_set_information_type-enumeration"></a>\_Enumeração de \_ tipo de informação de conjunto de CPU \_

Representa o tipo de informação na estrutura [**de \_ \_ \_ informações do conjunto de CPU do sistema**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information) .

## <a name="syntax"></a>Syntax


```C++
typedef enum _CPU_SET_INFORMATION_TYPE { 
  CpuSetInformation
} CPU_SET_INFORMATION_TYPE, *PCPU_SET_INFORMATION_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="CpuSetInformation"></span><span id="cpusetinformation"></span><span id="CPUSETINFORMATION"></span>**CpuSetInformation**
</dt> <dd>

A estrutura contém informações de conjunto de CPU.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                                                       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2016\]<br/>                                                              |
| parâmetro<br/>                   | <dl> <dt>Processthreadsapi. h (incluir Windows. h)</dt> </dl> |



 

 




