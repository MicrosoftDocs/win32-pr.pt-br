---
title: Estruturas e uniões de BITS
description: As interfaces Serviço de Transferência Inteligente em Segundo Plano (BITS) usam as seguintes estruturas.
ms.assetid: a1b8b4a1-77d6-46ac-96d5-6a0c99cfc643
ms.topic: article
ms.date: 02/21/2019
ms.openlocfilehash: 93763daa73bc96e12dd27b862d75fbb23869c20f
ms.sourcegitcommit: 31f494fef71b63ad411b86b22b4cc01af6e37c8d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/20/2019
ms.locfileid: "104292900"
---
# <a name="bits-structures-and-unions"></a>Estruturas e uniões de BITS

As [interfaces](bits-interfaces.md) serviço de transferência inteligente em segundo plano (bits) usam as seguintes estruturas.

## <a name="in-this-section"></a>Nesta seção

| Tópico | Descrição |
|-|-|
| [**BG_AUTH_CREDENTIALS**](/windows/win32/api/bits1_5/ns-bits1_5-bg_auth_credentials) | Identifica o destino (proxy ou servidor), o esquema de autenticação e as credenciais do usuário a serem usadas para solicitações de autenticação de usuário. A estrutura é passada para o [método IBackgroundCopyJob2:: SetCredentials](/windows/win32/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials). |
| [**BG_AUTH_CREDENTIALS_UNION**](/windows/win32/api/bits1_5/ns-bits1_5-bg_auth_credentials_union) | Identifica as credenciais a serem usadas para o esquema de autenticação especificado na [estrutura de BG_AUTH_CREDENTIALS](/windows/win32/api/bits1_5/ns-bits1_5-bg_auth_credentials). |
| [**BG_BASIC_CREDENTIALS**](/windows/win32/api/bits1_5/ns-bits1_5-bg_basic_credentials) | Identifica o nome de usuário e a senha a serem autenticados. |
| [**BG_FILE_INFO**](/windows/win32/api/bits/ns-bits-bg_file_info) | Fornece os nomes local e remoto do arquivo a ser transferido. |
| [**BG_FILE_PROGRESS**](/windows/win32/api/bits/ns-bits-bg_file_progress) | Fornece informações de progresso relacionadas a arquivos, como o número de bytes transferidos. |
| [**BG_FILE_RANGE**](/windows/win32/api/bits2_0/ns-bits2_0-bg_file_range) | Identifica um intervalo de bytes para baixar de um arquivo. |
| [**BG_JOB_PROGRESS**](/windows/win32/api/bits/ns-bits-bg_job_progress) | Fornece informações de progresso relacionadas ao trabalho, como o número de bytes e arquivos transferidos. Para trabalhos de carregamento, o progresso se aplica ao arquivo de carregamento, não ao arquivo de resposta. Para exibir o progresso do arquivo de resposta, consulte a [estrutura de BG_JOB_REPLY_PROGRESS](/windows/win32/api/bits1_5/ns-bits1_5-bg_job_reply_progress). |
| [**BG_JOB_REPLY_PROGRESS**](/windows/win32/api/bits1_5/ns-bits1_5-bg_job_reply_progress) | Fornece informações de progresso relacionadas à parte de resposta de um trabalho de resposta de upload. |
| [**BG_JOB_TIMES**](/windows/win32/api/bits/ns-bits-bg_job_times) | Fornece carimbos de data/hora relacionados ao trabalho. |
| [**União de BITS_FILE_PROPERTY_VALUE**](/windows/win32/api/bits5_0/ns-bits5_0-bits_file_property_value) | Fornece o valor da propriedade de um arquivo BITS. |
| [**BITS_JOB_PROPERTY_VALUE**](/windows/win32/api/bits5_0/ns-bits5_0-bits_file_property_value) | Fornece o valor da Propriedade do trabalho BITS com base no valor da [enumeração BITS_JOB_PROPERTY_ID](/windows/win32/api/bits5_0/ne-bits5_0-bits_job_property_id). |
