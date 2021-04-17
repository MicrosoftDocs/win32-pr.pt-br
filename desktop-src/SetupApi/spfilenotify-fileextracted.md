---
description: A \_ notificação FILEextraíted do SPFILENOTIFY é enviada a uma rotina de retorno de chamada por SetupIterateCabinet para indicar que um arquivo foi extraído do gabinete ou que uma extração falhou e o processamento do gabinete foi cancelado.
ms.assetid: 70ffe06c-e72d-4bb8-a13c-e2946ff72fa6
title: Mensagem de SPFILENOTIFY_FILEEXTRACTED (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efdd66c7f218e632ba817d00a6e6c9447052e350
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749443"
---
# <a name="spfilenotify_fileextracted-message"></a>SPFILENOTIFY \_ extracçãod Message

A **notificação \_ fileextraíted do SPFILENOTIFY** é enviada a uma rotina de retorno de chamada por [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) para indicar que um arquivo foi extraído do gabinete ou que uma extração falhou e o processamento do gabinete foi cancelado.


```C++
SPFILENOTIFY_FILEEXTRACTED
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Param1* 
</dt> <dd>

Ponteiro [**para uma estrutura de arquivo**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) de dados que contém informações de caminho para o arquivos extraídos. O membro **SourceFile** da estrutura **filePaths** contém o caminho de origem completo do gabinete. O membro **TargetFile** fornece o caminho de destino completo do arquivo a ser instalado no sistema.

</dd> <dt>

*Param2* 
</dt> <dd>

Não utilizado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

A rotina de retorno de chamada do gabinete deve retornar um dos valores a seguir.



| Código de retorno                                                                               | Descrição                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SEM \_ erros**</dt> </dl>  | Nenhum erro foi encontrado, continue processando o gabinete.<br/>                                                                                                                                |
| <dl> <dt>**ERRO \_ xxx**</dt> </dl> | Ocorreu um erro do tipo especificado. [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) retornará zero. [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará o código de erro especificado.<br/> |



 

> [!Note]  
> Não há uma rotina de retorno de chamada de gabinete padrão fornecida com a API de instalação. O aplicativo de instalação deve fornecer uma rotina de retorno de chamada para manipular as notificações enviadas pela função [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) .

 

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

[**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)
</dt> </dl>

 

