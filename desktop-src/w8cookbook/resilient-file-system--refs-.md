---
title: Sistema de arquivos resiliente
description: Sistema de arquivos resiliente
ms.assetid: 6E5532F9-64BC-4DD7-9873-3FE4E4DE2DD0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dba011dcdd3cd39280e0a79d0b325f9e75d6b64
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "104008543"
---
# <a name="resilient-file-system"></a>Sistema de arquivos resiliente

## <a name="platform"></a>Plataforma

**Servidores** – Windows Server 2012 

## <a name="description"></a>Descrição

O ReFS (sistema de arquivos resiliente) é um novo sistema de arquivos local. Ela maximiza a disponibilidade dos dados, apesar dos erros que, historicamente, causam perda de dados ou tempo de inatividade. A integridade dos dados garante que os dados críticos dos negócios sejam protegidos contra erros e disponíveis quando necessário. Sua arquitetura foi projetada para fornecer escalabilidade e desempenho em uma época de crescimento constante de tamanhos de conjuntos de dados e cargas de trabalho dinâmicas.

Os principais recursos do ReFS são:

-   **Integridade**: ReFS armazena dados para que eles sejam protegidos de muitos dos erros comuns que podem causar perda de dados. Os metadados do sistema de arquivos são sempre protegidos. Opcionalmente, os dados do usuário podem ser protegidos em uma base por volume, por diretório ou por arquivo. Se ocorrer corrupção, o ReFS poderá detectar e, quando configurado com espaços de armazenamento, corrigir automaticamente o dano. No caso de um erro do sistema, o ReFS foi projetado para se recuperar rapidamente desse erro, sem perda de dados do usuário.
-   **Disponibilidade**: ReFS foi projetado para priorizar a disponibilidade de dados. Com ReFS, se ocorrer corrupção e não puder ser reparado automaticamente, o processo de resgate online será localizado na área de corrupção, não exigindo nenhum tempo de inatividade de volume. Em resumo, se a corrupção ocorrer, ReFS permanecerá online.
-   **Escalabilidade**: ReFS foi projetado para os tamanhos de conjunto de dados atuais e os tamanhos de conjunto de dados de amanhã; Ele é otimizado para alta escalabilidade.
-   **Compatibilidade de aplicativos**: para maximizar o AppCompat, o ReFS dá suporte a um subconjunto de recursos NTFS, além de APIs do Win32 amplamente adotadas.
-   **Identificação de erro proativo**: os recursos de integridade de ReFS são aproveitados por um verificador de integridade de dados (um "scrubbing") que examina periodicamente o volume, tenta identificar a corrupção latente e, em seguida, dispara proativamente um reparo desses dados corrompidos.

## <a name="resources"></a>Recursos

-   [Postagem do blog criando o Windows 8 – criando o sistema de arquivos da próxima geração para Windows: ReFS](/archive/blogs/b8/building-the-next-generation-file-system-for-windows-refs)
-   [Compatibilidade de aplicativos e ReFS](https://www.microsoft.com/download/en/details.aspx?id=29043)

 

 