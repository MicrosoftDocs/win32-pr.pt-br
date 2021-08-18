---
title: Interface IBackgroundCopyJob (Deliveryoptimization.h)
description: Use a interface IBackgroundCopyJob para adicionar arquivos ao trabalho, definir o nível de prioridade do trabalho, determinar o estado do trabalho e iniciar e parar o trabalho.
ms.assetid: 0D1EAC8D-0013-4FBC-A07F-14CD5D709549
keywords:
- Interface IBackgroundCopyJob
- Interface IBackgroundCopyJob, descrita
topic_type:
- apiref
api_name:
- IBackgroundCopyJob
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 27febd08519a06f7ad452882cf0725fed209e0306182ba336343049936795acf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543022"
---
# <a name="ibackgroundcopyjob-interface"></a>Interface IBackgroundCopyJob

Use a interface [**IBackgroundCopyJob**](https://www.bing.com/search?q=**IBackgroundCopyJob**) para adicionar arquivos ao trabalho, definir o nível de prioridade do trabalho, determinar o estado do trabalho e iniciar e parar o trabalho.

Para criar um trabalho, chame o [**método IBackgroundCopyManager::CreateJob.**](ibackgroundcopymanager-createjob.md) Para obter um ponteiro de interface [**IBackgroundCopyJob**](https://www.bing.com/search?q=**IBackgroundCopyJob**) para um trabalho existente, chame o [**método IBackgroundCopyManager::GetJob.**](ibackgroundcopymanager-getjob.md)

## <a name="members"></a>Membros

A interface **IBackgroundCopyJob** herda da interface [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IBackgroundCopyJob** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IBackgroundCopyJob** tem esses métodos.



| Método                                                                  | Descrição                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Cancelar**](ibackgroundcopyjob-cancel.md)                             | Cancela o trabalho e remove arquivos temporários do cliente.<br/>                                                                                                                                                           |
| [**Concluir**](ibackgroundcopyjob-complete.md)                         | Encerra o trabalho e salva os arquivos transferidos no cliente.<br/>                                                                                                                                                            |
| [**EnumFiles**](ibackgroundcopyjob-enumfiles.md)                       | Retorna um ponteiro de interface para um objeto enumerador que você usa para enumerar os arquivos no trabalho.<br/>                                                                                                                   |
| [**Getdisplayname**](ibackgroundcopyjob-getdisplayname.md)             | Recupera o nome de exibição que identifica o trabalho.<br/>                                                                                                                                                                    |
| [**Geterror**](ibackgroundcopyjob-geterror.md)                         | Recupera um ponteiro de interface para o objeto de erro depois que ocorre um erro.<br/>                                                                                                                                              |
| [**Getid**](ibackgroundcopyjob-getid.md)                               | Recupera o identificador do trabalho na fila.<br/>                                                                                                                                                                      |
| [**GetNoProgressTimeout**](ibackgroundcopyjob-getnoprogresstimeout.md) | Recupera o período de tempo que o DO continua tentando transferir o arquivo depois de encontrar uma condição de erro transitória.<br/>                                                                                             |
| [**GetNotifyFlags**](ibackgroundcopyjob-getnotifyflags.md)             | Recupera os sinalizadores de notificação de eventos (retorno de chamada) que você definiu para seu aplicativo.<br/>                                                                                                                                   |
| [**GetNotifyInterface**](ibackgroundcopyjob-getnotifyinterface.md)     | Recupera um ponteiro para sua implementação da interface [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) (retornos de chamada).<br/>                                                                                    |
| [**Getpriority**](ibackgroundcopyjob-getpriority.md)                   | Recupera o nível de prioridade que você definiu para o trabalho.<br/>                                                                                                                                                                 |
| [**GetProgress**](ibackgroundcopyjob-getprogress.md)                   | Recupera informações de progresso relacionadas ao trabalho, como o número de bytes e arquivos transferidos para o cliente.<br/>                                                                                                           |
| [**GetState**](ibackgroundcopyjob-getstate.md)                         | Recupera o estado do trabalho.<br/>                                                                                                                                                                                        |
| [**GetTimes**](ibackgroundcopyjob-gettimes.md)                         | Recupera carimbos de data/hora para atividades relacionadas ao trabalho, como a hora em que o trabalho foi criado.<br/>                                                                                                                         |
| [**Gettype**](ibackgroundcopyjob-gettype.md)                           | Recupera o tipo de transferência que está sendo executada, como um download de arquivo.<br/>                                                                                                                                               |
| [**Retomar**](ibackgroundcopyjob-resume.md)                             | Inicia um novo trabalho ou reinicia um trabalho suspenso.<br/>                                                                                                                                                                          |
| [**SetNoProgressTimeout**](ibackgroundcopyjob-setnoprogresstimeout.md) | Especifica o período de tempo que o DO continua tentando transferir o arquivo depois de encontrar uma condição de erro transitória.<br/>                                                                                             |
| [**SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md)             | Especifica o tipo de notificação de evento a ser recebido.<br/>                                                                                                                                                                   |
| [**SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md)     | Especifica um ponteiro para a implementação da interface [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) (retornos de chamada). A interface recebe notificação com base nos sinalizadores de notificação de eventos definidos.<br/> |
| [**Setpriority**](ibackgroundcopyjob-setpriority.md)                   | Especifica a prioridade do trabalho em relação a outros trabalhos na fila de transferência.<br/>                                                                                                                                        |
| [**Suspend**](ibackgroundcopyjob-suspend.md)                           | Pausa o trabalho.<br/>                                                                                                                                                                                                        |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1709 somente para \[ aplicativos da área de trabalho\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Servidor, versão 1709 somente \[ aplicativos da área de trabalho\]<br/>                                       |
| Cabeçalho<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob é definido como 37668D37-507E-4160-9316-26306D150B12<br/>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IBackgroundCopyFile**](ibackgroundcopyfile.md)
</dt> <dt>

[**IBackgroundCopyManager**](ibackgroundcopymanager.md)
</dt> </dl>

 

