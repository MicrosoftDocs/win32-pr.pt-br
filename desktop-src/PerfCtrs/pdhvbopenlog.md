---
description: A função PdhVbOpenLog abre o arquivo de log especificado para leitura e gravação. Essa função chama PdhOpenLog.
ms.assetid: d9b8d98c-64f2-4319-8ab2-67b776143cf7
title: Função PdhVbOpenLog
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbOpenLog
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 7921585039cab285589f2cdde0f328c033069a87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505881"
---
# <a name="pdhvbopenlog-function"></a>Função PdhVbOpenLog

A função **PdhVbOpenLog** abre o arquivo de log especificado para leitura e gravação. Essa função chama [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga).

> [!IMPORTANT]
> A função que este tópico descreve pode ser alterada ou indisponível no futuro. Em vez disso, a Microsoft recomenda que você use as funções descritas em [funções de contadores de desempenho](performance-counters-functions.md).

A função PdhVbOpenLog ( \_ ByVal SzLogFileName as LPCTSTR, \_ ByVal DWACCESSFLAGS as DWORD, \_ ByVal lpdwLogType as LPDWORD, \_ ByVal hQuery as PDH \_ HQUERY, \_ ByVal DwMaxSize as DWORD, \_ ByVal SZUSERCAPTION as LPCSTR, \_ ByRef phLog as PDH \_ HLOG \_ ) como DWORD

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*szLogFileName* \[ no\]
</dt> <dd>

Ponteiro para uma cadeia de caracteres que especifica o nome do arquivo de log a ser aberto.

Se o arquivo de log contiver dados SQL, o formato do nome do arquivo de log será **SQL:**_DataSourceName_*_!_* _LogFileName_. Nesse caso, o valor do parâmetro *lpdwLogType* é o tipo de \_ log \_ PDH \_ SQL.

</dd> <dt>

*dwAccessFlags* \[ no\]
</dt> <dd>

Tipo de acesso a ser especificado quando o arquivo de log é aberto. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                                   | Significado                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="PDH_LOG_READ_ACCESS"></span><span id="pdh_log_read_access"></span><dl> <dt>**\_acesso de \_ leitura do log de PDH \_**</dt> </dl>       | Um arquivo de log é aberto para uma operação de leitura.<br/>            |
| <span id="PDH_LOG_WRITE_ACCESS"></span><span id="pdh_log_write_access"></span><dl> <dt>**\_acesso de \_ gravação de log de PDH \_**</dt> </dl>    | Um novo arquivo de log é aberto para uma operação de gravação.<br/>       |
| <span id="PDH_LOG_UPDATE_ACCESS"></span><span id="pdh_log_update_access"></span><dl> <dt>**\_acesso de \_ atualização de log PDH \_**</dt> </dl> | Um arquivo de log existente é aberto para uma operação de gravação.<br/> |



 

O valor selecionado na tabela anterior pode ser combinado usando o operador OR com um dos seguintes sinalizadores de acesso de criação.



| Valor                                                                                                                                                                                   | Significado                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PDH_LOG_CREATE_NEW"></span><span id="pdh_log_create_new"></span><dl> <dt>**\_ \_ criar novo log \_ de PDH**</dt> </dl>          | Um novo arquivo de log com o nome especificado é criado.<br/>                                                                                                    |
| <span id="PDH_LOG_CREATE_ALWAYS"></span><span id="pdh_log_create_always"></span><dl> <dt>**\_ \_ criar sempre log \_ de PDH**</dt> </dl> | Um novo arquivo de log com o nome especificado é criado e qualquer arquivo de log existente com o mesmo nome é apagado.<br/>                                             |
| <span id="PDH_LOG_OPEN_EXISTING"></span><span id="pdh_log_open_existing"></span><dl> <dt>**LOG de PDH \_ \_ aberto \_ existente**</dt> </dl> | Um arquivo de log existente com o nome especificado é aberto. Se um arquivo de log com o nome especificado não existir, isso será igual ao log de PDH \_ \_ criar \_ novo.<br/> |
| <span id="PDH_LOG_OPEN_ALWAYS"></span><span id="pdh_log_open_always"></span><dl> <dt>**\_ \_ abrir sempre o log de PDH \_**</dt> </dl>       | Um arquivo de log existente com o nome especificado é aberto ou um novo arquivo de log com o nome especificado é criado.<br/>                                          |



 

</dd> <dt>

*lpdwLogType* \[ no\]
</dt> <dd>

