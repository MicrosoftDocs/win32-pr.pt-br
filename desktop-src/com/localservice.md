---
title: LocalService
description: Instala um objeto como um aplicativo de serviço.
ms.assetid: e8086118-f956-4cc2-a0fb-3cebd2e66799
keywords:
- COM valor de registro LocalService COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31f630c7c0a6f5e3bbf4b9c26ad82e5a104be238
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103824018"
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

Além de serem executados como um executável de servidor local (EXE), um objeto COM também pode optar por empacotar para ser executado como um aplicativo de serviço quando ativado por um cliente local ou remoto. Os serviços dão suporte a vários recursos administrativos úteis e integrados à interface do usuário, incluindo início, parada, pausa e reinicialização locais e remotos, bem como a capacidade de estabelecer o servidor para ser executado em uma conta de usuário e estação de janela específicas.

Um objeto escrito como um serviço é instalado para ser usado pelo COM, estabelecendo um valor de **LocalService** e executando uma instalação de serviço padrão. O valor **LocalService** deve ser definido como o nome do serviço, conforme configurado em **HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Services**, como o valor de **\_ sz padrão reg** .

Quando o **LocalService** é definido, qualquer cadeia de caracteres atribuída a [**serviceparameters**](serviceparameters.md) é passada como um argumento de linha de comando para o serviço à medida que ele é iniciado.

A configuração de serviço é preferida em muitas situações em que os recursos das APIs de gerenciamento de serviço local e remoto e a interface do usuário podem ser úteis para os serviços que o objeto fornece. Por exemplo, aproveitar a estrutura administrativa existente da arquitetura de serviço deve ser uma opção óbvia se o objeto for de longa duração ou der suporte imediato a conceitos como iniciar, parar, redefinir ou pausar.

Os serviços podem ser configurados dinamicamente e podem ser configurados para serem executados automaticamente quando o computador é inicializado, ou para serem iniciados quando solicitado por um aplicativo cliente.

Se você estiver implementando classes como serviços, deve estar ciente dos seguintes pontos:

-   Esse valor é usado em preferência à chave [**LocalServer32**](localserver32.md) para ativação local e remota requestsâ € "se o **LocalService** existir e se referir a um serviço válido, a chave **LocalServer32** será ignorada.
-   Atualmente, apenas uma única instância de um aplicativo de serviço pode estar sendo executada em um determinado momento em um computador. Os serviços COM devem, portanto, registrar seus objetos de classe na inicialização usando REGCLS \_ MULTIPLEUSE para dar suporte a vários clientes.
-   Para iniciar e inicializar corretamente, os serviços COM configurados para serem executados automaticamente quando um computador é inicializado devem incluir RPCSs na lista de serviços dependentes.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registrando servidores COM](registering-com-servers.md)
</dt> <dt>

[**Serviceparameters**](serviceparameters.md)
</dt> <dt>

[Serviços](/windows/desktop/Services/services)
</dt> </dl>

 

 