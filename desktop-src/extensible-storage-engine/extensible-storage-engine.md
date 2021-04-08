---
description: 'Saiba mais sobre: mecanismo de armazenamento extensível'
title: Mecanismo de armazenamento extensível
TOCTitle: Extensible Storage Engine
ms:assetid: 5c485eff-4329-4dc1-aa45-fb66e6554792
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269259(v=EXCHG.10)
ms:contentKeyID: 32765561
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 0ef85de696f52d2220c11b05ed7ada76a70df871
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010675"
---
# <a name="extensible-storage-engine"></a>Mecanismo de armazenamento extensível


_**Aplica-se a:** Windows | Windows Server_

## <a name="extensible-storage-engine"></a>Mecanismo de armazenamento extensível

O ESE (mecanismo de armazenamento extensível) é uma tecnologia de armazenamento de ISAM (método de acesso sequencial) e indexado avançado. O ESE permite que os aplicativos armazenem e recuperem dados de tabelas usando a navegação de cursor indexada ou sequencial. Ele dá suporte a esquemas desnormalizados, incluindo tabelas amplas com várias colunas esparsas, colunas com vários valores e índices esparsos e sofisticados. Ele permite que os aplicativos aproveitem um estado de dados consistente usando a atualização de dados transacional e a recuperação. Um mecanismo de recuperação de falha é fornecido para que a consistência dos dados seja mantida mesmo no caso de uma falha do sistema. Ele fornece transações ACID (duráveis consistentes isoladas) em dados e esquema por meio de um log write-ahead e um modelo de isolamento de instantâneo. As transações no ESE são altamente simultâneas, tornando o ESE útil para aplicativos de servidor. Ele armazena dados em cache para maximizar o acesso de alto desempenho aos dados. Além disso, é leve, tornando-o útil para aplicativos que atendem a funções auxiliares.

O ESE é para uso em aplicativos que exigem um armazenamento de dados estruturado rápido e/ou leve, onde o acesso a arquivos brutos ou o registro não oferece suporte aos requisitos de indexação ou de tamanho de dados do aplicativo.

Ele é usado por aplicativos que nunca armazenam mais de 1 megabyte de dados, e que foram usados em aplicativos com bancos de dado em casos extremos, excedentes a 1 terabyte e, em geral, mais de 50 gigabytes.

Esta documentação destina-se a desenvolvedores que estão familiarizados com o C e C++ e conceitos básicos de banco de dados, como tabelas, colunas, índices, recuperação e transações. O único método de acesso para ESE é a API C descrita nesta documentação.

O mecanismo de armazenamento extensível é um componente do Windows que foi introduzido no Windows 2000. Nem todos os recursos ou APIs estão disponíveis em todas as versões dos sistemas operacionais Windows.

O ESE fornece um mecanismo de armazenamento de modo de usuário que gerencia dados dentro de arquivos binários simples que podem ser acessados por meio das APIs do Windows. O ESE é acessado por meio de uma DLL que é carregada diretamente no processo do aplicativo; nenhum método de acesso remoto é exigido ou fornecido pelo próprio mecanismo de banco de dados. Embora o ESE não tenha nenhum método de acesso remoto ou entre processos, os arquivos de dados usados por ele podem ser fornecidos remotamente usando o protocolo SMB por meio das APIs do Windows, mas isso não é recomendado.

**Observação**  O Windows XP 64-bit Edition é o mesmo que o Windows Server 2003 com a finalidade de determinar o conjunto de recursos do ESE com suporte.

### <a name="notes"></a>Observações

O ESE era conhecido anteriormente como tecnologia de mecanismo conjunta (JET) azul e, com frequência, o termo "JET Blue" ou "JET" é usado de maneira intercambiável com o termo ESE fora desta documentação. No entanto, na verdade, há duas implementações completamente separadas da API do JET, chamada JET Blue e JET Red. O termo "JET" geralmente também é usado para referir-se ao JET Red, que é o mecanismo de banco de dados usado com o acesso ao Microsoft Office. As duas implementações do JET são completamente diferentes, são mantidas separadamente, têm um conjunto de recursos amplamente diferente e não são intercambiáveis. Na documentação do ESE, "JET" refere-se ao ESE ou à API do JET, pois o ESE o implementa. Todas as referências ao JET vermelho sempre serão rotuladas explicitamente como "JET Red".

### <a name="in-this-section"></a>Nesta seção

[Referência do mecanismo de armazenamento extensível](./extensible-storage-engine-reference.md)
