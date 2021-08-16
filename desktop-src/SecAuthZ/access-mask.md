---
description: Define direitos padrão, específicos e genéricos. Esses direitos são usados em ACEs (entradas de controle de acesso) e são o principal meio de especificar o acesso solicitado ou concedido a um objeto.
ms.assetid: f115ee54-3333-4109-8004-d71904a7a943
title: ACCESS_MASK (Winnt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d13378b44d17bedd818efd5fc84310b304a2f683a3331237e8cca208be8de810
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785461"
---
# <a name="access_mask"></a>MÁSCARA DE \_ ACESSO

O **tipo de dados ACCESS \_ MASK** é um **valor DWORD** que define direitos padrão, específicos e genéricos. Esses direitos são usados [*em*](/windows/desktop/SecGloss/a-gly) ACEs (entradas de controle de acesso) e são o principal meio de especificar o acesso solicitado ou concedido a um objeto.


```C++
typedef DWORD ACCESS_MASK;
typedef ACCESS_MASK* PACCESS_MASK;
```



## <a name="remarks"></a>Comentários

Os bits nesse valor são alocados da seguinte forma.



| Bits             | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 15<br/>  | Direitos específicos. Contém a máscara de acesso específica ao tipo de objeto associado à máscara.<br/>                                                                                                                                                                                                                                                                                                                                                                                                          |
| 16 23<br/> | Direitos padrão. Contém os direitos de acesso padrão do objeto.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| 24<br/>    | Segurança do sistema de acesso (**ACCESS \_ SYSTEM \_ SECURITY**). Ele é usado para indicar o acesso a uma SACL (lista de controle de acesso [*do sistema).*](/windows/desktop/SecGloss/s-gly) Esse tipo de acesso requer que o processo de chamada tenha **o privilégio ES SECURITY \_ \_ NAME** (Gerenciar log de auditoria e segurança). Se esse sinalizador for definido na máscara de acesso de uma ACE de acesso de auditoria (acesso bem-sucedido ou sem êxito), o acesso SACL será auditado.<br/> |
| 25<br/>    | Máximo permitido (**MÁXIMO \_ PERMITIDO).**<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| 26 27<br/> | Reservado.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| 28<br/>    | Generic all (**GENERIC \_ ALL**).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| 29<br/>    | Execução genérica (**GENERIC \_ EXECUTE**).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| 30<br/>    | Gravação genérica (**GRAVAÇÃO \_ GENÉRICA**).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| 31<br/>    | Leitura genérica (**GENERIC \_ READ**).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

Os bits de direitos padrão, de 16 a 23, contêm os direitos de acesso padrão do objeto e podem ser uma combinação dos sinalizadores predefinidos a seguir.



| bit           | Sinalizador                         | Significado                                                                                                                                                                                                                                  |
|---------------|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 16<br/> | **DELETE**<br/>        | Excluir acesso.<br/>                                                                                                                                                                                                                |
| 17<br/> | **CONTROLE \_ DE LEITURA**<br/> | Acesso de leitura ao proprietário, grupo e DACL [*(lista*](/windows/desktop/SecGloss/d-gly) de controle de acesso discricionário) do descritor de segurança.<br/> |
| 18<br/> | **ESCREVER \_ DAC**<br/>    | Acesso de gravação à DACL.<br/>                                                                                                                                                                                                     |
| 19<br/> | **PROPRIETÁRIO \_ DA GRAVAÇÃO**<br/>  | Acesso de gravação ao proprietário.<br/>                                                                                                                                                                                                        |
| 20<br/> | **Sincronizar**<br/>   | Sincronizar o acesso.<br/>                                                                                                                                                                                                           |



 

As constantes a seguir definidas em Winnt.h representam os direitos de acesso específicos e padrão.


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
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                   |
| Cabeçalho<br/>                   | <dl> <dt>Winnt.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Controle de acesso](access-control.md)
</dt> <dt>

[Estruturas básicas de controle de acesso](authorization-structures.md)
</dt> <dt>

[Direitos de acesso e máscaras de acesso](access-rights-and-access-masks.md)
</dt> <dt>

[**MAPEAMENTO \_ GENÉRICO**](/windows/desktop/api/Winnt/ns-winnt-generic_mapping)
</dt> </dl>

 

