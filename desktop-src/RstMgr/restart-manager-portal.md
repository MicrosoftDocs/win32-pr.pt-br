---
title: Gerenciador de Reinicialização
description: Escreva instaladores personalizados para eliminar reinicializações do sistema necessárias para concluir a atualização de um arquivo em uso. Desligue e reinicie todos os serviços de sistema críticos de programas.
ms.assetid: 44b7975a-0093-4c8f-9a14-2a6bfd7a68a5
keywords:
- Reiniciar Mgr do Gerenciador de Reinicialização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d67910428fb781a5ddf8e2c719d30f2f0488e11d6b07daad1770788e8ad5f5ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010094"
---
# <a name="restart-manager"></a>Gerenciador de Reinicialização

## <a name="purpose"></a>Finalidade

A API do Gerenciador de Reinicialização pode eliminar ou reduzir o número de reinicializações do sistema necessárias para concluir uma instalação ou atualização. O principal motivo pelo qual as atualizações de software exigem uma reinicialização do sistema durante uma instalação ou atualização é que alguns dos arquivos que estão sendo atualizados estão sendo usados atualmente por um aplicativo ou serviço em execução. O Gerenciador de Reinicialização permite que todos os serviços [críticos do](critical-system-services.md) sistema sejam desligados e reiniciados. Isso libera arquivos que estão em uso e permite que as operações de instalação sejam concluídas.

## <a name="where-applicable"></a>Quando aplicável

A DLL do Gerenciador de Reinicialização exporta uma interface C pública que pode ser carregada por instaladores padrão ou personalizados. O instalador pode usar o Gerenciador de Reinicialização para registrar arquivos que devem ser substituídos durante a instalação de um aplicativo ou atualização. Em seguida, durante uma atualização ou instalação subsequente, o instalador pode usar o Gerenciador de Reinicialização para determinar quais arquivos não podem ser atualizados porque estão em uso no momento. O Restart Manager pode desligar e reiniciar os serviços ou aplicativos não críticos que estão usando esses arquivos no momento. Os instaladores podem direcionar o Gerenciador de Reinicialização para desligar e reiniciar aplicativos ou serviços com base no arquivo em uso, na ID do processo (PID) ou no nome curto de um serviço Windows.

O Gerenciador de Reinicialização destina-se ao desenvolvimento de aplicativos de estilo de área de trabalho.

## <a name="developer-audience"></a>Público de desenvolvedores

Esta documentação destina-se a desenvolvedores de aplicativos de instalação que querem aproveitar os recursos do instalador no Windows Vista ou Windows Server 2008. Os aplicativos que usam o [Windows Installer](/windows/desktop/Msi/windows-installer-portal) versão 4.0 para instalação e manutenção usam automaticamente o Gerenciador de Reinicialização para reduzir as reinicializações do sistema. Os instaladores personalizados também podem ser projetados para chamar a API do Gerenciador de Reinicialização para desligar e reiniciar aplicativos e serviços. Nos casos em que uma reinicialização do sistema é inevitável, os instaladores podem usar a API do Gerenciador de Reinicialização para agendar reinicializações de forma que minimize a interrupção do fluxo de trabalho do usuário.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

A API do Restart Manager está disponível a partir do Windows Vista e Windows Server 2008. O Restart Manager consiste em uma única DLL que os aplicativos podem carregar para acessar a API do Restart Manager.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                 | Descrição                                                     |
|-----------------------------------------------------------------------|-----------------------------------------------------------------|
| [Sobre o Restart Manager](about-restart-manager.md)<br/>         | Tópicos de visão geral que descrevem o Gerenciador de Reinicialização.<br/>   |
| [Usando o Gerenciador de Reinicialização](using-restart-manager.md)<br/>         | Tópicos de visão geral sobre como usar a API do Gerenciador de Reinicialização.<br/> |
| [Referência do Gerenciador de Reinicialização](restart-manager-reference.md)<br/> | Tópicos de referência para a API do Gerenciador de Reinicialização.<br/>        |



 

 

