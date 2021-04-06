---
description: Uma atualização importante pode ser aplicada a um aplicativo por meio da aplicação de patch na instalação local do aplicativo a partir da linha de comando ou usando um executável.
ms.assetid: be651457-5c66-478b-89d5-3d7607702b8e
title: Aplicando as principais atualizações por meio da aplicação de patch na instalação local do produto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 043d106ed9f8d6455ab4412959b70854a526a4e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828071"
---
# <a name="applying-major-upgrades-by-patching-the-local-installation-of-the-product"></a>Aplicando as principais atualizações por meio da aplicação de patch na instalação local do produto

Uma atualização importante pode ser aplicada a um aplicativo por meio da aplicação de patch na instalação local do aplicativo a partir da linha de comando ou usando um executável.

> [!Note]  
> Não é recomendável fornecer uma atualização importante como um pacote de patch porque um pacote de patch de atualização importante não pode ser sequenciado com outras atualizações e porque o patch não é um [patch desinstalável](uninstallable-patches.md). O utilitário de [Msimsp.exe](msimsp-exe.md) não pode ser usado para gerar um pacote de patch que aplica uma atualização importante. Em vez disso, aplique atualizações importantes, conforme descrito em [aplicando as principais atualizações instalando o produto](applying-major-upgrades-by-installing-the-product.md).

 

**Para aplicar um patch de atualização importante a uma instalação local do produto**

1.  Inicie a instalação do patch na linha de comando ou usando um executável. Para iniciar a partir da linha de comando, use msiexec/p patch. msp. Para iniciar a partir de um executável, chame [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) ou o [**método ApplyPatch**](installer-applypatch.md) e forneça os mesmos argumentos de linha de comando.
2.  Ao aplicar patch na instalação de um cliente, o instalador ignora a origem da instalação e prossegue para corrigir os arquivos que já estão instalados no computador do usuário.
3.  O instalador altera todos os componentes com patches marcados como executar da origem para execução local. Os usuários não poderão executar esses componentes da origem desde que o patch permaneça no computador.
4.  O instalador adiciona todas as transformações usadas para atualizar o arquivo. msi ou adiciona informações específicas do patch ao perfil do usuário.
5.  O instalador armazena em cache o arquivo. msi no computador do usuário para que ele possa executar a instalação sob demanda, reinstalar e reparar o aplicativo. Depois que um patch é aplicado a uma instalação autônoma, o instalador faz referência a duas ou mais listas de origem a arquivos externos: uma para a fonte original e outra para cada patch que foi aplicado.

 

 



