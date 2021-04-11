---
description: A \_ notificação SPFILENOTIFY NEEDNEWCABINET é enviada pelo SetupIterateCabinet para indicar que o arquivo atual continua em outro gabinete.
ms.assetid: 01207429-11fb-4e2c-89ba-54321992e953
title: Mensagem de SPFILENOTIFY_NEEDNEWCABINET (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3187d48b89579c329a4d0163e151824288462344
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171663"
---
# <a name="spfilenotify_neednewcabinet-message"></a>\_Mensagem SPFILENOTIFY NEEDNEWCABINET

A notificação **SPFILENOTIFY \_ NEEDNEWCABINET** é enviada pelo [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) para indicar que o arquivo atual continua em outro gabinete. Sua rotina de retorno de chamada pode então chamar [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska)ou criar sua própria caixa de diálogo para solicitar que o usuário insira o próximo disco.


```C++
SPFILENOTIFY_NEEDNEWCABINET
  Param1 = (UINT) CabinetInfo;
  Param2 = (UINT) NewPath;
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Param1* 
</dt> <dd>

Ponteiro para uma estrutura de [**\_ informações de gabinete**](/windows/desktop/api/Setupapi/ns-setupapi-cabinet_info_a) que contém informações sobre o gabinete e o arquivo a ser extraído.

</dd> <dt>

*Param2* 
</dt> <dd>

Se o retorno de chamada não retornar nenhum \_ erro, esse parâmetro será um ponteiro para uma cadeia de caracteres terminada em nulo. Se a cadeia de caracteres não estiver vazia, ela especificará um novo caminho para o gabinete.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sua rotina deve retornar um dos valores a seguir.



| Código de retorno                                                                                 | Descrição                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SEM \_ erros**</dt> </dl>    | Nenhum erro foi encontrado, continue processando o gabinete.<br/>                                                                                                                                                                        |
| <dl> <dt>**Erro \_* do XXX * * *</dt> </dl> | Ocorreu um erro do tipo especificado. A função [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) retornará **false** e o código de erro especificado será retornado por uma chamada para [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).<br/> |



 

> [!Note]  
> Não há rotina de retorno de chamada de gabinete padrão; Portanto, você deve fornecer uma rotina de retorno de chamada para manipular as notificações enviadas pelo [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).

 

## <a name="remarks"></a>Comentários

Se a rotina de retorno de chamada não retornar nenhum \_ erro, o [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) verificará o buffer apontado por *param2*. Se o buffer não estiver vazio, ele conterá um novo caminho de origem. Se o buffer estiver vazio, o caminho de origem será considerado inalterado.

Sua função de retorno de chamada deve garantir que o gabinete esteja acessível antes de retornar, chamando a função [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska) , se for necessário inserir uma nova mídia.

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

[**informações do gabinete \_**](/windows/desktop/api/Setupapi/ns-setupapi-cabinet_info_a)
</dt> <dt>

[**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)
</dt> </dl>

 

