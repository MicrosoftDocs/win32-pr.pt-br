---
description: Uma pequena atualização pode ser aplicada a um aplicativo por meio da aplicação de patch na instalação local do aplicativo.
ms.assetid: 2a04ffd0-d5b6-44f3-bef2-73f59179aed1
title: Aplicando pequenas atualizações por meio da aplicação de patch na instalação local do produto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bced3e7f69761ff3e270046718eedb9032cab8a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921514"
---
# <a name="applying-small-updates-by-patching-the-local-installation-of-the-product"></a>Aplicando pequenas atualizações por meio da aplicação de patch na instalação local do produto

Uma pequena atualização pode ser aplicada a um aplicativo por meio da aplicação de patch na instalação local do aplicativo.

**Para aplicar um patch de atualização pequeno a uma instalação local do produto**

1.  Inicie a instalação do patch na linha de comando ou usando um executável. Para iniciar a partir da linha de comando, use **msiexec/p patch. msp \[ reinstalar =***_\] REINSTALLMODE_* da _lista de recursos_ = omus. Para iniciar a partir de um executável, chame [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) ou o [**método ApplyPatch**](installer-applypatch.md) e forneça os mesmos argumentos de linha de comando.
2.  Ao aplicar patch na instalação de um cliente, o instalador ignora a origem da instalação e prossegue para corrigir os arquivos que já estão instalados no computador do usuário.
3.  O instalador altera todos os componentes com patches marcados como executar da origem para execução local. Os usuários não poderão executar esses componentes da origem desde que o patch permaneça no computador.
4.  O instalador adiciona todas as transformações usadas para atualizar o arquivo. msi ou adiciona informações específicas do patch ao perfil do usuário.
5.  O instalador armazena em cache o arquivo. msi no computador do usuário para que ele possa executar a instalação sob demanda, reinstalar e reparar o aplicativo. Depois que um patch é aplicado a uma instalação autônoma, o instalador faz referência a duas ou mais listas de origem a arquivos externos: uma para a fonte original e outra para cada patch que foi aplicado.

 

 



