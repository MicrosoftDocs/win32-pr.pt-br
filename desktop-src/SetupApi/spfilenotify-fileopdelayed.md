---
description: A \_ notificação SPFILENOTIFY FILEOPDELAYED é enviada por SetupInstallFileEx ou SetupCommitFileQueue para uma rotina de retorno de chamada quando uma operação de arquivo foi atrasada porque o arquivo estava em uso. A operação será processada na próxima vez em que o sistema for reinicializado.
ms.assetid: a0b38e2b-2390-49e5-b288-77c31636e696
title: Mensagem de SPFILENOTIFY_FILEOPDELAYED (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38975506ff998ec09c4549ec95d9ddb620466cf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827926"
---
# <a name="spfilenotify_fileopdelayed-message"></a>\_Mensagem SPFILENOTIFY FILEOPDELAYED

A notificação **SPFILENOTIFY \_ FILEOPDELAYED** é enviada por [**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa) ou [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) para uma rotina de retorno de chamada quando uma operação de arquivo foi atrasada porque o arquivo estava em uso. A operação será processada na próxima vez em que o sistema for reinicializado.


```C++
SPFILENOTIFY_FILEOPDELAYED
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Param1* 
</dt> <dd>

Ponteiro para uma estrutura [**FILEpaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .

Se a operação atrasada for uma operação de cópia de arquivo, a estrutura [**FILEpaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) conterá as informações a seguir.



| Membro filePaths | Valor                                |
|------------------|--------------------------------------|
| **Win32Error**   | SEM \_ erros                            |
| **Sinalizadores**        | \_cópia FILEOP                         |
| **Origem**       | Caminho completo do arquivo temporário.     |
| **Target (destino)**       | Caminho completo do arquivo de destino real. |



 

Esse arquivo temporário será copiado para o diretório de destino quando o sistema for reinicializado. As funções de instalação geram automaticamente um caminho para o arquivo temporário.

Se a operação atrasada for uma operação de exclusão de arquivo, a estrutura [**FILEpaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) conterá as informações a seguir.



| Membro filePaths | Valor                                |
|------------------|--------------------------------------|
| **Win32Error**   | SEM \_ erros                            |
| **Sinalizadores**        | FILEOP \_ excluir                       |
| **Origem**       | NULO                                 |
| **Target (destino)**       | Caminho completo do arquivo a ser excluído. |



 

</dd> <dt>

*Param2* 
</dt> <dd>

Não é usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é ignorado.

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

[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)
</dt> <dt>

[**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)
</dt> <dt>

[**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> </dl>

 

 




