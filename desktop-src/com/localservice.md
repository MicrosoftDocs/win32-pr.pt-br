---
title: LocalService
description: Instala um objeto como um aplicativo de serviço.
ms.assetid: e8086118-f956-4cc2-a0fb-3cebd2e66799
keywords:
- Valor do Registro LocalService COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e454566ac505907f66fad585062bc67f41c865df45b30405b83e5faadef7f9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736462"
---
# <a name="localservice"></a>LocalService

Instala um objeto como um aplicativo de serviço.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      LocalService = name
```

## <a name="remarks"></a>Comentários

Além de ser executado como um EXE (executável de servidor local), um objeto COM também pode optar por empacotá-lo para ser executado como um aplicativo de serviço quando ativado por um cliente local ou remoto. Os serviços suportam vários recursos administrativos úteis e integrados à interface do usuário, incluindo início local e remoto, parada, pausa e reinicialização, bem como a capacidade de estabelecer o servidor para ser executado em uma conta de usuário e estação de janela específicas.

Um objeto gravado como um serviço é instalado para uso pelo COM estabelecendo um **valor LocalService** e executando uma instalação de serviço padrão. O **valor LocalService** deve ser definido como o nome do serviço, conforme configurado em **HKEY LOCAL MACHINE System \_ \_ \\ \\ CurrentControlSet \\ Services**, como o valor **padrão de REG \_ SZ.**

Quando **LocalService** é definido, qualquer cadeia de caracteres atribuída a [**ServiceParameters**](serviceparameters.md) é passada como um argumento de linha de comando para o serviço enquanto ele está sendo lançado.

A configuração de serviço é preferencial em muitas situações em que os recursos das APIs de gerenciamento de serviços locais e remotos e da interface do usuário podem ser úteis para os serviços que o objeto fornece. Por exemplo, aproveitar a estrutura administrativa existente da arquitetura de serviço deve ser uma opção óbvia se o objeto tiver vida longa ou prontamente dar suporte a conceitos como iniciar, parar, redefinir ou pausar.

Os serviços podem ser configurados dinamicamente e podem ser configurados para serem executados automaticamente quando o computador for inicializado ou inicializados quando solicitados por um aplicativo cliente.

Se você estiver implementando classes como serviços, deverá estar ciente dos seguintes pontos:

-   Esse valor é usado como preferência para a chave [**LocalServer32**](localserver32.md) para solicitações de ativação local e remota" se **LocalService** existir e se referir a um serviço válido, a chave **LocalServer32** será ignorada.
-   Atualmente, apenas uma única instância de um aplicativo de serviço pode estar em execução em um determinado momento em um computador. Portanto, os serviços COM devem registrar seus objetos de classe na iniciação usando REGCLS \_ MULTIPLEUSE para dar suporte a vários clientes.
-   Para iniciar e inicializar corretamente, os serviços COM configurados para executar automaticamente quando uma inicialização de computador deve incluir RPCSS na lista de serviços dependentes.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registrando servidores COM](registering-com-servers.md)
</dt> <dt>

[**ServiceParameters**](serviceparameters.md)
</dt> <dt>

[Serviços](/windows/desktop/Services/services)
</dt> </dl>

 

 