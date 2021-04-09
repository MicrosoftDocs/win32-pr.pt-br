---
description: Define direitos padrão, específicos e genéricos. Esses direitos são usados nas ACEs (entradas de controle de acesso) e são os principais meios de especificar o acesso solicitado ou concedido a um objeto.
ms.assetid: f115ee54-3333-4109-8004-d71904a7a943
title: ACCESS_MASK (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d10d9e8db246c2705911cc57221400f40da014d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091521"
---
# <a name="access_mask"></a>máscara de acesso \_

O tipo de dados **\_ máscara de acesso** é um valor **DWORD** que define direitos padrão, específicos e genéricos. Esses direitos são usados nas ACEs ( [*entradas de controle de acesso*](/windows/desktop/SecGloss/a-gly) ) e são os principais meios de especificar o acesso solicitado ou concedido a um objeto.


```C++
typedef DWORD ACCESS_MASK;
typedef ACCESS_MASK* PACCESS_MASK;
```



## <a name="remarks"></a>Comentários

Os bits nesse valor são alocados da seguinte maneira.



| Bits             | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 15<br/>  | Direitos específicos. Contém a máscara de acesso específica ao tipo de objeto associado à máscara.<br/>                                                                                                                                                                                                                                                                                                                                                                                                          |
| 16 23<br/> | Direitos padrão. Contém os direitos de acesso padrão do objeto.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| 24<br/>    | Acesso à segurança do sistema (**\_ \_ segurança do sistema de acesso**). Ele é usado para indicar acesso a uma SACL ( [*lista de controle de acesso*](/windows/desktop/SecGloss/s-gly) ) do sistema. Esse tipo de acesso requer que o processo de chamada tenha o privilégio **\_ \_ nome de segurança de se** (gerenciar auditoria e log de segurança). Se esse sinalizador for definido na máscara de acesso de uma ACE de acesso de auditoria (acesso bem-sucedido ou malsucedido), o acesso à SACL será auditado.<br/> |
| 25<br/>    | Máximo permitido (**máximo \_ permitido**).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| 26 27<br/> | Reservado.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| 28<br/>    | Todos genéricos (**\_ todos genéricos**).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| 29<br/>    | Execução genérica (**\_ execução genérica**).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| 30<br/>    | Gravação genérica (**\_ gravação genérica**).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| 31<br/>    | Leitura genérica (**\_ leitura genérica**).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

Os bits de direitos padrão, 16 a 23, contêm os direitos de acesso padrão do objeto e podem ser uma combinação dos seguintes sinalizadores predefinidos.



| bit           | Sinalizador                         | Significado                                                                                                                                                                                                                                  |
|---------------|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 16<br/> | **DELETE**<br/>        | Excluir acesso.<br/>                                                                                                                                                                                                                |
| 17<br/> | **controle de leitura \_**<br/> | Acesso de leitura ao proprietário, grupo e [*lista de controle de acesso discricional*](/windows/desktop/SecGloss/d-gly) (DACL) do descritor de segurança.<br/> |
| 18<br/> | **GRAVAR \_ DAC**<br/>    | Acesso de gravação à DACL.<br/>                                                                                                                                                                                                     |
| 19<br/> | **proprietário da gravação \_**<br/>  | Acesso de gravação ao proprietário.<br/>                                                                                                                                                                                                        |
| 20<br/> | **SYNCHRONIZE**<br/>   | Sincronizar o acesso.<br/>                                                                                                                                                                                                           |



 

As constantes a seguir definidas em Winnt. h representam os direitos de acesso padrão e específicos.


```C++
#define DELETE                           (0x00010000L)
#define READ_CONTROL                     (0x00020000L)
#define WRITE_DAC                        (0x00040000L)
#define WRITE_OWNER                      (0x00080000L)
#define SYNCHRONIZE                      (0x00100000L)

#define STANDARD_RIGHTS_REQUIRED         (0x000F0000L)

#define STANDARD_RIGHTS_READ             (READ_CONTROL)
#define STANDARD_RIGHTS_WRITE            (READ_CONTROL)
#define STANDARD_RIGHTS_EXECUTE          (READ_CONTROL)

#define STANDARD_RIGHTS_ALL              (0x001F0000L)

#define SPECIFIC_RIGHTS_ALL              (0x0000FFFFL)
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                   |
| parâmetro<br/>                   | <dl> <dt>Winnt. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Controle de acesso](access-control.md)
</dt> <dt>

[Estruturas de controle de acesso básicas](authorization-structures.md)
</dt> <dt>

[Direitos de acesso e máscaras de acesso](access-rights-and-access-masks.md)
</dt> <dt>

[**\_mapeamento genérico**](/windows/desktop/api/Winnt/ns-winnt-generic_mapping)
</dt> </dl>

 

