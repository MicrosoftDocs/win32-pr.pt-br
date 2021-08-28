---
description: A \_ notificação SPFILENOTIFY QUEUESCAN \_ ex é enviada para uma rotina de retorno de chamada por SetupScanFileQueue para cada nó na subfila de cópia da fila de arquivos.
ms.assetid: 293e63f9-9567-4ea7-b7e5-e5046c8a704b
title: Mensagem de SPFILENOTIFY_QUEUESCAN_EX (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95d151a5172918e7a7dcb13e8c480aae82da0a3ec1ffb38d26db29d63143cbc1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992586"
---
# <a name="spfilenotify_queuescan_ex-message"></a>\_Mensagem SPFILENOTIFY QUEUESCAN \_ ex

A notificação **SPFILENOTIFY \_ QUEUESCAN \_ ex** é enviada para uma rotina de retorno de chamada por [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) para cada nó na subfila de cópia da fila de arquivos. Isso só ocorrerá se a função **SetupScanFileQueue** tiver sido chamada especificando o sinalizador SPQ de \_ verificação \_ usar \_ CALLBACKEX.


```C++
SPFILENOTIFY_QUEUESCAN_EX
  Param1 = (PFILEPATHS) Filepaths;
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Param1* 
</dt> <dd>

Ponteiro para uma estrutura [**FILEpaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) . O membro de **destino** é o nome do arquivo de destino no sistema. O membro de **origem** é o caminho esperado do arquivo de origem. O membro **Win32Error** é o erro de assinatura.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

A rotina de retorno de chamada deve retornar um [código de erro do sistema](/windows/desktop/Debug/system-error-codes).

Se a rotina de retorno de chamada não retornar nenhum \_ erro, a verificação da fila continuará. Se a rotina retornar qualquer outro código de erro, a verificação de fila aborta e [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) retorna false.

> [!Note]  
> Essa notificação não é tratada pela função [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) .

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Setupapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral](overview.md)
</dt> <dt>

[Notificações](notifications.md)
</dt> <dt>

[**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)
</dt> </dl>

 

