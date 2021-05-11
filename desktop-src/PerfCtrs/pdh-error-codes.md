---
description: Todas as funções de PDH (Auxiliar de Dados de Desempenho) retornam um valor do tipo \_ PDH STATUS.
ms.assetid: ea67d798-81db-44ad-b0fb-24e0c3be7388
title: Códigos de erro de auxiliar de dados de desempenho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e24a5bb82aafa3e4a29bd24c087826bb5ead5e
ms.sourcegitcommit: 9db18b0737bda194728fe387f336c92361f1b418
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "109690373"
---
# <a name="performance-data-helper-error-codes"></a>Códigos de erro de auxiliar de dados de desempenho

Todas as funções do PDH (Auxiliar de Dados de Desempenho) retornam um valor do tipo **\_ PDH STATUS.** Se a função for bem-sucedida, o valor de retorno será `ERROR_SUCCESS` . Caso contrário, a função retornará [um código de erro do sistema](/windows/desktop/Debug/system-error-codes) ou um código de erro PDH. Para recuperar o texto de descrição do erro em seu aplicativo, use a [**função FormatMessage,**](/windows/desktop/api/winbase/nf-winbase-formatmessage) conforme mostrado no exemplo a seguir.

```C++
#include <windows.h>
#include <stdio.h>
#include <pdhmsg.h>

void main(void)
{
    HANDLE hPdhLibrary = NULL;
    LPWSTR pMessage = NULL;
    DWORD dwErrorCode = PDH_PLA_ERROR_ALREADY_EXISTS;

    hPdhLibrary = LoadLibrary(L"pdh.dll");
    if (NULL == hPdhLibrary)
    {
        wprintf(L"LoadLibrary failed with %lu\n", GetLastError());
        return;
    }

    if (!FormatMessage(FORMAT_MESSAGE_FROM_HMODULE |
                       FORMAT_MESSAGE_ALLOCATE_BUFFER |
                       FORMAT_MESSAGE_IGNORE_INSERTS,
                       hPdhLibrary,
                       dwErrorCode,
                       0,
                       (LPWSTR)&pMessage,
                       0,
                       NULL))
    {
        wprintf(L"Format message failed with 0x%x\n", GetLastError());
        return;
    }

    wprintf(L"Formatted message: %ls\n", pMessage);
    LocalFree(pMessage);
}
```

Para funções de coleta e formatação de dados, é importante lembrar que o valor de retorno da função indica o êxito ou o erro da chamada de função e não necessariamente o dos dados do contador. Sempre verifique o **membro CStatus** do valor do contador retornado para garantir que os dados retornados são válidos antes de usá-los. Se o valor do **membro CStatus** não indicar êxito, não use os dados.

A tabela a seguir fornece uma lista de códigos de erro específicos ao PDH. Esses valores são definidos no `pdhmsg.h` arquivo de header.

