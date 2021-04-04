---
title: Gerenciador de reinicialização
description: Escreva instaladores personalizados para eliminar reinicializações do sistema que são necessárias para concluir a atualização de um arquivo em uso. Desligue e reinicie todos os serviços do sistema, exceto os críticos, dos programas.
ms.assetid: 44b7975a-0093-4c8f-9a14-2a6bfd7a68a5
keywords:
- Gerenciador de reinicialização do reinício
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1244cff7bc22fd2e7b6d2540051bd0984596086
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007885"
---
# <a name="restart-manager"></a>Gerenciador de reinicialização

## <a name="purpose"></a>Finalidade

A API do Gerenciador de reinicialização pode eliminar ou reduzir o número de reinicializações do sistema que são necessárias para concluir uma instalação ou atualização. O principal motivo pelo qual as atualizações de software exigem uma reinicialização do sistema durante uma instalação ou atualização é que alguns dos arquivos que estão sendo atualizados estão sendo usados no momento por um aplicativo ou serviço em execução. O Gerenciador de reinicialização permite que todos, exceto os [serviços críticos do sistema](critical-system-services.md) sejam desligados e reiniciados. Isso libera os arquivos que estão em uso e permite que as operações de instalação sejam concluídas.

## <a name="where-applicable"></a>Quando aplicável

O DLL do Gerenciador de reinicialização exporta uma interface C pública que pode ser carregada por instaladores padrão ou personalizados. O instalador pode usar o Gerenciador de reinicialização para registrar os arquivos que devem ser substituídos durante a instalação de um aplicativo ou atualização. Em seguida, durante uma atualização ou instalação subsequente, o instalador pode usar o Gerenciador de reinicialização para determinar quais arquivos não podem ser atualizados porque estão em uso no momento. O Gerenciador de reinicialização pode desligar e reiniciar os serviços não críticos ou os aplicativos que estão usando esses arquivos no momento. Os instaladores podem instruir o Gerenciador de reinicialização a desligar e reiniciar aplicativos ou serviços com base no arquivo em uso, na ID do processo (PID) ou no nome curto de um serviço do Windows.

O Gerenciador de reinicialização destina-se ao desenvolvimento de aplicativos de estilo de área de trabalho.

## <a name="developer-audience"></a>Público de desenvolvedores

Esta documentação destina-se a desenvolvedores de aplicativos de instalação que desejam aproveitar os recursos do instalador no Windows Vista ou no Windows Server 2008. Os aplicativos que usam o [Windows Installer](/windows/desktop/Msi/windows-installer-portal) versão 4,0 para instalação e manutenção automaticamente usam o Gerenciador de reinicialização para reduzir as reinicializações do sistema. Instaladores personalizados também podem ser criados para chamar a API do Gerenciador de reinicialização para desligar e reiniciar aplicativos e serviços. Nos casos em que uma reinicialização do sistema é inevitável, os instaladores podem usar a API do Gerenciador de reinicialização para agendar reinicializações de forma a minimizar a interrupção do fluxo de trabalho do usuário.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

A API do Gerenciador de reinicialização está disponível a partir do Windows Vista e do Windows Server 2008. O Gerenciador de reinicialização consiste em uma única DLL que os aplicativos podem carregar para acessar a API do Gerenciador de reinicialização.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                 | Descrição                                                     |
|-----------------------------------------------------------------------|-----------------------------------------------------------------|
| [Sobre o Gerenciador de reinicialização](about-restart-manager.md)<br/>         | Tópicos de visão geral que descrevem o Gerenciador de reinicialização.<br/>   |
| [Usando o Gerenciador de reinicialização](using-restart-manager.md)<br/>         | Tópicos de visão geral sobre como usar a API do Gerenciador de reinicialização.<br/> |
| [Referência do Gerenciador de reinicialização](restart-manager-reference.md)<br/> | Tópicos de referência para a API do Gerenciador de reinicialização.<br/>        |



 

 

