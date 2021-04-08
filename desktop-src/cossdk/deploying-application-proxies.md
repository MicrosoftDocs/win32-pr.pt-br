---
description: Para acessar um aplicativo de servidor COM+ remotamente de outro computador (cliente), o computador cliente deve ter um subconjunto dos atributos do aplicativo de servidor instalado, incluindo DLLs proxy/stub e bibliotecas de tipos para comunicação remota da interface DCOM/QC.
ms.assetid: 293b424c-4cd4-43a9-9b56-687c753a34f2
title: Implantando proxies de aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f5e6439574602005ca53917945fa9005f8959b5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920608"
---
# <a name="deploying-application-proxies"></a>Implantando proxies de aplicativo

Para acessar um aplicativo de servidor COM+ remotamente de outro computador (cliente), o computador cliente deve ter um subconjunto dos atributos do aplicativo de servidor instalado, incluindo DLLs proxy/stub e bibliotecas de tipos para comunicação remota da interface DCOM/QC. Esse subconjunto é chamado de *proxy de aplicativo*.

Por meio da ferramenta administrativa serviços de componentes, você pode exportar facilmente um aplicativo de servidor COM+ como um proxy de aplicativo. Para que o COM+ gere um proxy de aplicativo, é importante que todos os componentes no aplicativo de servidor tenham sido instalados e não importados. (Para obter mais informações sobre essa distinção, consulte [importando componentes](importing-components.md).) Isso garante que o aplicativo inclua todas as informações de Registro necessárias.

> [!Note]  
> É recomendável que você separe as definições de interface das implementações de classe. Caso contrário, o conjunto de DLLs ou bibliotecas de tipos incluídas no proxy de aplicativo COM+ incluirá o código de servidor real.

 

Os proxies de aplicativo gerados pelo COM+ são Windows Installer pacotes de instalação. Após a instalação, os proxies de aplicativo aparecem no painel de controle adicionar/remover programas do computador cliente (a menos que o arquivo. msi seja modificado usando uma ferramenta de criação de Windows Installer).

## <a name="remote-access-via-application-proxies"></a>Acesso remoto por meio de proxies de aplicativo

Ao gerar um proxy de aplicativo, o COM+ fornece automaticamente as seguintes informações, necessárias para que o proxy de aplicativo acesse remotamente um aplicativo de servidor COM+:

-   Informações de identidade de classe (CLSIDs e ProgIDs). Um proxy de aplicativo dá suporte a até dois ProgIDs.
-   Identidade do aplicativo e relação de classes para aplicativos (AppID).
-   Informações de local por aplicativo (nome do servidor remoto).
-   Informações de marshaling para todas as interfaces expostas pelo aplicativo (por exemplo, bibliotecas de tipos e proxy/stubs).
-   Identificadores e nomes de fila do MSMQ (se o serviço de componentes em fila estiver habilitado para o aplicativo).
-   Atributos de classe, interface e método, excluindo informações de função.
-   Atributos do aplicativo.

## <a name="installing-application-proxies-on-other-operating-systems"></a>Instalando proxies de aplicativo em outros sistemas operacionais

Diferentemente dos aplicativos do servidor COM+, os proxies de aplicativo podem ser instalados em qualquer sistema operacional que dê suporte a DCOM (e Windows Installer). Em computadores que não estão executando o COM+, somente o subconjunto de informações necessário para a comunicação remota do DCOM é instalado. Essas informações são instaladas no registro do Windows (usando as \_ chaves hKey classes \_ raiz, AppID/CLSID).

> [!Note]  
> Ao instalar um proxy de aplicativo (arquivo. msi) em computadores que não estão executando o COM+, é necessário ter Windows Installer em execução nesses computadores. É recomendável que os desenvolvedores enviem o arquivo de Windows Installer redistribuível (instmsi.exe) junto com o arquivo. msi de seu aplicativo. Isso garantirá que os administradores do sistema tenham Windows Installer disponíveis ao implantar proxies de aplicativo em clientes que não estão executando o COM+.

 

Em computadores que executam o COM+, as informações do proxy de aplicativo são instaladas no catálogo COM+ e ficam visíveis na ferramenta administrativa serviços de componentes.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando pacotes de instalação para aplicativos COM+](creating-installation-packages-for-com--applications.md)
</dt> <dt>

[O catálogo COM+](the-com--catalog.md)
</dt> <dt>

[O utilitário de replicação COMREPL](the-comrepl-replication-utility.md)
</dt> </dl>

 

 



