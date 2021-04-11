---
description: A proteção de recursos impede a substituição de arquivos e pastas do sistema e chaves do registro essenciais para o sistema operacional. A modificação de recursos protegidos pode causar falha no aplicativo ou no sistema.
ms.assetid: 27df9300-8bea-4748-9acd-2c1625093ece
title: Proteção de Recursos do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cff6c89e99b885256c7dd054a12c6a69795d794c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297092"
---
# <a name="windows-resource-protection"></a>Proteção de Recursos do Windows

## <a name="purpose"></a>Finalidade

O Proteção de Recursos do Windows (WRP) impede a substituição de arquivos de sistema, pastas e chaves do registro essenciais que são instalados como parte do sistema operacional. Ele se tornou disponível a partir do Windows Server 2008 e do Windows Vista. Os aplicativos não devem substituir esses recursos porque eles são usados pelo sistema e por outros aplicativos. A proteção desses recursos impede falhas de aplicativos e do sistema operacional. WRP é o novo nome da WFP (proteção de arquivo do Windows). A WRP protege chaves e pastas do registro, bem como arquivos essenciais do sistema.

## <a name="where-applicable"></a>Quando aplicável

Todos os aplicativos baseados no Windows e seus programas de instalação executados no Windows Server 2008 ou no Windows Vista e em sistemas operacionais posteriores devem estar cientes da WRP. Todos os aplicativos baseados no Windows que são executados no Microsoft Windows Server 2003 ou no Windows XP e seus programas de instalação devem estar cientes do WFP.

## <a name="developer-audience"></a>Público de desenvolvedores

A API WRP foi projetada para uso por programadores C/C++. A API WRP tem duas funções: [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) e [**SfcIsKeyProtected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected).

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

Os aplicativos que usam apenas a função [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) exigem o windows Server 2008, o Windows Vista, o windows Server 2003 ou o Windows XP. Os aplicativos que usam a função [**SfcIsKeyProtected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected) exigem o windows Server 2008 ou o Windows Vista.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                     | Descrição                                 |
|-------------------------------------------------------------------------------------------|---------------------------------------------|
| [Sobre Proteção de Recursos do Windows](about-windows-file-protection.md)<br/>         | Informações gerais sobre WRP.<br/>   |
| [Referência de Proteção de Recursos do Windows](windows-file-protection-reference.md)<br/> | Documentação de referência para WRP.<br/> |



 

 

 




