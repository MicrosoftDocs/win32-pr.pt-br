---
description: O isolamento é a meta principal de um ambiente de execução do AppContainer.
ms.assetid: 13C579F9-7F9F-4602-9B03-08CD820C3BBA
title: Isolamento do AppContainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82fec44fd3d6eb9495370c42e52726ceb0f63806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170801"
---
# <a name="appcontainer-isolation"></a>Isolamento do AppContainer

O isolamento é a meta principal de um ambiente de execução do AppContainer. Ao isolar um aplicativo de recursos desnecessários e de outros aplicativos, as oportunidades de manipulação mal-intencionada são minimizadas. Conceder acesso com base no privilégio mínimo impede que aplicativos e usuários acessem recursos além de seus direitos. Controlar o acesso a recursos protege o processo, o dispositivo e a rede.

A maioria das vulnerabilidades no Windows é iniciada com o aplicativo. Alguns exemplos comuns incluem um aplicativo que está dividindo seu navegador ou enviando um documento inadequado para o Internet Explorer, bem como a exploração de plugins, como o flash. Quanto mais esses aplicativos puderem ser isolados em um AppContainer, mais seguro será o dispositivo e os recursos. Mesmo se a vulnerabilidade em um aplicativo for explorada, o aplicativo não poderá acessar recursos além do que é concedido ao AppContainer. Aplicativos mal-intencionados não podem assumir o resto do computador.

## <a name="credential-isolation"></a>Isolamento de credenciais

Gerenciando identidades e credenciais, o AppContainer impede o uso de credenciais do usuário para obter acesso a recursos ou fazer logon em outros ambientes. O ambiente do AppContainer cria um identificador que usa as identidades combinadas do usuário e do aplicativo, portanto, as credenciais são exclusivas para cada emparelhamento de usuário/aplicativo e o aplicativo não pode representar o usuário.

## <a name="device-isolation"></a>Isolamento do dispositivo

Isolar o aplicativo dos recursos do dispositivo, como sensores passivos (câmera, microfone, GPS) e bombas de dinheiro (3G/4G, telefone de discagem) o ambiente do AppContainer impede que o aplicativo Explore o dispositivo de forma mal-intencionada. Esses recursos são bloqueados por padrão e podem ter acesso concedido conforme necessário. Em alguns casos, esses recursos são protegidos por "agentes". Alguns recursos, como teclado e mouse, estão sempre disponíveis para o AppContainer e o aplicativo residente.

## <a name="file-isolation"></a>Isolamento de arquivo

Controlando o acesso ao arquivo e ao registro, o ambiente do AppContainer impede que o aplicativo modifique os arquivos que não deveria. O acesso de leitura/gravação pode ser concedido a arquivos persistentes e chaves do registro específicos. O acesso somente leitura é menos restrito. Um aplicativo sempre tem acesso aos arquivos residentes na memória criados especificamente para esse AppContainer.

## <a name="network-isolation"></a>Isolamento de rede

Isolando o aplicativo dos recursos de rede além daqueles alocados especificamente, o AppContainer impede que o aplicativo "escape" seu ambiente e explore os recursos de rede de forma mal-intencionada. O acesso granular pode ser concedido para acesso à Internet, acesso à intranet e atuar como um servidor.

## <a name="process-isolation"></a>Isolamento do processo

Colocar os objetos de kernel do aplicativo em área restrita, o ambiente do AppContainer impede que o aplicativo ininfluenciasse ou seja influenciado por outros processos de aplicativos. Isso impede que um aplicativo independente apropriado corrompa outros processos no caso de uma exceção.

## <a name="window-isolation"></a>Isolamento de janela

Isolando o aplicativo de outras janelas, o ambiente do AppContainer impede que o aplicativo afete outras interfaces do aplicativo.

 

 



