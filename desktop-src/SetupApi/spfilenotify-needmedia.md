---
description: A \_ notificação SPFILENOTIFY NEEDMEDIA é enviada para a rotina de retorno de chamada quando uma nova mídia ou um novo arquivo de gabinete é necessário.
ms.assetid: 6a7947de-1bb3-46e0-9334-405684e58e98
title: Mensagem de SPFILENOTIFY_NEEDMEDIA (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6b856a95f3c2e200d1d81cfa00c05ef592c1759
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105762885"
---
# <a name="spfilenotify_needmedia-message"></a>\_Mensagem SPFILENOTIFY NEEDMEDIA

A notificação **SPFILENOTIFY \_ NEEDMEDIA** é enviada para a rotina de retorno de chamada quando uma nova mídia ou um novo arquivo de gabinete é necessário.


```C++
SPFILENOTIFY_NEEDMEDIA
  Param1 = (UINT) SourceMediaInfo;
  Param2 = (UINT) NewPathInfo;
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Param1* 
</dt> <dd>

Ponteiro para uma estrutura de [**\_ mídia de origem**](/windows/desktop/api/Setupapi/ns-setupapi-source_media_a) .

</dd> <dt>

*Param2* 
</dt> <dd>

Ponteiro para uma matriz de caracteres para armazenar novas informações de caminho fornecidas pelo usuário. O tamanho do buffer é uma matriz **TCHAR** de máximo de \_ elementos Path. As informações de caminho retornadas pelo seu aplicativo de instalação não devem exceder esse tamanho.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

A rotina de retorno de chamada deve retornar um dos seguintes.



| Código de retorno                                                                                    | Descrição                                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**FILEOP \_ NEWPATH**</dt> </dl> | A mídia está presente e o arquivo solicitado está disponível no caminho especificado no buffer apontado por *param2*.<br/>                                                                                         |
| <dl> <dt>**FILEOP \_ ignorar**</dt> </dl>    | Ignorar o arquivo solicitado<br/>                                                                                                                                                                                      |
| <dl> <dt>**\_anular FILEOP**</dt> </dl>   | Anular o processamento da fila. A função [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) retorna **false**. GetLastError retorna informações de erro estendidas, como erro \_ cancelado se o usuário cancelou.<br/> |
| <dl> <dt>**FILEOP-DOIT**</dt> </dl>     | A mídia está disponível.<br/>                                                                                                                                                                                      |



 

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

[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> <dt>

[**mídia de origem \_**](/windows/desktop/api/Setupapi/ns-setupapi-source_media_a)
</dt> </dl>

 

 




