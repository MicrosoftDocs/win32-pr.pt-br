---
title: Usando TBS
description: Cada comando enviado ao TBS é associado a uma entidade específica. Isso é feito criando um ou mais contextos para uma entidade, que são então associados a cada comando subsequente enviado por essa entidade.
ms.assetid: 609f1e95-9868-4e34-8758-71306ac4e51f
keywords:
- TBS de serviços base do TPM, exemplos
- TBS de serviços base do TPM, usando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 189d047e6cf969887e390ac7dad1cfc8cdbfa4f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916321"
---
# <a name="using-tbs"></a>Usando TBS

O recurso de serviços base do TPM é dividido em quatro áreas funcionais:

-   [Virtualização de recursos](resource-virtualization.md)
-   [Agendamento de comandos](command-scheduling.md)
-   [Gerenciamento de Energia](power-management.md)
-   [Bloqueio de comando](command-blocking.md)

Para garantir que entidades diferentes não possam acessar os recursos uns dos outros, cada comando enviado ao TBS é associado a uma entidade específica. Isso é feito criando um ou mais contextos para uma entidade, que são então associados a cada comando subsequente enviado por essa entidade. Cada comando inclui um objeto de contexto, que permite que o TBS execute comandos do TPM no contexto apropriado. Todos os objetos criados por comandos são liberados do TPM quando o contexto é fechado.

Uma entidade cria o contexto antes de ele primeiro acessar o TBS e mantém o contexto até que ele termine de executar acessos TBS. Por exemplo, no caso de um TSS, o recurso de TCS (serviços principais do TCG) do TSS criaria um contexto TBS quando ele for iniciado, e ele manterá esse contexto ativo até ser desligado.

Para o Windows Server 2008 e o Windows Vista, o TBS restringe o acesso à API TBS para as contas de administradores, NT e LocalService da autoridade \\ NT \\ . Por padrão, essas contas são as únicas que podem se conectar a TBS e criar contextos. As restrições de acesso podem ser modificadas com a criação de um **acesso à** chave do registro com um nome de valor do registro de cadeia de caracteres (**reg \_ sz**) **SecurityDescriptor** <dl> <dt>

Tipo de dados
</dt> <dd>REG_SZ</dd> </dl> under it as follows:

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         TPM
            Access
               SecurityDescriptor = SecurityDescriptor
```

Exemplo:

**O:BAG: INADEQUADO: (A;; 0 x00000001;;; BA) (A;; 0 x00000001;;; NS) (A;; 0 x00000001;;; LS**

Por padrão, o número máximo de contextos com suporte no TBS é 25. Esse número pode ser alterado criando ou modificando um valor de registro **DWORD** chamado **MaxContexts** em **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **TPM**. O uso de contexto TBS em tempo real pode ser observado usando a ferramenta Monitor de desempenho para controlar o número de contextos TBS.

Para o Windows 8, o Windows Server 2012 e posterior, o TBS permite o acesso a usuários e administradores padrão. As chaves do registro **SecurityDescriptor** e **MaxContexts** se tornaram obsoletas. Para o Windows 8, o Windows Server 2012 e posterior, o TBS restringe o acesso a certos comandos usando o bloqueio de comando.

Para o Windows 10, versão 1607, o TBS permite o acesso de aplicativos do AppContainer. Para cada versão do TPM, as chaves **BlockedAppContainerCommands** e **AllowedW8AppContainerCommands** foram adicionadas com as listas correspondentes de comandos do TPM bloqueados e permitidos, respectivamente.

Para o Windows 10, versão 1803, as chaves do registro em **AllowedW8AppContainerCommands** não são mais suportadas.

 

 




