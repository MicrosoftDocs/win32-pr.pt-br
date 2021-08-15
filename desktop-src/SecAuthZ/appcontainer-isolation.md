---
description: O isolamento é a meta principal de um ambiente de execução appContainer.
ms.assetid: 13C579F9-7F9F-4602-9B03-08CD820C3BBA
title: Isolamento do AppContainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfe42b12698983bc3a90af06be2bb45992013b52e16e6f7de37083d6c92b9422
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117784702"
---
# <a name="appcontainer-isolation"></a>Isolamento do AppContainer

O isolamento é a meta principal de um ambiente de execução appContainer. Ao isolar um aplicativo de recursos não necessários e outros aplicativos, as oportunidades de manipulação mal-intencionada são minimizadas. Conceder acesso com base em privilégios mínimos impede que aplicativos e usuários acessem recursos além de seus direitos. Controlar o acesso aos recursos protege o processo, o dispositivo e a rede.

A maioria das vulnerabilidades Windows começar com o aplicativo. Alguns exemplos comuns incluem um aplicativo que sai do navegador ou envia um documento ruim para Internet Explorer, bem como a exploração de plug-ins, como flash. Quanto mais esses aplicativos puderem ser isolados em um AppContainer, mais seguro será o dispositivo e os recursos. Mesmo que a vulnerabilidade em um aplicativo seja explorada, o aplicativo não poderá acessar recursos além do que é concedido ao AppContainer. Aplicativos mal-intencionados não podem assumir o restante do computador.

## <a name="credential-isolation"></a>Isolamento de credenciais

Gerenciando identidade e credenciais, o AppContainer impede o uso de credenciais de usuário para obter acesso a recursos ou fazer logon em outros ambientes. O ambiente do AppContainer cria um identificador que usa as identidades combinadas do usuário e do aplicativo, portanto, as credenciais são exclusivas para cada emparelhamento de usuário/aplicativo e o aplicativo não pode representar o usuário.

## <a name="device-isolation"></a>Isolamento do dispositivo

Isolar o aplicativo de recursos do dispositivo, como sensores passivos (câmera, microfone, GPS) e bomba de dinheiro (3G/4G, telefone discado), o ambiente appContainer impede que o aplicativo explore o dispositivo de forma mal-intencionada. Esses recursos são bloqueados por padrão e podem ter acesso conforme necessário. Em alguns casos, esses recursos são ainda mais protegidos por 'brokers'. Alguns recursos, como teclado e mouse, estão sempre disponíveis para o AppContainer e o aplicativo residente.

## <a name="file-isolation"></a>Isolamento de arquivo

Controlando o acesso ao arquivo e ao Registro, o ambiente AppContainer impede que o aplicativo modifique arquivos que ele não deveria. O acesso de leitura/gravação pode ser concedido a arquivos persistentes e chaves do Registro específicos. O acesso somente leitura é menos restrito. Um aplicativo sempre tem acesso aos arquivos residentes de memória criados especificamente para esse AppContainer.

## <a name="network-isolation"></a>Isolamento de rede

Isolando o aplicativo de recursos de rede além daqueles especificamente alocados, AppContainer impede que o aplicativo "escape" seu ambiente e exploram maliciosamente os recursos de rede. O acesso granular pode ser concedido para acesso à Internet, acesso à Intranet e atuar como um servidor.

## <a name="process-isolation"></a>Isolamento do processo

Ao fazer a área sandbox dos objetos de kernel do aplicativo, o ambiente AppContainer impede que o aplicativo influencia ou seja influenciado por outros processos de aplicativo. Isso impede que um aplicativo contido corretamente corrompa outros processos no caso de uma exceção.

## <a name="window-isolation"></a>Isolamento de janela

Isolando o aplicativo de outras janelas, o ambiente AppContainer impede que o aplicativo afete outras interfaces de aplicativo.

 

 



