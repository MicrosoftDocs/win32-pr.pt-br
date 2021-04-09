---
description: O tipo de dados de identificador do SCE \_ é um identificador opaco fornecido pelo conjunto de ferramentas de configuração de segurança. Ele é usado pelas informações de consulta do PFSCE \_ \_ e pelas funções de \_ suporte do PFSCE Set \_ info para passar informações entre o anexo e o banco de dados de segurança.
ms.assetid: 8db91e6f-b31e-40c6-a158-b4b3b00ba0c0
title: SCE_HANDLE (Scesvc. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fef21dbe03d97dfa14537d5df132ba3cb222643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090183"
---
# <a name="sce_handle"></a>identificador do SCE \_

O tipo de dados de **\_ identificador do SCE** é um identificador opaco fornecido pelo conjunto de ferramentas de configuração de segurança. Ele é usado pelas [**\_ \_ informações de consulta do PFSCE**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) e pelas funções de suporte do [**PFSCE \_ set \_ info**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) para passar informações entre o anexo e o banco de dados de segurança.


```C++
typedef PVOID SCE_HANDLE;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                |
| parâmetro<br/>                   | <dl> <dt>Scesvc. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_informações de consulta do PFSCE \_**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info)
</dt> <dt>

[**PFSCE \_ definir \_ informações**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info)
</dt> </dl>

 

