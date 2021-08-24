---
title: Funções de segurança
description: As funções de segurança de gerenciamento de rede obtêm e definem descritores de segurança para raízes autônomas e baseadas em domínio do DFS.
ms.assetid: 90860842-0f4d-49ad-b835-50305328a050
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d31611aa650bb55ecdc29af468e0ef784b670555b247d536d27b397de356f4ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119677796"
---
# <a name="security-functions"></a>Funções de segurança

As funções de segurança de gerenciamento de rede obtêm e definem descritores de segurança para raízes autônomas e baseadas em domínio do DFS.

As funções de segurança do DFS são listadas a seguir.

| Função                                                               | Descrição                                                                                                          |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**NetDfsGetSecurity**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetsecurity)                         | Obtém o descritor de segurança para o objeto raiz da raiz DFS especificada.                                       |
| [**NetDfsSetSecurity**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetsecurity)                         | Localiza o objeto raiz para a raiz DFS especificada e define o descritor de segurança fornecido nele.                  |
| [**NetDfsGetStdContainerSecurity**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetftcontainersecurity) | Obtém o descritor de segurança para o objeto de contêiner da raiz autônoma do DFS especificada.                      |
| [**NetDfsSetStdContainerSecurity**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetstdcontainersecurity) | Localiza o objeto de contêiner para a raiz autônoma do DFS especificada e define o descritor de segurança fornecido nele. |
| [**NetDfsGetFtContainerSecurity**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetftcontainersecurity)   | Obtém o descritor de segurança para o objeto de contêiner da raiz de domínio do DFS especificada.                           |
| [**NetDfsSetFtContainerSecurity**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetftcontainersecurity)   | Localiza o objeto de contêiner para a raiz de domínio do DFS especificada e define o descritor de segurança fornecido nele.      |
