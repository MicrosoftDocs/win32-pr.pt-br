---
description: A notificação SPFILENOTIFY NEEDNEWCABINET é enviada por SetupIterateCabinet para indicar que o \_ arquivo atual continua em outro gabinete.
ms.assetid: 01207429-11fb-4e2c-89ba-54321992e953
title: SPFILENOTIFY_NEEDNEWCABINET mensagem (Setupapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a78950c5557973e5e4e7ab696be11c14c5122884542ae67e8d5c7b4c1a134cf5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117964420"
---
# <a name="spfilenotify_neednewcabinet-message"></a>Mensagem SPFILENOTIFY \_ NEEDNEWCABINET

A **notificação SPFILENOTIFY \_ NEEDNEWCABINET** é enviada por [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) para indicar que o arquivo atual continua em outro gabinete. Sua rotina de retorno de chamada pode chamar [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska)ou criar sua própria caixa de diálogo para solicitar que o usuário insira o próximo disco.


```C++
SPFILENOTIFY_NEEDNEWCABINET
  Param1 = (UINT) CabinetInfo;
  Param2 = (UINT) NewPath;
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Param1* 
</dt> <dd>

Ponteiro para uma [**estrutura DE \_ INFORMAÇÕES DE**](/windows/desktop/api/Setupapi/ns-setupapi-cabinet_info_a) GABINETE que contém informações sobre o gabinete e o arquivo a ser extraído.

</dd> <dt>

*Param2* 
</dt> <dd>

Se o retorno de chamada retornar NENHUM \_ ERRO, esse parâmetro será um ponteiro para uma cadeia de caracteres terminada em nulo. Se a cadeia de caracteres não estiver vazia, ela especificará um novo caminho para o gabinete.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sua rotina deve retornar um dos valores a seguir.



| Código de retorno                                                                                 | Descrição                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NENHUM \_ ERRO**</dt> </dl>    | Nenhum erro foi encontrado, continue processando o gabinete.<br/>                                                                                                                                                                        |
| <dl> <dt>**ERRO \_* XXX***</dt> </dl> | Ocorreu um erro do tipo especificado. A [**função SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) retornará **FALSE** e o código de erro especificado será retornado por uma chamada para [**GetLastError.**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)<br/> |



 

> [!Note]  
> Não há nenhuma rotina de retorno de chamada de gabinete padrão; portanto, você deve fornecer uma rotina de retorno de chamada para lidar com as notificações enviadas por [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).

 

## <a name="remarks"></a>Comentários

Se a rotina de retorno de chamada retornar NENHUM \_ ERRO, [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) verificará o buffer apontado *por Param2.* Se o buffer não estiver vazio, ele conterá um novo caminho de origem. Se o buffer estiver vazio, o caminho de origem será presumido como inalterado.

Sua função de retorno de chamada deve garantir que o gabinete seja acessível antes de retornar, chamando a [**função SetupPromptForDisk,**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska) se a nova mídia precisar ser inserida.

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

[**INFORMAÇÕES DE \_ GABINETE**](/windows/desktop/api/Setupapi/ns-setupapi-cabinet_info_a)
</dt> <dt>

[**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)
</dt> </dl>

 