| Código do erro                                                   | Descrição
|--------------------------------------------------------------|------------
| 0x00000000 (DADOS VÁLIDOS DO PDH \_ CSTATUS) \_ \_                       | Os dados retornados são válidos.
| 0x00000001 (PDH \_ CSTATUS \_ NEW \_ DATA)                         | O valor dos dados de retorno é válido e diferente do último exemplo.
| 0x800007D0 (PDH \_ CSTATUS \_ NO \_ MACHINE)                       | Não é possível se conectar ao computador especificado ou o computador está offline.
| 0x800007D1 (PDH \_ CSTATUS \_ NO \_ INSTANCE)                      | A instância especificada não está presente.
| 0x800007D2 (PDH \_ MORE \_ DATA)                                 | Há mais dados a retornar do que caberia no buffer fornecido. Aloque um buffer maior e chame a função novamente.
| 0x800007D3 (PDH \_ CSTATUS \_ item \_ não \_ validado)              | O item de dados foi adicionado à consulta, mas não foi validado nem acessado. Nenhuma outra informação de status sobre este item de dados está disponível.
| 0x800007D4 ( \_ nova tentativa de PDH)                                      | A operação selecionada deve ser repetida.
| 0x800007D5 (PDH \_ sem \_ dados)                                   | Nenhum dado a ser retornado.
| 0x800007D6 ( \_ denominador de cálculo negativo do PDH \_ \_ )                | Foi detectado um contador com um valor de denominador negativo.
| 0x800007D7 ( \_ base de \_ dados negativo de cálculo de PDH \_ )                   | Foi detectado um contador com um valor de base de tempo negativo.
| 0x800007D8 ( \_ valor negativo de cálculo de PDH \_ \_ )                      | Foi detectado um contador com um valor negativo.
| 0x800007D9 ( \_ caixa de diálogo PDH \_ cancelada)                          | O usuário cancelou a caixa de diálogo.
| 0x800007DA ( \_ fim \_ do arquivo de log da PDH \_ \_ )                         | O fim do arquivo de log foi atingido.
| 0x800007DB ( \_ tempo limite de consulta assíncrona de PDH \_ \_ )                      | Tempo limite excedido ao aguardar a finalização do thread de coleção do contador assíncrono.
| 0x800007DC (PDH \_ NÃO PODE DEFINIR FONTE DE DADOS PADRÃO EM TEMPO \_ \_ \_ \_ REAL) | Não é possível alterar a fonte de dados padrão em tempo real do conjunto. Há sessões de consulta em tempo real coletando dados do contador.
| 0xC0000BB8 (PDH \_ CSTATUS \_ NO \_ OBJECT)                        | O objeto especificado não foi encontrado no sistema.
| 0xC0000BB9 (PDH \_ CSTATUS \_ NO \_ COUNTER)                       | Não foi possível encontrar o contador especificado.
| 0xC0000BBA (DADOS INVÁLIDOS DO PDH \_ CSTATUS) \_ \_                     | Os dados retornados não são válidos.
| 0xC0000BBB (FALHA DE \_ ALOCAÇÃO DE MEMÓRIA \_ \_ PDH)                | Uma função PDH não pôde alocar memória temporária suficiente para concluir a operação. Feche alguns aplicativos ou estenda o arquivo de página e repetir a função.
| 0xC0000BBC (PDH \_ INVALID \_ HANDLE)                            | O identificador não é um objeto PDH válido.
| 0xC0000BBD (PDH \_ INVALID \_ ARGUMENT)                          | Um argumento necessário está ausente ou incorreto.
| 0xC0000BBE (FUNÇÃO PDH \_ \_ NÃO \_ ENCONTRADA)                       | Não é possível encontrar a função especificada.
| 0xC0000BBF (PDH \_ CSTATUS \_ NO \_ COUNTERNAME)                   | Nenhum contador foi especificado.
| 0xC0000BC0 (PDH \_ CSTATUS \_ Bad \_ COUNTERNAME)                  | Não é possível analisar o caminho do contador. Verifique o formato e a sintaxe do caminho especificado.
| 0xC0000BC1 ( \_ buffer inválido de PDH \_ )                            | O buffer passado pelo chamador não é válido.
| 0xC0000BC2 (PDH \_ buffer insuficiente \_ )                       | Os dados solicitados são maiores que o buffer fornecido. Não é possível retornar os dados solicitados.
| 0xC0000BC3 (PDH \_ não pode \_ conectar a \_ máquina)                   | Não é possível conectar-se ao computador solicitado.
| 0xC0000BC4 ( \_ caminho inválido da PDH \_ )                              | O caminho do contador especificado não pôde ser interpretado.
| 0xC0000BC5 ( \_ instância inválida do PDH \_ )                          | O nome da instância não pôde ser lido a partir do caminho do contador especificado.
| 0xC0000BC6 ( \_ dados inválidos da PDH \_ )                              | Os dados não são válidos.
| 0xC0000BC7 (PDH \_ sem \_ dados de diálogo \_ )                           | O bloco de dados da caixa de diálogo estava ausente ou não é válido.
| 0xC0000BC8 (PDH \_ não \_ pode \_ ler \_ cadeias de caracteres de nome)                | Não é possível ler o contador e/ou o texto de ajuda do computador especificado.
| 0xC0000BC9 ( \_ erro de criação do arquivo de log PDH \_ \_ \_ )                   | Não é possível criar o arquivo de log especificado.
| 0xC0000BCA (PDH \_ LOG \_ FILE OPEN \_ \_ ERROR)                     | Não é possível abrir o arquivo de log especificado.
| 0xC0000BCB (TIPO DE LOG PDH \_ \_ NÃO \_ \_ ENCONTRADO)                      | O tipo de arquivo de log especificado não foi instalado nesse sistema.
| 0xC0000BCC (PDH \_ NÃO \_ HÁ MAIS \_ DADOS)                             | Não existem mais dados disponíveis.
| 0xC0000BCD (ENTRADA PDH \_ \_ NÃO NO ARQUIVO \_ DE \_ \_ LOG)                  | O registro especificado não foi encontrado no arquivo de log.
| 0xC0000BCE (FONTE DE DADOS PDH \_ \_ É ARQUIVO DE \_ \_ \_ LOG)                | A fonte de dados especificada é um arquivo de log.
| 0xC0000BCF (A FONTE DE DADOS PDH \_ \_ É EM TEMPO \_ \_ \_ REAL)               | A fonte de dados especificada é a atividade atual.
| 0xC0000BD0 (PDH \_ NÃO É POSSÍVEL LER O \_ \_ \_ HEADER DO LOG)                  | Não foi possível ler o header do arquivo de log.
| 0xC0000BD1 (ARQUIVO PDH \_ \_ NÃO \_ ENCONTRADO)                           | Não é possível encontrar o arquivo especificado.
| 0xC0000BD2 (O ARQUIVO PDH \_ \_ JÁ \_ EXISTE)                      | Já existe um arquivo com o nome de arquivo especificado.
| 0xC0000BD3 (PDH \_ NÃO \_ IMPLEMENTADO)                           | A função referenciada não foi implementada.
| 0xC0000BD4 (cadeia de PDH \_ \_ não \_ encontrada)                         | Não é possível localizar a cadeia de caracteres especificada na lista de cadeias de texto de nome de desempenho e de ajuda.
| 0x80000BD5 (PDH \_ não pode \_ Mapear \_ arquivos de nome \_ )                   | Não é possível mapear os arquivos de dados do nome do contador de desempenho. Os dados serão lidos do registro e armazenados localmente.
| 0xC0000BD6 ( \_ formato de log desconhecido de PDH \_ \_ )                       | O formato do arquivo de log especificado não é reconhecido pela DLL PDH.
| 0xC0000BD7 ( \_ \_ comando LOGSVC PDH desconhecido \_ )                   | O valor do comando de serviço de log especificado não é reconhecido.
| 0xC0000BD8 ( \_ consulta PDH \_ LOGSVC \_ não \_ encontrada)                  | A consulta especificada do serviço de log não pôde ser encontrada ou não pôde ser aberta.
| 0xC0000BD9 (PDH \_ LOGSVC \_ não \_ aberto)                        | Não foi possível abrir a chave de serviço de log de dados de desempenho. Isso pode ser devido a privilégios insuficientes ou porque o serviço não foi instalado.
| 0xC0000BDA (erro do PDH \_ WBEM \_ )                                | Ocorreu um erro ao acessar o armazenamento de dados WBEM.
| 0xC0000BDB (PDH \_ acesso \_ negado)                             | Não é possível acessar o computador ou o serviço desejado. Verifique as permissões e a autenticação do serviço de log ou a sessão de usuário interativa nos computadores ou no serviço que está sendo monitorado.
| 0xC0000BDC (arquivo de log de PDH \_ \_ \_ muito \_ pequeno)                      | O tamanho máximo do arquivo de log especificado é muito pequeno para registrar os contadores selecionados. Nenhum dado será registrado nesse arquivo de log. Especifique um conjunto menor de contadores para registrar em log ou um tamanho de arquivo maior e repetir essa chamada.
| 0xC0000BDD (PDH \_ INVALID \_ DATASOURCE)                        | Não é possível se conectar ao Nome da Fonte de Dados ODBC.
| 0xC0000BDE (PDH \_ INVALID \_ SQLDB)                             | O Banco de Dados SQL não contém um conjunto válido de tabelas para o Perfmon.
| 0xC0000BDF (PDH \_ NO \_ COUNTERS)                               | Nenhum contador foi encontrado para este Conjunto de Log do SQL Perfmon.
| 0xC0000BE0 (PDH \_ SQL \_ ALLOC \_ FAILED)                         | Falha na chamada para SQLAllocStmt com %1.
| 0xC0000BE1 (PDH \_ SQL \_ ALLOCCON \_ FAILED)                      | Falha na chamada para SQLAllocConnect com %1.
| 0xC0000BE2 (FALHA NO PDH \_ SQL \_ EXEC \_ \_ DIRECT)                  | Falha na chamada para SQLExecDirect com %1.
| 0xC0000BE3 (FALHA NA BUSCA \_ DO SQL \_ \_ PDH)                         | Falha na chamada para SQLFetch com %1.
| 0xC0000BE4 (PDH \_ SQL \_ ROWCOUNT \_ FALHOU)                      | Falha na chamada para SQLRowCount com %1.
| 0xC0000BE5 (FALHA NOS RESULTADOS DO PDH \_ SQL \_ \_ \_ MAIS)                 | Falha na chamada para SQLMoreResults com %1.
| 0xC0000BE6 ( \_ \_ falha no SQL Connect do PDH \_ )                       | Falha na chamada para SQLConnect com %1.
| 0xC0000BE7 ( \_ \_ falha na associação do SQL PDH \_ )                          | Falha na chamada para SQLBindCol com %1.
| 0xC0000BE8 (PDH \_ não pode \_ conectar o \_ \_ servidor WMI)               | Não é possível conectar ao servidor WMI no computador solicitado.
| 0xC0000BE9 (a \_ coleção do PDH PLA \_ \_ já \_ está em execução)          | Coleção "%1! s!" Já está em execução.
| 0xC0000BEA ( \_ sobreposição de agendamento de erro de PLA da PDH \_ \_ \_ )              | A hora de início especificada é posterior à hora de término.
| 0xC0000BEB (coleção de PLA da PDH \_ \_ \_ não \_ encontrada)                | Coleção "%1! s!" não existe.
| 0xC0000BEC (agenda de erro de Pla de PDH \_ \_ \_ \_ decorrido)              | A hora de término especificada já expirou.
| 0xC0000BED (erro de PLA da PDH \_ \_ \_ nostart)                        | Coleção "%1! s!" não iniciado; Verifique se há erros no log de eventos do aplicativo.
| 0xC0000BEE (o \_ erro de Pla de PDH \_ \_ já \_ existe)                | Coleção "%1!s!" já existe.
| 0xC0000BEF (INCOMPATIBILIDADE DO TIPO DE ERRO PDH \_ \_ \_ \_ PLA)                 | Há uma incompatibilidade no tipo de configurações.
| 0xC0000BF0 (PDH \_ PLA \_ ERROR \_ FILEPATH)                       | As informações especificadas não são resolvidas para um nome de caminho válido.
| 0xC0000BF1 (ERRO DE SERVIÇO \_ PDH \_ \_ PLA)                        | O serviço "Logs de & alertas" não respondeu.
| 0xC0000BF2 (ERRO DE VALIDAÇÃO DE PDH \_ \_ \_ PLA)                     | As informações passadas não são válidas.
| 0x80000BF3 (AVISO DE VALIDAÇÃO DE PDH \_ \_ \_ PLA)                   | As informações passadas não são válidas.
| 0xC0000BF4 (NOME DE ERRO DO PDH \_ PLA \_ MUITO \_ \_ \_ LONGO)                | O nome fornecido é muito longo.
| 0xC0000BF5 (FORMATO DE LOG SQL INVÁLIDO DE \_ \_ \_ \_ PDH)                  | O formato de log do SQL está incorreto. O formato correto é `SQL:<DSN-name>!<LogSet-Name>` .
| 0XC0000BF6 (O CONTADOR PDH \_ \_ JÁ ESTÁ EM \_ \_ CONSULTA)                | O contador de desempenho [**na chamada PdhAddCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera) já foi adicionado à consulta de desempenho. Esse contador é ignorado.
| 0xC0000BF7 (LOG BINÁRIO PDH \_ \_ \_ CORROMPIDO)                       | Não é possível ler informações do contador e dados de arquivos de log binários de entrada.
| 0xC0000BF8 (exemplo de log de PDH \_ \_ \_ muito \_ pequeno)                    | Pelo menos um dos arquivos de log binários de entrada contém menos de dois exemplos de dados.
| 0xC0000BF9 ( \_ so PDH \_ \_ versão posterior)                         | A versão do sistema operacional no computador chamado %1 é posterior à do computador local. Esta operação não está disponível no computador local.
| 0xC0000BFA ( \_ versão anterior do sistema operacional PDH \_ \_ )                       | %1 dá suporte a %2 ou posterior. Verifique a versão do sistema operacional no computador chamado %3.
| 0xC0000BFB ( \_ tempo de acréscimo incorreto do PDH \_ \_ )                    | O arquivo de saída deve conter dados anteriores do que o arquivo a ser anexado.
| 0xC0000BFC ( \_ contador de acréscimo sem correspondência de PDH \_ \_ )                 | Os dois arquivos devem ter contadores idênticos para acrescentar.
| 0xC0000BFD ( \_ \_ falha no ALTER SQL de PDH \_ \_ )                 | Não é possível alterar o layout da tabela de detalhes no banco de dados SQL.
| 0xC0000BFE ( \_ \_ tempo limite de dados perf da consulta PDH \_ \_ )                 | O sistema está ocupado. Tempo limite excedido ao coletar dados do contador. Tente novamente mais tarde ou aumente o valor do registro **collecttime** .
