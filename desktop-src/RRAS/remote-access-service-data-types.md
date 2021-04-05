---
title: Tipos de dados do serviço de acesso remoto (RAS. h)
description: Os tipos de dados a seguir são usados pela API do serviço de acesso remoto.
ms.assetid: aaa7f971-9c23-4738-a386-9b7db859f6be
keywords:
- RASIPV4ADDR
- RASIPV6ADDR
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c8aa2fdae531c5aae0986d3289802565c6914fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918415"
---
# <a name="remote-access-service-data-types"></a>Tipos de dados do serviço de acesso remoto

Os tipos de dados a seguir são usados pela API do serviço de acesso remoto.


```C++
typedef in_addr RASIPV4ADDR;
typedef in6_addr RASIPV6ADDR;
```



<dl> <dt>

**RASIPV4ADDR**
</dt> <dd>

Um [**em \_ addr**](/windows/desktop/api/winsock2/ns-winsock2-in_addr) que contém um endereço IPv4.

> [!Note]  
> Com suporte no Windows Vista ou em versões posteriores do Windows.

 

</dd> <dt>

**RASIPV6ADDR**
</dt> <dd>

Um [**\_ end In6**](/previous-versions/windows/desktop/legacy/ms738560(v=vs.85)) que contém um endereço IPv6.

> [!Note]  
> Com suporte no Windows Vista ou em versões posteriores do Windows.

 

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>RAS. h</dt> </dl> |



 

