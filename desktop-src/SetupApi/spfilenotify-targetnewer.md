---
description: A notificação de SPFILENOTIFY \_ TARGETNEWER será enviada para a rotina de retorno de chamada se o arquivo a ser copiado tiver sido colocado na fila com a cópia do SP \_ \_ mais recente ou a \_ cópia \_ do SP Force os \_ sinalizadores mais recentes especificados e uma versão mais recente do arquivo já existir no diretório de destino.
ms.assetid: 93bcd610-f75d-4900-841c-f67946af5c4a
title: Mensagem de SPFILENOTIFY_TARGETNEWER (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c432515a5ce0e9a1eddb8ea6e92f7376c318b4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748379"
---
# <a name="spfilenotify_targetnewer-message"></a>\_Mensagem SPFILENOTIFY TARGETNEWER

A notificação de **SPFILENOTIFY \_ TARGETNEWER** será enviada para a rotina de retorno de chamada se o arquivo a ser copiado tiver sido colocado na fila com a cópia do SP \_ \_ mais recente ou a \_ cópia \_ do SP Force os \_ sinalizadores mais recentes especificados e uma versão mais recente do arquivo já existir no diretório de destino. Ele pode ser enviado para a rotina de retorno de chamada sozinha ou vinculada com [**SPFILENOTIFY \_ LANGMISMATCH**](spfilenotify-langmismatch.md) e/ou [**SPFILENOTIFY \_ TARGETEXISTS**](spfilenotify-targetexists.md).


```C++
SPFILENOTIFY_TARGETNEWER
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Param1* 
</dt> <dd>

Ponteiro para uma estrutura [**FILEpaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) que contém informações sobre os caminhos para arquivos de origem e de destino.

</dd> <dt>

*Param2* 
</dt> <dd>

Esse parâmetro não é usado a menos que essa notificação seja combinada, usando o operador OR, com [**SPFILENOTIFY \_ LANGMISMATCH**](spfilenotify-langmismatch.md).

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

 

 




