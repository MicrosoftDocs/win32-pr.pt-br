---
description: A \_ notificação SPFILENOTIFY TARGETEXISTS será enviada para a rotina de retorno de chamada se o arquivo a ser copiado tiver sido colocado na fila com o \_ sinalizador de cópia NoOverwrite do SP \_ e esse arquivo já existir no diretório de destino.
ms.assetid: 5c6e0c59-0340-4aa6-94db-8d9a5d202758
title: Mensagem de SPFILENOTIFY_TARGETEXISTS (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1d0c1a1ffba520789113b0dc78246657a4fe324
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104370748"
---
# <a name="spfilenotify_targetexists-message"></a>\_Mensagem SPFILENOTIFY TARGETEXISTS

A notificação **SPFILENOTIFY \_ TARGETEXISTS** será enviada para a rotina de retorno de chamada se o arquivo a ser copiado tiver sido colocado na fila com o \_ sinalizador de cópia NoOverwrite do SP \_ e esse arquivo já existir no diretório de destino. Ele pode ser enviado para a rotina de retorno de chamada isoladamente ou combinada, usando o operador OR, com as notificações [**SPFILENOTIFY \_ LANGMISMATCH**](spfilenotify-langmismatch.md) e/ou [**SPFILENOTIFY \_ TARGETNEWER**](spfilenotify-targetnewer.md) .


```C++
SPFILENOTIFY_TARGETEXISTS
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Param1* 
</dt> <dd>

Ponteiro para uma estrutura [**FILEpaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) que contém informações sobre os caminhos para os arquivos de origem e de destino.

</dd> <dt>

*Param2* 
</dt> <dd>

Esse parâmetro não é usado a menos que essa notificação seja combinada, usando o operador OR, com a notificação [**SPFILENOTIFY \_ LANGMISMATCH**](spfilenotify-langmismatch.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

A rotina de retorno de chamada deve retornar um dos valores a seguir.



| Código de retorno                                                                          | Descrição                                            |
|--------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>**TRUE**</dt> </dl>  | Substitua o arquivo no diretório de destino.<br/> |
| <dl> <dt>**FOR**</dt> </dl> | Ignore a operação de cópia atual.<br/>            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Setupapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral](overview.md)
</dt> <dt>

[Notificações](notifications.md)
</dt> <dt>

[**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> <dt>

[**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)
</dt> <dt>

[**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)
</dt> <dt>

[**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> </dl>

 

 




