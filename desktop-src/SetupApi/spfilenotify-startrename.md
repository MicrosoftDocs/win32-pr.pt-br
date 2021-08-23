---
description: A \_ notificação SPFILENOTIFY STARTRENAME é enviada para a função de retorno de chamada quando a fila inicia uma operação de renomeação de arquivo.
ms.assetid: 005c1840-6aa9-4e94-bfe7-6a9d53735fd9
title: Mensagem de SPFILENOTIFY_STARTRENAME (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ec75c84841adf5cb8a187e8d8431f031af74b31f33af7a87e46225b1e9a3464
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739416"
---
# <a name="spfilenotify_startrename-message"></a>\_Mensagem SPFILENOTIFY STARTRENAME

A notificação **SPFILENOTIFY \_ STARTRENAME** é enviada para a função de retorno de chamada quando a fila inicia uma operação de renomeação de arquivo.


```C++
SPFILENOTIFY_STARTRENAME
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) Operation;
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Param1* 
</dt> <dd>

Ponteiro para uma estrutura [**FILEpaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .

</dd> <dt>

*Param2* 
</dt> <dd>

Sempre tem o valor FILEOP \_ Rename.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

A rotina de retorno de chamada deve retornar um dos valores a seguir.



| Código de retorno                                                                                  | Descrição                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_anular FILEOP**</dt> </dl> | Anule a confirmação da fila. A rotina de retorno de chamada deve chamar [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) para indicar o motivo do encerramento. [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) retorna **false** e uma chamada subsequente para [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retorna o código de erro definido pela rotina de retorno de chamada durante a chamada para **SetLastError**.<br/> |
| <dl> <dt>**FILEOP \_ doit**</dt> </dl>  | Execute a operação de cópia de arquivo.<br/>                                                                                                                                                                                                                                                                                                                                     |
| <dl> <dt>**FILEOP \_ ignorar**</dt> </dl>  | Ignore a operação de cópia atual.<br/>                                                                                                                                                                                                                                                                                                                                     |



 

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

[**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

