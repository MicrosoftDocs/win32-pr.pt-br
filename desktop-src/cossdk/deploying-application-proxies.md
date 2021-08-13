---
description: Para acessar um aplicativo de servidor COM+ remotamente de outro computador (cliente), o computador cliente deve ter um subconjunto dos atributos do aplicativo de servidor instalado, incluindo DLLs de proxy/stub e bibliotecas de tipos para comunicação remota de interface DCOM/QC.
ms.assetid: 293b424c-4cd4-43a9-9b56-687c753a34f2
title: Implantando proxies de aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e651338e4bd89cb4fe5cb77789e5e10392f62e065da0f61ec4ea19f7cca312b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118547984"
---
# <a name="deploying-application-proxies"></a>Implantando proxies de aplicativo

Para acessar um aplicativo de servidor COM+ remotamente de outro computador (cliente), o computador cliente deve ter um subconjunto dos atributos do aplicativo de servidor instalado, incluindo DLLs de proxy/stub e bibliotecas de tipos para comunicação remota de interface DCOM/QC. Esse subconjunto é chamado de *proxy de aplicativo.*

Por meio da ferramenta administrativa serviços de componentes, você pode exportar facilmente um aplicativo de servidor COM+ como um proxy de aplicativo. Para que o COM+ gere um proxy de aplicativo, é importante que todos os componentes no aplicativo de servidor sejam instalados e não importados. (Para obter mais informações sobre essa distinção, consulte [Importando componentes](importing-components.md).) Isso garante que o aplicativo inclua todas as informações de registro necessárias.

> [!Note]  
> É recomendável separar as definições de interface das implementações de classe. Caso contrário, o conjunto de DLLs ou bibliotecas de tipos incluídas no proxy de aplicativo COM+ incluirá o código do servidor real.

 

Proxies de aplicativo gerados pelo COM+ são Windows de instalação do Instalador. Após a instalação, os proxies do aplicativo aparecem no painel de controle Adicionar/Remover Programas do computador cliente (a menos que o arquivo .msi seja modificado usando uma ferramenta de Windows de instalação).

## <a name="remote-access-via-application-proxies"></a>Acesso remoto por meio de proxies de aplicativo

Ao gerar um proxy de aplicativo, o COM+ fornece automaticamente as seguintes informações, necessárias para que o proxy de aplicativo acesse remotamente um aplicativo de servidor COM+:

-   Informações de identidade de classe (CLSIDs e ProgIDs). Um proxy de aplicativo dá suporte a até dois ProgIDs.
-   Identidade do aplicativo e relação de classes com aplicativos (AppID).
-   Informações de localização por aplicativo (Nome do Servidor Remoto).
-   Marshaling de informações para todas as interfaces expostas pelo aplicativo (por exemplo, bibliotecas de tipos e proxy/stubs).
-   Identificadores e nomes de fila do MSMQ (se o serviço de componentes na fila estiver habilitado para o aplicativo).
-   Atributos de classe, interface e método, excluindo informações de função.
-   Atributos de aplicativo.

## <a name="installing-application-proxies-on-other-operating-systems"></a>Instalando proxies de aplicativo em outros sistemas operacionais

Ao contrário dos aplicativos de servidor COM+, os proxies de aplicativo podem ser instalados em qualquer sistema operacional que dá suporte ao DCOM (e Windows Installer). Em computadores que não estão executando o COM+, apenas o subconjunto de informações necessário para a comunicação de comunicação comunicação de DCOM está instalado. Essas informações são instaladas no Windows (usando as chaves HKEY \_ CLASSES \_ ROOT, APPID/CLSID).

> [!Note]  
> Ao instalar um proxy de aplicativo (.msi arquivo) em computadores que não executam o COM+, é necessário ter um instalador Windows em execução nesses computadores. É recomendável que os desenvolvedores Windows arquivo redistribuível do Windows (instmsi.exe) juntamente com o arquivo .msi aplicativo. Isso garantirá que os administradores do sistema tenham Windows instalador disponível ao implantar proxies de aplicativo em clientes que não estão executando COM+.

 

Em computadores que executam o COM+, as informações do proxy de aplicativo são instaladas no catálogo COM+ e são visíveis na ferramenta administrativa dos Serviços de Componentes.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando pacotes de instalação para aplicativos COM+](creating-installation-packages-for-com--applications.md)
</dt> <dt>

[O catálogo COM+](the-com--catalog.md)
</dt> <dt>

[O utilitário de replicação COMREPL](the-comrepl-replication-utility.md)
</dt> </dl>

 

 



