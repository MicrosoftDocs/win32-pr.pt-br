---
description: O servidor de pipe especifica os modos de acesso, sobreposição e write-through do pipe no parâmetro dwOpenMode da função CreateNamedPipe. Os clientes do pipe podem especificar esses modos abertos para seus identificadores de pipe usando a função CreateFile.
ms.assetid: 88824566-93c7-4941-a4fc-3a7ae9a332a4
title: Modos abertos do pipe nomeado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97f51d41ea98a47a269634b06ccdad869bd649fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922655"
---
# <a name="named-pipe-open-modes"></a>Modos abertos do pipe nomeado

O servidor de pipe especifica os modos de acesso, sobreposição e write-through do pipe no parâmetro *dwOpenMode* da função [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) . Os clientes do pipe podem especificar esses modos abertos para seus identificadores de pipe usando a função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .

## <a name="access-mode"></a>Modo de acesso

Definir o modo de acesso do pipe é equivalente a especificar o acesso de leitura ou gravação associado às alças do servidor de pipe. A tabela a seguir mostra o direito de acesso genérico equivalente para cada modo de acesso que você pode especificar com [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea).



| Modo de acesso            | Direito de acesso genérico equivalente |
|------------------------|---------------------------------|
| \_entrada de acesso de pipe \_  | \_leitura genérica                   |
| \_saída de acesso de pipe \_ | \_gravação genérica                  |
| \_duplex de acesso de pipe \_   | gravação genérica de \_ leitura genérica \| \_ |



 

Se o servidor de pipe criar um pipe com acesso de PIPE de \_ \_ entrada, o pipe será somente leitura para o servidor de pipe e somente gravação para o cliente de pipe. Se o servidor de pipe criar um pipe com \_ saída de acesso de pipe \_ , o pipe será somente gravação para o servidor de pipe e somente leitura para o cliente do pipe. Um pipe criado com o \_ duplex de acesso de pipe \_ é de leitura/gravação para o servidor de pipe e o cliente de pipe.

Os clientes de pipe que usam [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para se conectar a um pipe nomeado devem especificar um direito de acesso no parâmetro *dwDesiredAccess* que seja compatível com o modo de acesso especificado pelo servidor de pipe. Por exemplo, um cliente deve especificar \_ o acesso de leitura genérico para abrir um identificador para um pipe que o servidor de pipe criado com acesso de saída de pipe \_ \_ . Os modos de acesso devem ser os mesmos para todas as instâncias de um pipe.

Para ler atributos de pipe, como o modo de leitura ou o modo de bloqueio, o identificador de pipe deve ter o \_ direito de acesso aos atributos de leitura de arquivo \_ ; para gravar os atributos de pipe, o identificador de pipe deve ter o \_ direito de acesso atributos de gravação de arquivo \_ . Esses direitos de acesso podem ser combinados com o direito de acesso genérico apropriado para o pipe: \_ leitura genérica com \_ \_ atributos de gravação de arquivo para um pipe somente leitura ou \_ gravação genérica com \_ \_ atributos de leitura de arquivo para um pipe somente gravação. Restringir os direitos de acesso dessa maneira fornece melhor segurança para o pipe.

## <a name="overlapped-mode"></a>Modo sobreposto

No modo sobreposto, as funções que executam operações longas de leitura, gravação e conexão podem retornar imediatamente. Isso permite que o thread execute outras operações enquanto uma operação demorada está em execução em segundo plano. Para especificar o modo sobreposto, use o \_ sinalizador de sinalizador de arquivo \_ sobreposto. Para obter mais informações, consulte [entrada e saída síncronas e sobrepostas](synchronous-and-overlapped-input-and-output.md).

A função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) permite que o cliente de pipe defina o modo sobreposto ( \_ sinalizador de arquivo \_ sobreposto) para seus identificadores de pipe usando o parâmetro *dwFlagsAndAttributes* .

## <a name="write-through-mode"></a>Modo de Write-Through

Especifique o modo de write-through com gravação de sinalizador de arquivo \_ \_ \_ . Esse modo afeta somente operações de gravação em pipes de tipo de byte entre clientes de pipe e servidores de pipe em computadores diferentes. No modo de write-through, as funções que gravam em um pipe nomeado não retornam até que os dados sejam transmitidos pela rede e para o buffer do pipe no computador remoto. O modo de write-through é útil para aplicativos que exigem sincronização para cada operação de gravação.

Se o modo write-through não estiver habilitado, o sistema aprimorará a eficiência das operações de rede armazenando dados em buffer até que um número mínimo de bytes seja acumulado ou até que um período de tempo máximo tenha decorrido. O armazenamento em buffer permite que o sistema combine várias operações de gravação em uma única transmissão de rede. Isso significa que uma operação de gravação pode ser concluída com êxito depois que o sistema coloca os dados no buffer de saída, mas antes que o sistema o transmita pela rede.

A função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) permite que o cliente de pipe defina o modo de write-through ( \_ gravação de sinalizador de arquivo \_ \_ ) para seus identificadores de pipe usando o parâmetro *dwFlagsAndAttributes* . O modo de write-through de um identificador de pipe não pode ser alterado após a criação do identificador de pipe. O modo write-through pode ser diferente para identificadores de servidor e cliente para a mesma instância de pipe.

Um cliente de pipe pode usar a função [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) para controlar o número de bytes e o período de tempo limite antes da transmissão para um pipe no qual o modo de write-through está desabilitado. Para um pipe somente leitura, o identificador de pipe deve ser aberto com os \_ direitos de acesso de atributos de leitura e gravação de arquivo genéricos \_ \_ .

 

 
