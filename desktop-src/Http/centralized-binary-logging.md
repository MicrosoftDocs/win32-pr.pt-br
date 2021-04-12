---
title: Log binário centralizado
description: O log binário centralizado é um tipo de registro no servidor que pode ser habilitado na sessão do servidor.
ms.assetid: 957a7bc4-9db3-4153-b0a9-e53b3cc514c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64bc7bdc6f7a5fce78ff66e58b4c50eac36be3f9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104294002"
---
# <a name="centralized-binary-logging"></a>Log binário centralizado

O log binário centralizado é um tipo de registro no servidor que pode ser habilitado na sessão do servidor. O log binário centralizado funciona como uma forma centralizada de registro em log para todos os grupos de URLs criados na sessão do servidor e permite que todos os grupos de URLs na sessão do servidor enviem dados de log binários não formatados para um único arquivo de log. Esse tipo de registro em log só pode ser habilitado na sessão do servidor; Ele não pode ser habilitado no grupo de URLs.

## <a name="when-to-use-centralized-binary-logging"></a>Quando usar o log binário centralizado

Quando a sessão do servidor tem inúmeros grupos de URLs, o processo de criação de centenas de arquivos de log formatados para grupos de URL individuais e a gravação dos dados de log em um disco pode consumir rapidamente recursos valiosos de CPU e memória, criando assim problemas de desempenho e escalabilidade. O log binário centralizado minimiza a quantidade de recursos do sistema usados para registro em log, enquanto, ao mesmo tempo, fornece dados de log detalhados para organizações que o exigem.

O log binário centralizado é uma propriedade de sessão de servidor que, quando habilitada, configura o registro em log para todos os grupos de URLs na sessão do servidor. Quando o log binário centralizado está habilitado, os dados não podem ser gravados ou formatados para grupos de URL individuais. O arquivo de log de log binário centralizado tem uma extensão de nome de arquivo (. IBL) de log binário da Internet. Essa extensão de nome de arquivo garante que os utilitários de texto não tentem abrir e ler o arquivo de log de log binário central.

## <a name="extracting-data-from-the-centralized-binary-log-file"></a>Extraindo dados do arquivo de log binário centralizado

As etapas a seguir são executadas para extrair dados de um arquivo de log bruto:

-   Crie uma ferramenta que localize e extraia os dados desejados do arquivo bruto e converta os dados em texto formatado. Você pode exibir um arquivo de cabeçalho e descrições de formato de arquivo de log no Software Development Kit do IIS 6,0 no MSDN.
-   Use a ferramenta Log Parser para extrair dados do arquivo bruto. A ferramenta Log Parser e a documentação do usuário que o acompanham estão incluídas nas ferramentas do kit de recursos do IIS 6,0.

## <a name="centralized-binary-logging-file-format"></a>Formato de arquivo de log binário centralizado

O arquivo de log de registro binário centralizado bruto é composto de registros de comprimento fixo ou registros de índice que contêm identificadores de cadeia de caracteres. Os registros de índice aparecem porque, em um esforço para registrar o máximo possível de informações, os campos de cadeia de caracteres de comprimento variável são substituídos por identificadores numéricos — os índices — que mapeiam a cadeia de caracteres de comprimento variável para o identificador registrado.

O arquivo de log bruto não é legível e não pode ser lido usando os analisadores de log mais disponíveis. Para extrair dados de um arquivo de log bruto, você pode criar uma ferramenta que localiza e extrai os dados e, em seguida, converte-os em texto formatado.

Para obter mais informações, consulte [registro em log binário centralizado](/previous-versions/windows/it-pro/windows-server-2003/cc758733(v=ws.10)) no Microsoft TechNet.

 

 