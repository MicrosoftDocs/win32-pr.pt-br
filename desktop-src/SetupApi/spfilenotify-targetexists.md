---
description: A notificação SPFILENOTIFY TARGETEXISTS será enviada para a rotina de retorno de chamada se o arquivo a ser copiado tiver sido enxuado com o sinalizador \_ SP \_ COPY NOOVERWRITE e esse arquivo já existir no diretório de \_ destino.
ms.assetid: 5c6e0c59-0340-4aa6-94db-8d9a5d202758
title: SPFILENOTIFY_TARGETEXISTS mensagem (Setupapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c51f845d7ccb41b330f6365eff269645d08e58597e7e6dd3e9acc7a7f0300c80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664736"
---
# <a name="spfilenotify_targetexists-message"></a>Mensagem SPFILENOTIFY \_ TARGETEXISTS

A **notificação SPFILENOTIFY \_ TARGETEXISTS** será enviada para a rotina de retorno de chamada se o arquivo a ser copiado tiver sido enxuado com o sinalizador SP \_ COPY NOOVERWRITE e esse arquivo já existir no diretório de \_ destino. Ele pode ser enviado para a rotina de retorno de chamada sozinho ou combinado, usando o operador OR, com as notificações [**SPFILENOTIFY \_ LANGMISMATCH**](spfilenotify-langmismatch.md) e/ou [**SPFILENOTIFY \_ TARGETNEWER.**](spfilenotify-targetnewer.md)


```C++
SPFILENOTIFY_TARGETEXISTS
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Param1* 
</dt> <dd>

Ponteiro para uma [**estrutura FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) que contém informações sobre os caminhos para os arquivos de origem e de destino.

</dd> <dt>

*Param2* 
</dt> <dd>

Esse parâmetro não é usado, a menos que essa notificação seja combinada, usando o operador OR, com a notificação [**SPFILENOTIFY \_ LANGMISMATCH.**](spfilenotify-langmismatch.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

A rotina de retorno de chamada deve retornar um dos valores a seguir.



| Código de retorno                                                                          | Descrição                                            |
|--------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>**Verdade**</dt> </dl>  | Substituir o arquivo no diretório de destino.<br/> |
| <dl> <dt>**False**</dt> </dl> | Ignore a operação de cópia atual.<br/>            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Setupapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral](overview.md)
</dt> <dt>

[Notificações](notifications.md)
</dt> <dt>

[**Filepaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
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

 

 




