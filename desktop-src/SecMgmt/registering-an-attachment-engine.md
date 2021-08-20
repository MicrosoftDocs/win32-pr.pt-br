---
description: Antes que o Mecanismo de Configuração de Segurança possa chamar o mecanismo de anexo para processar tarefas específicas do serviço, você deve instalar o mecanismo de anexo e registrá-lo com o Mecanismo de Configuração de Segurança.
ms.assetid: f7376a79-97cd-4607-9e1b-5b8c7cd76a32
title: Registrando um mecanismo de anexo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04d3d13bab6c26254295734344011a9f56457b8fac28c913178c7515cc147fb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118893695"
---
# <a name="registering-an-attachment-engine"></a>Registrando um mecanismo de anexo

Antes que o Mecanismo de Configuração de Segurança possa chamar o mecanismo de anexo para processar tarefas específicas do serviço, você deve instalar o mecanismo de anexo e registrá-lo com o Mecanismo de Configuração de Segurança.

**Para instalar e registrar a DLL do mecanismo de anexo**

1.  Copie a DLL do mecanismo de anexo para um diretório no sistema. O diretório preferencial é %windir% \\ secedit \\ attachments. Se esse diretório não existir, você deverá crie-o.
2.  Crie uma chave do Registro no nó a seguir. O *nome do* serviço é o nome registrado para o anexo e deve ser o mesmo nome de serviço usado no Service Control Manager, um módulo que gerencia a interrupção e o início dos serviços. O nome também deve ser exclusivo para que não entre em conflito com os nomes de outros anexos.

    ```
    HKEY_LOCAL_MACHINE
       Microsoft
          Windows NT
             CurrentVersion
                SeCEdit
                   Service
                      service name
    ```

3.  Crie o seguinte valor de cadeia de caracteres na nova chave do Registro. *o caminho do mecanismo de* anexo é o caminho completo para o módulo do mecanismo de anexo.<dl> <dd>**ServiceAttachmentPath**  =  *caminho do mecanismo de anexo*<dl> <dt>

Tipo de dados
</dt> <dd>REG_SZ</dd> </dl> </dd> </dl>

 

 



