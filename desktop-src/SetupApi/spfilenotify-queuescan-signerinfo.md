---
description: A \_ notificação SPFILENOTIFY QUEUESCAN \_ SIGNERINFO é enviada a uma rotina de retorno de chamada por SetupScanFileQueue para cada nó na subfila de cópia da fila de arquivos.
ms.assetid: 5b22e8ba-9a18-461b-bad7-b2d76f83d7f3
title: Mensagem de SPFILENOTIFY_QUEUESCAN_SIGNERINFO (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e29bf9e9c7e0ab76303d8c2fb21a0109ec60358f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922093"
---
# <a name="spfilenotify_queuescan_signerinfo-message"></a>SPFILENOTIFY \_ QUEUESCAN \_ SIGNERINFO Message

A notificação **SPFILENOTIFY \_ QUEUESCAN \_ SIGNERINFO** é enviada a uma rotina de retorno de chamada por [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) para cada nó na subfila de cópia da fila de arquivos. Isso só ocorrerá se a função **SetupScanFileQueue** for chamada especificando o sinalizador SPQ de \_ verificação \_ usar \_ retorno de chamada \_ SIGNERINFO. Disponível a partir do Windows XP.


```C++
SPFILENOTIFY_QUEUESCAN_SIGNERINFO
  Param1 = (PFILEPATHS_SIGNERINFO) Filepaths;
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Param1* 
</dt> <dd>

Ponteiro para uma estrutura de [**\_ SIGNERINFO de caminho**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_signerinfo_a) . O membro de **destino** é o nome do arquivo de destino no sistema. O membro de **origem** é o caminho esperado do arquivo de origem. O membro **Win32Error** é o erro de assinatura. As informações de assinatura serão retornadas se a rotina de retorno de chamada retornar **Win32Error**= = sem \_ erro. O membro **DigitalSigner** é o signatário digital. O membro da **versão** é a versão. O **catálogofile** é o arquivo de catálogo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

A rotina de retorno de chamada deve retornar um [código de erro do sistema](/windows/desktop/Debug/system-error-codes).

Se a rotina de retorno de chamada não retornar nenhum \_ erro, a verificação de fila continuará e retornará se a rotina retornar qualquer outro código de erro, a verificação de fila aborta e [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) retornará **false**.

> [!Note]  
> Essa notificação não é tratada pela função [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) .

 

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

[**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)
</dt> </dl>

 

