---
description: A \_ notificação SPFILENOTIFY FILEINCABINET é enviada a uma rotina de retorno de chamada por SetupIterateCabinet para cada arquivo encontrado no gabinete. A rotina de retorno de chamada deve retornar um valor que indica se deseja extrair o arquivo.
ms.assetid: c6d89759-c0d4-4741-b992-43eaa0dc4f01
title: Mensagem de SPFILENOTIFY_FILEINCABINET (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 496db3cef814f2bf366f4cb6f91132efe01a2406
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756361"
---
# <a name="spfilenotify_fileincabinet-message"></a>\_Mensagem SPFILENOTIFY FILEINCABINET

A notificação **SPFILENOTIFY \_ FILEINCABINET** é enviada a uma rotina de retorno de chamada por [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) para cada arquivo encontrado no gabinete. A rotina de retorno de chamada deve retornar um valor que indica se deseja extrair o arquivo.


```C++
SPFILENOTIFY_FILEINCABINET
  Param1 = (UINT) FileInCabinetInfo;
  Param2 = (UINT) CabinetFile;
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Param1* 
</dt> <dd>

Ponteiro para um [**arquivo \_ na estrutura de \_ \_ informações do gabinete**](/windows/desktop/api/Setupapi/ns-setupapi-file_in_cabinet_info_a) que contém informações sobre o arquivo no gabinete.

</dd> <dt>

*Param2* 
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que contém o nome do arquivo de gabinete.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sua rotina de retorno de chamada deve retornar um dos itens a seguir.



| Código de retorno                                                                                 | Descrição                                  |
|---------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**FILEOP \_ ignorar**</dt> </dl> | Não Extraia o arquivo, pule-o.<br/> |
| <dl> <dt>**FILEOP \_ doit**</dt> </dl> | Extraia o arquivo.<br/>                 |



 

Se a rotina de retorno de chamada retornar FILEOP \_ doit, o nome a ser usado para o arquivo extraído deverá ser especificado no membro **FullTargetName** do [**arquivo \_ na estrutura de \_ \_ informações do gabinete**](/windows/desktop/api/Setupapi/ns-setupapi-file_in_cabinet_info_a) passada para a rotina em *param1*.

> [!Note]  
> Não há rotina de retorno de chamada de gabinete padrão. O aplicativo de instalação deve fornecer uma rotina de retorno de chamada para manipular as notificações enviadas pelo [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).

 

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

[**ARQUIVO \_ em \_ informações do gabinete \_**](/windows/desktop/api/Setupapi/ns-setupapi-file_in_cabinet_info_a)
</dt> <dt>

[**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)
</dt> </dl>

 

 




