---
description: Instala drivers de dispositivo de programas com um script de configuração e arquivos INF. Escreva um programa de instalação para configuração de dispositivo e instalação de driver. Essa API não é mais recomendada para a finalidade de instalar aplicativos de software.
ms.assetid: 96a9e472-9b92-4976-9379-dc0c96524963
title: API de instalação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6101c2673e72095d0cf4ebe59c1cece83449d647
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756546"
---
# <a name="setup-api"></a>API de instalação

## <a name="purpose"></a>Finalidade

A API de instalação fornece um conjunto de funções que um aplicativo de instalação chama para executar operações de instalação.

## <a name="where-applicable"></a>Quando aplicável

Essas funções de instalação estão disponíveis para desenvolver um aplicativo de instalação. A API de instalação não deve mais ser usada para instalar aplicativos. Em vez disso, use o [Windows Installer](/windows/desktop/Msi/windows-installer-portal)para desenvolver instaladores de aplicativos. A API de instalação continua a ser usada para instalar drivers de dispositivo.

A API de instalação destina-se ao desenvolvimento de aplicativos de estilo de área de trabalho.

## <a name="developer-audience"></a>Público de desenvolvedores

Um desenvolvedor poderá usar a API de instalação se seu aplicativo de instalação exigir a seguinte funcionalidade:

-   Enfileiramento de arquivos.
-   Instalação de arquivos.
-   Tratamento de erros de instalação e solicitação de mídia.
-   Atualizando entradas do registro.
-   Registro de arquivos conforme eles são instalados.
-   Armazenamento dos caminhos de origem usados mais recentemente.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

Para obter informações sobre quais sistemas operacionais são necessários para usar uma função específica, consulte a seção requisitos da documentação da função.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                 | Descrição                                                                                 |
|---------------------------------------|---------------------------------------------------------------------------------------------|
| [Visão geral](overview.md)<br/>   | Informações gerais sobre a API de instalação.<br/>                                             |
| [Referência](reference.md)<br/> | Documentação de tipos de dados, estruturas, funções e notificações da API de instalação.<br/> |



 

 

