---
title: Tipos de dados do serviço de acesso remoto (RAS. h)
description: Os tipos de dados a seguir são usados pela API do serviço de acesso remoto.
ms.assetid: aaa7f971-9c23-4738-a386-9b7db859f6be
keywords:
- RASIPV4ADDR
- RASIPV6ADDR
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26df8b8336b9b96ec338a79ed846519fb8a0ca019e6dd5996b9ac17087faa371
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028246"
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
> com suporte no Windows Vista ou em versões posteriores do Windows.

 

</dd> <dt>

**RASIPV6ADDR**
</dt> <dd>

Um [**\_ end In6**](/previous-versions/windows/desktop/legacy/ms738560(v=vs.85)) que contém um endereço IPv6.

> [!Note]  
> com suporte no Windows Vista ou em versões posteriores do Windows.

 

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>RAS. h</dt> </dl> |



 

