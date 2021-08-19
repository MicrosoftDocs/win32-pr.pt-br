---
description: contém informações sobre a interface de programação para o serviço de configuração Zero sem fio no Windows XP e no Windows Server 2003.
ms.assetid: cd9e8fc0-0a65-4654-95aa-201751183521
title: Referência de configuração zero sem fio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 358ff3727edc34d4a5de0f4195895cf02b4596722aecd5849f4e35b9991dbe88
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684426"
---
# <a name="wireless-zero-configuration-reference"></a>Referência de configuração zero sem fio

\[não há mais suporte para a interface de programação de configuração Zero sem fio a partir do Windows Vista e do Windows Server 2008. Em vez disso, use a [API Wi-Fi nativa](native-wifi-reference.md), que fornece funcionalidade semelhante. Para obter mais informações, consulte [sobre a API Wi-Fi nativa](about-the-native-wifi-api.md).\]

esta seção contém informações sobre a interface de programação para o serviço de configuração Zero sem fio no Windows XP e no Windows Server 2003. Os tópicos incluem:

-   [Funções de configuração sem fio zero](wireless-zero-configuration-functions.md)
-   [Estruturas de configuração sem fio zero](wireless-zero-configuration-structures.md)

a configuração sem fio Zero é um serviço Windows no Windows XP e no Windows Server 2003 que é usado para configurar e gerenciar conexões de rede sem fio em um adaptador sem fio. O nome do serviço para a configuração zero sem fio é WZCSVC. no Windows XP, o nome de exibição para o serviço WZCSVC é a configuração Zero sem fio. no Windows Server 2003, o nome de exibição para o serviço WZCSVC é configuração sem fio.

O serviço de configuração zero sem fio normalmente é iniciado no momento da inicialização. A interface de programação para o serviço de configuração zero sem fio só poderá ser usada se o serviço de configuração sem fio for iniciado. Se o serviço de configuração zero sem fio não for iniciado, as funções de configuração sem fio zero retornarão um erro.

Para habilitar o serviço de configuração zero sem fio para que ele seja iniciado automaticamente, vá para o botão **Iniciar** . selecione a opção **Configurações** e, em seguida, selecione **painel de controle**. se você estiver usando a exibição Windows XP, selecione a categoria **desempenho e manutenção** e, em seguida, selecione **ferramentas administrativas**. Se você estiver usando o modo de exibição clássico, selecione **Ferramentas administrativas**. Clique no ícone **Serviços** no painel esquerdo. Clique no ícone configuração sem fio zero no painel direito e altere o **tipo de inicialização** Dropbox para **automático**. Essa configuração definirá o serviço para iniciar automaticamente no momento da inicialização. Em seguida, clique no botão **Iniciar** para iniciar o serviço de configuração zero sem fio sem fio zero e clique no botão **OK** .

A configuração sem fio zero também pode ser iniciada e interrompida em um prompt de comando. Para iniciar a configuração zero sem fio, execute o seguinte comando:

**net start WZCSVC**

Para interromper a configuração zero sem fio, execute o seguinte comando:

**WZCSVC net stop**

 

 



