---
description: Antes que o mecanismo de configuração de segurança possa chamar seu mecanismo de anexo para processar tarefas específicas do serviço, você deve instalar o mecanismo de anexo e registrá-lo no mecanismo de configuração de segurança.
ms.assetid: f7376a79-97cd-4607-9e1b-5b8c7cd76a32
title: Registrando um mecanismo de anexo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f50827fe27e86328e7e914bfc98740fa5e15060
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760195"
---
# <a name="registering-an-attachment-engine"></a>Registrando um mecanismo de anexo

Antes que o mecanismo de configuração de segurança possa chamar seu mecanismo de anexo para processar tarefas específicas do serviço, você deve instalar o mecanismo de anexo e registrá-lo no mecanismo de configuração de segurança.

**Para instalar e registrar a DLL do mecanismo de anexo**

1.  Copie a DLL do mecanismo de anexo para um diretório no sistema. O diretório preferencial são os anexos de% windir% \\ secedit \\ . Se esse diretório não existir, você deverá criá-lo.
2.  Crie uma chave do registro no nó a seguir. O *nome do serviço* é o nome registrado para o anexo e deve ser o mesmo nome de serviço usado no Gerenciador de controle de serviço, um módulo que gerencia a interrupção e o início dos serviços. O nome também deve ser exclusivo para que não entre em conflito com os nomes de outros anexos.

    ```
    HKEY_LOCAL_MACHINE
       Microsoft
          Windows NT
             CurrentVersion
                SeCEdit
                   Service
                      service name
    ```

3.  Crie o seguinte valor de cadeia de caracteres na nova chave do registro. *caminho do mecanismo de anexo* é o caminho completo para o módulo do mecanismo de anexo.<dl> <dd>**ServiceAttachmentPath**  =  *caminho do mecanismo de anexo*<dl> <dt>

Tipo de dados
</dt> <dd>REG_SZ</dd> </dl> </dd> </dl>

 

 



