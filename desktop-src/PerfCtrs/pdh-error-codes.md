---
description: Todas as funções PDH (auxiliar de dados de desempenho) retornam um valor do tipo PDH \_ status.
ms.assetid: ea67d798-81db-44ad-b0fb-24e0c3be7388
title: Códigos de erro de auxiliar de dados de desempenho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0417801b4f7a23e48a74201aa48193987a0edee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755065"
---
# <a name="performance-data-helper-error-codes"></a>Códigos de erro de auxiliar de dados de desempenho

Todas as funções PDH (auxiliar de dados de desempenho) retornam um valor do tipo **PDH \_ status**. Se a função for realizada com sucesso, o valor de retorno será `ERROR_SUCCESS` . Caso contrário, a função retorna um código de [erro do sistema](/windows/desktop/Debug/system-error-codes) ou um código de erro PDH. Para recuperar o texto de descrição do erro em seu aplicativo, use a função [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) , conforme mostrado no exemplo a seguir.

```C++
#include <windows.h>
#include <stdio.h>
#include <pdhmsg.h>

void main(void)
{
    HANDLE hPdhLibrary = NULL;
    LPWSTR pMessage = NULL;
    DWORD_PTR pArgs[] = { (DWORD_PTR)L"<collectionname>" };
    DWORD dwErrorCode = PDH_PLA_ERROR_ALREADY_EXISTS;

    hPdhLibrary = LoadLibrary(L"pdh.dll");
    if (NULL == hPdhLibrary)
    {
        wprintf(L"LoadLibrary failed with %lu\n", GetLastError());
        return;
    }

    if (!FormatMessage(FORMAT_MESSAGE_FROM_HMODULE
                       FORMAT_MESSAGE_ALLOCATE_BUFFER
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

Para funções de formatação e de coleta de dados, é importante lembrar que o valor de retorno da função indica o êxito ou o erro da chamada de função e não necessariamente o dos dados do contador. Sempre verifique o membro **CStatus** do valor do contador retornado para garantir que os dados retornados sejam válidos antes de usá-lo. Se o valor do membro **CStatus** não indicar êxito, não use os dados.

A tabela a seguir fornece uma lista de códigos de erro específicos para a PDH. Esses valores são definidos no `pdhmsg.h` arquivo de cabeçalho.

| Código do erro                                                   | Descrição
|--------------------------------------------------------------|------------
| 0x00000000 ( \_ dados válidos do PDH CSTATUS \_ \_ )                       | Os dados retornados são válidos.
| 0x00000001 (PDH \_ CSTATUS \_ novos \_ dados)                         | O valor de dados de retorno é válido e diferente do último exemplo.
| 0x800007D0 (PDH \_ CSTATUS \_ no \_ computador)                       | Não é possível conectar ao computador especificado ou o computador está offline.
| 0x800007D1 (PDH \_ CSTATUS \_ sem \_ instância)                      | A instância especificada não está presente.
| 0x800007D2 (PDH \_ mais \_ dados)                                 | Há mais dados a serem retornados do que se ajustaria no buffer fornecido. Aloque um buffer maior e chame a função novamente.
| 0x800007D3 (PDH \_ CSTATUS \_ item \_ não \_ validado)              | O item de dados foi adicionado à consulta, mas não foi validado nem acessado. Nenhuma outra informação de status sobre este item de dados está disponível.
| 0x800007D4 ( \_ nova tentativa de PDH)                                      | A operação selecionada deve ser repetida.
| 0x800007D5 (PDH \_ sem \_ dados)                                   | Nenhum dado a ser retornado.
| 0x800007D6 ( \_ denominador de cálculo negativo do PDH \_ \_ )                | Foi detectado um contador com um valor de denominador negativo.
| 0x800007D7 ( \_ base de \_ dados negativo de cálculo de PDH \_ )                   | Foi detectado um contador com um valor de base de tempo negativo.
| 0x800007D8 ( \_ valor negativo de cálculo de PDH \_ \_ )                      | Foi detectado um contador com um valor negativo.
| 0x800007D9 ( \_ caixa de diálogo PDH \_ cancelada)                          | O usuário cancelou a caixa de diálogo.
| 0x800007DA ( \_ fim \_ do arquivo de log da PDH \_ \_ )                         | O fim do arquivo de log foi atingido.
| 0x800007DB ( \_ tempo limite de consulta assíncrona de PDH \_ \_ )                      | Tempo limite excedido ao aguardar a finalização do thread de coleção do contador assíncrono.
| 0x800007DC (PDH \_ não pode \_ definir \_ DataSource em \_ tempo real padrão \_ ) | Não é possível alterar a fonte de dados padrão Set Default. Há sessões de consulta em tempo real coletando dados do contador.
| 0xC0000BB8 (PDH \_ CSTATUS \_ sem \_ objeto)                        | O objeto especificado não foi encontrado no sistema.
| 0xC0000BB9 (PDH \_ CSTATUS \_ sem \_ contador)                       | O contador especificado não pôde ser encontrado.
| 0xC0000BBA (PDH \_ CSTATUS \_ dados inválidos \_ )                     | Os dados retornados não são válidos.
| 0xC0000BBB (falha de alocação de memória de PDH \_ \_ \_ )                | Uma função PDH não pôde alocar memória temporária suficiente para concluir a operação. Feche alguns aplicativos ou estenda o arquivo de paginação e repita a função.
| 0xC0000BBC ( \_ identificador inválido de PDH \_ )                            | O identificador não é um objeto PDH válido.
| 0xC0000BBD (argumento de PDH \_ inválido \_ )                          | Um argumento necessário está ausente ou incorreto.
| 0xC0000BBE ( \_ função PDH \_ não \_ encontrada)                       | Não é possível localizar a função especificada.
| 0xC0000BBF (PDH \_ CSTATUS \_ sem \_ COUNTERNAME)                   | Nenhum contador foi especificado.
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
| 0xC0000BCA ( \_ erro de abertura de arquivo de log PDH \_ \_ \_ )                     | Não é possível abrir o arquivo de log especificado.
| 0xC0000BCB ( \_ tipo de log PDH \_ \_ não \_ encontrado)                      | O tipo de arquivo de log especificado não foi instalado neste sistema.
| 0xC0000BCC (PDH \_ não \_ mais \_ dados)                             | Não existem mais dados disponíveis.
| 0xC0000BCD (a \_ entrada PDH \_ não está \_ no \_ arquivo de log \_ )                  | O registro especificado não foi encontrado no arquivo de log.
| 0xC0000BCE (a \_ fonte de dados PDH \_ é um arquivo de \_ \_ log \_ )                | A fonte de dados especificada é um arquivo de log.
| 0xC0000BCF (a \_ fonte de dados PDH \_ é em \_ \_ \_ tempo real)               | A fonte de dados especificada é a atividade atual.
| 0xC0000BD0 (PDH \_ não pôde \_ ler o \_ cabeçalho do log \_ )                  | Não foi possível ler o cabeçalho do arquivo de log.
| 0xC0000BD1 ( \_ arquivo PDH \_ não \_ encontrado)                           | Não é possível localizar o arquivo especificado.
| 0xC0000BD2 (o \_ arquivo PDH \_ já \_ existe)                      | Já existe um arquivo com o nome de arquivo especificado.
| 0xC0000BD3 (PDH \_ não \_ implementado)                           | A função referenciada não foi implementada.
| 0xC0000BD4 (cadeia de PDH \_ \_ não \_ encontrada)                         | Não é possível localizar a cadeia de caracteres especificada na lista de cadeias de texto de nome de desempenho e de ajuda.
| 0x80000BD5 (PDH \_ não pode \_ Mapear \_ arquivos de nome \_ )                   | Não é possível mapear os arquivos de dados do nome do contador de desempenho. Os dados serão lidos do registro e armazenados localmente.
| 0xC0000BD6 ( \_ formato de log desconhecido de PDH \_ \_ )                       | O formato do arquivo de log especificado não é reconhecido pela DLL PDH.
| 0xC0000BD7 ( \_ \_ comando LOGSVC PDH desconhecido \_ )                   | O valor do comando de serviço de log especificado não é reconhecido.
| 0xC0000BD8 ( \_ consulta PDH \_ LOGSVC \_ não \_ encontrada)                  | A consulta especificada do serviço de log não pôde ser encontrada ou não pôde ser aberta.
| 0xC0000BD9 (PDH \_ LOGSVC \_ não \_ aberto)                        | Não foi possível abrir a chave de serviço de log de dados de desempenho. Isso pode ser devido a privilégios insuficientes ou porque o serviço não foi instalado.
| 0xC0000BDA (erro do PDH \_ WBEM \_ )                                | Ocorreu um erro ao acessar o armazenamento de dados WBEM.
| 0xC0000BDB (PDH \_ acesso \_ negado)                             | Não é possível acessar o computador ou o serviço desejado. Verifique as permissões e a autenticação do serviço de log ou a sessão de usuário interativa nos computadores ou no serviço que está sendo monitorado.
| 0xC0000BDC (arquivo de log de PDH \_ \_ \_ muito \_ pequeno)                      | O tamanho máximo do arquivo de log especificado é muito pequeno para registrar os contadores selecionados. Nenhum dado será gravado nesse arquivo de log. Especifique um conjunto menor de contadores para o log ou um tamanho de arquivo maior e repita a chamada.
| 0xC0000BDD (fonte de origem de PDH \_ inválido \_ )                        | Não é possível conectar-se ao nome da fonte de fontes ODBC.
| 0xC0000BDE (PDH \_ inválido \_ SQLDB)                             | O banco de dados SQL não contém um conjunto válido de tabelas para Perfmon.
| 0xC0000BDF (PDH \_ sem \_ contadores)                               | Nenhum contador foi encontrado para este conjunto de logs de SQL Perfmon.
| 0xC0000BE0 ( \_ \_ falha na alocação de SQL PDH \_ )                         | Falha na chamada para SQLAllocStmt com %1.
| 0xC0000BE1 (PDH \_ SQL \_ ALLOCCON \_ falhou)                      | Falha na chamada para SQLAllocConnect com %1.
| 0xC0000BE2 ( \_ falha direta do PDH SQL \_ exec \_ \_ )                  | Falha na chamada a SQLExecDirect com %1.
| 0xC0000BE3 ( \_ \_ falha na busca de SQL de PDH \_ )                         | Falha na chamada a SQLFetch com %1.
| 0xC0000BE4 ( \_ \_ falha na contagem de linhas de PDH SQL \_ )                      | Falha na chamada a SQLRowCount com %1.
| 0xC0000BE5 ( \_ \_ \_ falha na maioria dos resultados do SQL PDH \_ )                 | Falha na chamada para SQLMoreResults com %1.
| 0xC0000BE6 ( \_ \_ falha no SQL Connect do PDH \_ )                       | Falha na chamada para SQLConnect com %1.
| 0xC0000BE7 ( \_ \_ falha na associação do SQL PDH \_ )                          | Falha na chamada para SQLBindCol com %1.
| 0xC0000BE8 (PDH \_ não pode \_ conectar o \_ \_ servidor WMI)               | Não é possível conectar ao servidor WMI no computador solicitado.
| 0xC0000BE9 (a \_ coleção do PDH PLA \_ \_ já \_ está em execução)          | Coleção "%1! s!" Já está em execução.
| 0xC0000BEA ( \_ sobreposição de agendamento de erro de PLA da PDH \_ \_ \_ )              | A hora de início especificada é posterior à hora de término.
| 0xC0000BEB (coleção de PLA da PDH \_ \_ \_ não \_ encontrada)                | Coleção "%1! s!" não existe.
| 0xC0000BEC (agenda de erro de Pla de PDH \_ \_ \_ \_ decorrido)              | A hora de término especificada já expirou.
| 0xC0000BED (erro de PLA da PDH \_ \_ \_ nostart)                        | Coleção "%1! s!" não iniciado; Verifique se há erros no log de eventos do aplicativo.
| 0xC0000BEE (o \_ erro de Pla de PDH \_ \_ já \_ existe)                | Coleção "%1! s!" já existe.
| 0xC0000BEF (tipo de erro do PDH \_ PLA \_ \_ \_ incompatível)                 | Há uma incompatibilidade no tipo de configurações.
| 0xC0000BF0 (PDH de erro de PLA do daprópriat \_ \_ \_ )                       | As informações especificadas não são resolvidas para um nome de caminho válido.
| 0xC0000BF1 (erro de serviço de PLA da PDH \_ \_ \_ )                        | O serviço "logs de desempenho & alertas" não respondeu.
| 0xC0000BF2 (erro de validação de PLA da PDH \_ \_ \_ )                     | As informações transmitidas não são válidas.
| 0x80000BF3 (aviso de validação de PLA da PDH \_ \_ \_ )                   | As informações transmitidas não são válidas.
| 0xC0000BF4 (nome de erro de Pla de PDH \_ \_ \_ \_ muito \_ longo)                | O nome fornecido é muito longo.
| 0xC0000BF5 ( \_ formato de \_ log SQL inválido do PDH \_ \_ )                  | O formato do log SQL está incorreto. O formato correto é `SQL:<DSN-name>!<LogSet-Name>` .
| 0xC0000BF6 ( \_ contador PDH \_ já \_ na \_ consulta)                | O contador de desempenho na chamada [**PdhAddCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera) já foi adicionado na consulta de desempenho. Este contador é ignorado.
| 0xC0000BF7 ( \_ log binário \_ PDH \_ corrompido)                       | Não é possível ler informações do contador e dados de arquivos de log binários de entrada.
| 0xC0000BF8 (exemplo de log de PDH \_ \_ \_ muito \_ pequeno)                    | Pelo menos um dos arquivos de log binários de entrada contém menos de dois exemplos de dados.
| 0xC0000BF9 ( \_ so PDH \_ \_ versão posterior)                         | A versão do sistema operacional no computador chamado %1 é posterior à do computador local. Esta operação não está disponível no computador local.
| 0xC0000BFA ( \_ versão anterior do sistema operacional PDH \_ \_ )                       | %1 dá suporte a %2 ou posterior. Verifique a versão do sistema operacional no computador chamado %3.
| 0xC0000BFB ( \_ tempo de acréscimo incorreto do PDH \_ \_ )                    | O arquivo de saída deve conter dados anteriores do que o arquivo a ser anexado.
| 0xC0000BFC ( \_ contador de acréscimo sem correspondência de PDH \_ \_ )                 | Os dois arquivos devem ter contadores idênticos para acrescentar.
| 0xC0000BFD ( \_ \_ falha no ALTER SQL de PDH \_ \_ )                 | Não é possível alterar o layout da tabela de detalhes no banco de dados SQL.
| 0xC0000BFE ( \_ \_ tempo limite de dados perf da consulta PDH \_ \_ )                 | O sistema está ocupado. Tempo limite excedido ao coletar dados do contador. Tente novamente mais tarde ou aumente o valor do registro **collecttime** .
