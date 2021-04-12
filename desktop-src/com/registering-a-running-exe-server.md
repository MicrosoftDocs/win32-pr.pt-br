---
title: Registrando um servidor EXE em execução
description: Registrando um servidor EXE em execução
ms.assetid: 277f44bb-72b7-4409-955d-2cd53bc99467
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa0c6cae15818e5cdb3931f71f0d4be1ac1baef6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292585"
---
# <a name="registering-a-running-exe-server"></a>Registrando um servidor EXE em execução

Quando um servidor executável (EXE) é iniciado, ele deve chamar [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject), que registra o CLSID para o servidor no que é chamado de tabela de classe (uma tabela diferente da tabela de objetos em execução). Quando um servidor é registrado na tabela de classes, ele permite que o SCM (Gerenciador de controle de serviço) determine que não é necessário iniciar a classe novamente, porque o servidor já está em execução. Somente se o servidor não estiver listado na tabela de classe, o SCM verificará os valores apropriados no registro e iniciará o servidor associado ao CLSID fornecido.

Você passa [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) o CLSID para a classe e um ponteiro para sua interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) . Os clientes que, posteriormente, chamam o [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) com esse CLSID recuperarão um ponteiro para a interface solicitada, desde que a segurança não proíba isso. (Consulte [funções auxiliares de criação de instância](instance-creation-helper-functions.md) para obter uma descrição de várias funções de criação e ativação de instância.)

O servidor para um objeto de classe deve chamar [**CoRevokeClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-corevokeclassobject) para revogar o objeto de classe (remover seu registro) quando todas as seguintes opções forem verdadeiras:

-   Não há instâncias existentes da definição de objeto.
-   Não há bloqueios no objeto de classe.
-   O aplicativo que fornece serviços para o objeto de classe não está sob controle de usuário (não visível para o usuário na exibição).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instalando como um aplicativo de serviço](installing-as-a-service-application.md)
</dt> <dt>

[Registrando uma classe na instalação](registering-a-class-at-installation.md)
</dt> <dt>

[Registrando objetos no corrompidos](registering-objects-in-the-rot.md)
</dt> <dt>

[Registro automático](self-registration.md)
</dt> </dl>

 

 




