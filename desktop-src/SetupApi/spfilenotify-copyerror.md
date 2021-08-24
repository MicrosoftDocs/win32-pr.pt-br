---
description: A \_ notificação SPFILENOTIFY COPYERROR será enviada para a rotina de retorno de chamada se ocorrer um erro durante uma operação de cópia de arquivo.
ms.assetid: d6096954-c6a5-44d4-a358-c1320c50730a
title: Mensagem de SPFILENOTIFY_COPYERROR (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80160af9d8053a90c1848d397da6bbb9bf41f2793756e1d5491fb0d6f5e39abc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665146"
---
# <a name="spfilenotify_copyerror-message"></a>\_Mensagem SPFILENOTIFY COPYERROR

A notificação **SPFILENOTIFY \_ COPYERROR** será enviada para a rotina de retorno de chamada se ocorrer um erro durante uma operação de cópia de arquivo.


```C++
SPFILENOTIFY_COPYERROR
  Param1 = (UINT_PTR) FilePathInfo;
  Param2 = (UINT_PTR) ReturnBuffer;
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Param1* 
</dt> <dd>

Ponteiro para uma estrutura [**FILEpaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .

</dd> <dt>

*Param2* 
</dt> <dd>

Ponteiro para um buffer, de tamanho máximo de \_ caracteres de caminho, que armazena novas informações de caminho especificadas pelo usuário.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O retorno de chamada deve retornar um dos valores a seguir.



| Código de retorno                                                                                    | Descrição                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_anular FILEOP**</dt> </dl>   | O processamento da fila deve ser cancelado. [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) retorna zero e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retorna informações de erro ESTENDIdas, como erro \_ cancelado (se o usuário cancelou) ou erro \_ não \_ há \_ memória suficiente.<br/> |
| <dl> <dt>**FILEOP \_ NEWPATH**</dt> </dl> | Repita a operação de cópia usando o caminho que a função de retorno de chamada colocou no buffer apontado pelo parâmetro *param2* . A rotina de retorno de chamada deve garantir que o caminho não exceda o tamanho do buffer de uma matriz TCHAR de \_ elementos de caminho máximo.<br/>                |
| <dl> <dt>**repetição de FILEOP \_**</dt> </dl>   | O usuário está tentando a operação de cópia novamente.<br/>                                                                                                                                                                                                                   |
| <dl> <dt>**FILEOP \_ ignorar**</dt> </dl>    | O usuário está ignorando a operação de cópia de arquivo.<br/>                                                                                                                                                                                                                      |



 

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

 