Ponteiro para uma variável que indica o tipo de arquivo de log a ser aberto. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                                      | Significado                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span id="PDH_LOG_TYPE_UNDEFINED"></span><span id="pdh_log_type_undefined"></span><dl> <dt>**\_tipo de log PDH \_ \_ indefinido**</dt> </dl> | Formato de arquivo de log indefinido.<br/>                                                                                   |
| <span id="PDH_LOG_TYPE_CSV"></span><span id="pdh_log_type_csv"></span><dl> <dt>**tipo de log de PDH \_ \_ \_ CSV**</dt> </dl>                   | Arquivos de texto que contêm cabeçalhos de coluna na primeira linha e exemplos de dados individuais em cada linha subsequente.<br/> |
| <span id="PDH_LOG_TYPE_SQL"></span><span id="pdh_log_type_sql"></span><dl> <dt>**tipo de log de PDH \_ \_ \_ SQL**</dt> </dl>                   | Os dados no arquivo de log estão em SQL.<br/>                                                                          |
| <span id="PDH_LOG_TYPE_TSV"></span><span id="pdh_log_type_tsv"></span><dl> <dt>**tipo de log de PDH \_ \_ \_ TSV**</dt> </dl>                   | Mesmo que o \_ tipo de log de PDH \_ \_ CSV.<br/>                                                                                 |
| <span id="PDH_LOG_TYPE_BINARY"></span><span id="pdh_log_type_binary"></span><dl> <dt>**\_binário de \_ tipo de log PDH \_**</dt> </dl>          | Formato do arquivo de log binário. Inclui arquivos de log circulares.<br/>                                                         |
| <span id="PDH_LOG_TYPE_PERFMON"></span><span id="pdh_log_type_perfmon"></span><dl> <dt>**\_tipo de log PDH \_ \_ Perfmon**</dt> </dl>       | Formato do arquivo de log Perfmon.<br/>                                                                                     |



 

</dd> <dt>

*hQuery* \[ no\]
</dt> <dd>

Identificador de consulta. Esse identificador é retornado pela função [**PdhVbOpenQuery**](pdhvbopenquery.md) .

Esse parâmetro poderá ser **nulo** se o arquivo de log for aberto para leitura.

</dd> <dt>

*dwMaxSize* \[ no\]
</dt> <dd>

Tamanho máximo do arquivo de log, em bytes. Esse valor será usado somente se o arquivo de log for um arquivo de log circular ou de tamanho limitado.

</dd> <dt>

*szUserCaption* \[ no\]
</dt> <dd>

Ponteiro para uma cadeia de caracteres que especifica a legenda definida pelo usuário do arquivo de log. Uma legenda do arquivo de log geralmente descreve o conteúdo do arquivo de log. Quando um arquivo de log existente é aberto, o valor desse parâmetro é ignorado.

</dd> <dt>

*phLog* \[ em, ref\]
</dt> <dd>

Ponteiro para um buffer que recebe um identificador para o arquivo de log aberto.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, ela retornará 0.

Se a função falhar, o valor de retorno será um [código de erro do sistema](/windows/desktop/Debug/system-error-codes) ou um código de [erro PDH](pdh-error-codes.md). Os valores a seguir são possíveis.



| Código de retorno                                                                                                | Descrição                                                                                            |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_buffer insuficiente de PDH \_**</dt> </dl>   | Os dados solicitados são maiores que o buffer fornecido. Não é possível retornar os dados solicitados.<br/> |
| <dl> <dt>**\_argumento inválido de PDH \_**</dt> </dl>      | Um ou mais dos buffers de cadeia de caracteres não tem o tamanho correto.<br/>                                  |
| <dl> <dt>**\_identificador inválido de PDH \_**</dt> </dl>        | O identificador não é um objeto PDH válido.<br/>                                                       |
| <dl> <dt>**\_ \_ \_ erro ao abrir arquivo de log PDH \_**</dt> </dl> | Não é possível abrir o arquivo de log especificado.<br/>                                                      |
| <dl> <dt>**\_arquivo PDH \_ não \_ encontrado**</dt> </dl>       | Não é possível localizar o arquivo especificado.<br/>                                                          |



 

## <a name="remarks"></a>Comentários

Ao usar essa função para gravar dados de desempenho em um arquivo de log, uma consulta deve ser aberta primeiro usando [**PdhVbOpenQuery**](pdhvbopenquery.md).

Deve haver uma consulta aberta no momento e os contadores desejados devem ser adicionados a ela, antes que essa função seja chamada.

Observe que os arquivos de log no formato Perfmon só podem ser abertos para leitura.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                               |
| Biblioteca<br/>                  | <dl> <dt>PDH. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga)
</dt> <dt>

[**PdhVbGetLogFileSize**](pdhvbgetlogfilesize.md)
</dt> <dt>

[**PdhVbUpdateLog**](pdhvbupdatelog.md)
</dt> </dl>

 

