---
description: A API (interface de programação de aplicativo) da instalação do fornece um conjunto de funções que seu aplicativo de instalação pode chamar para executar operações de instalação. Essas funções de instalação funcionam com arquivos INF do Windows para fornecer a seguinte funcionalidade de instalação.
ms.assetid: 58201596-cb8c-480a-abef-896c1f9ef098
title: Visão geral
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a32b99c6079fdb61fd6bfd0033ffccb9ebb7b922
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748381"
---
# <a name="overview"></a>Visão geral

A API (interface de programação de aplicativo) da instalação do fornece um conjunto de funções que seu aplicativo de instalação pode chamar para executar operações de instalação. Essas funções de instalação funcionam com arquivos INF do Windows para fornecer a seguinte funcionalidade de instalação.



| Para obter informações sobre                       | Consulte                                                                                                                                                                         |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Enfileirando arquivos                               | [Filas de arquivos](file-queues.md)                                                                                                                                              |
| Instalando arquivos                            | [Filas de arquivos](file-queues.md)<br/> [Aplicativos de instalação](setup-applications.md)<br/> [Criando aplicativos de instalação](creating-setup-applications.md)<br/> |
| Tratamento de erros e solicitação de mídia     | [Solicitação de disco e tratamento de erros](disk-prompting-and-error-handling.md)                                                                                                  |
| Atualizando entradas do registro                   | [Aplicativos de instalação](setup-applications.md)                                                                                                                                |
| Registrando arquivos instalados                     | [Log de arquivo](file-log.md)                                                                                                                                                    |
| Armazenando os caminhos de origem usados mais recentemente | [Lista de origem MRU](mru-source-list.md)                                                                                                                                      |



 

As versões Unicode e ANSI estão disponíveis para a maioria das funções de instalação. Os arquivos de texto Unicode devem conter a marca de ordem de byte 0xFEFF padrão para permitir que as funções de instalação identifiquem o arquivo como texto Unicode.

Embora a API de instalação ofereça suporte à solicitação de novas mídias e caixas de diálogo básicas de tratamento de erros, as funções de instalação não fornecem a funcionalidade do assistente ou uma interface de usuário genérica.

Os desenvolvedores devem considerar se podem usar [Windows Installer](/windows/desktop/Msi/windows-installer-portal) para instalar seus aplicativos em vez da API de instalação. Windows Installer reduz o TCO (custo total de propriedade) para seus clientes, permitindo que eles instalem e configurem seus produtos e aplicativos com eficiência. O instalador também pode fornecer a seus produtos novos recursos para anunciar recursos sem instalá-los, instalar produtos sob demanda e adicionar personalizações do usuário.

 

