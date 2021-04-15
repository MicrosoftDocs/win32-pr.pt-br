---
description: O componente principal da interface de impressão é o spooler de impressão.
ms.assetid: 36ffb001-78e2-4fa0-8241-3891493ac02d
title: Spooler de impressão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dfcc6ea2e46c06b5e51032a4c43f46df7f07c04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104505901"
---
# <a name="print-spooler"></a>Spooler de impressão

O componente principal da interface de impressão é o spooler de impressão. O spooler de impressão é um arquivo executável que gerencia o processo de impressão. O gerenciamento de impressão envolve a recuperação do local do driver de impressora correto, o carregamento desse driver, o spool de chamadas de função de alto nível em um trabalho de impressão, o agendamento do trabalho de impressão para impressão e assim por diante. O spooler é carregado na inicialização do sistema e continua a ser executado até que o sistema operacional seja desligado.

Aplicativos que imprimem criam um contexto de dispositivo de impressora (DC). Quando um aplicativo cria um controlador de domínio de impressora, o spooler executa as tarefas necessárias, como determinar o local do driver de impressora necessário e, em seguida, carregar esse driver. O spooler de impressão também determina o tipo de dados usado para registrar o trabalho de impressão.

O spooler de impressão dá suporte aos seguintes tipos de dados:

-   Metarquivo avançado (EMF).
-   Texto ASCII.
-   Dados brutos, que incluem tipos de dados de impressora, como PostScript, PCL e tipos de dados personalizados.

Os tipos de dados personalizados podem ser adicionados ao spooler instalando drivers de impressora e processadores de impressão adicionais. Um trabalho de impressão é um documento armazenado internamente e codificado usando um dos tipos de dados com suporte, e um trabalho de impressão pode conter uma ou mais páginas de saída. O trabalho de impressão pode consistir em várias formas; por exemplo, um trabalho pode consistir em um envelope e três páginas de papel A4. Um trabalho de impressão é definido (ou entre colchetes) pelas funções [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) e [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) .

O tipo de dados padrão para um trabalho de impressão é o metarquivo avançado. Um registro EMF é uma estrutura compacta usada para armazenar comandos de saída de texto, comandos de gráficos de varredura e assim por diante. Quando um aplicativo chama [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca), o spooler cria um arquivo de spool e um arquivo de dados e começa a armazenar os registros EMF no arquivo de spool. Cada vez que o aplicativo chama uma das funções de desenho do GDI, um ou mais novos registros EMF são criados e armazenados no arquivo de spool. O spool e os arquivos de dados são criados em um diretório do sistema operacional. O spooler usa o arquivo de spool para armazenar registros EMF e usa o arquivo de dados para registrar o tipo de formulário, o tipo de dados para o trabalho de impressão, a impressora de destino e assim por diante. O spooler exclui esses arquivos quando o trabalho foi impresso com êxito.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Metarquivos de formato avançado](/windows/desktop/gdi/enhanced-format-metafiles)
</dt> </dl>

 

 
