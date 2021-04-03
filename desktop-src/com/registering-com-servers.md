---
title: Registrando servidores COM
description: Registrando servidores COM
ms.assetid: aaa09a1b-deb8-424f-a911-ae22d39919d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefaa47d159d776a3c931ca48de0dd3161c29913
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104084912"
---
# <a name="registering-com-servers"></a>Registrando servidores COM

Depois de definir uma classe no código (garantindo que ela implemente [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) ou [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2)) e atribuída a ela um CLSID, você precisa colocar as informações no registro que permitirá com, na solicitação de um cliente com o CLSID, para criar instâncias de seus objetos. Essas informações dizem ao sistema, para um determinado CLSID, onde o código DLL ou EXE para essa classe está localizado e como ele deve ser iniciado.

Há mais de uma maneira de registrar uma classe no registro. Além disso, há outras maneiras de "registrar" uma classe com o sistema quando ele está em execução, para que o sistema esteja ciente de que um objeto em execução está atualmente no sistema.

Consulte os tópicos a seguir para obter mais informações sobre como registrar-se:

-   [Registrando uma classe na instalação](registering-a-class-at-installation.md)
-   [Registrando um servidor EXE em execução](registering-a-running-exe-server.md)
-   [Registrando objetos no corrompidos](registering-objects-in-the-rot.md)
-   [Registro automático](self-registration.md)
-   [Instalando como um aplicativo de serviço](installing-as-a-service-application.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Responsabilidades do servidor COM](com-server-responsibilities.md)
</dt> </dl>

 

 