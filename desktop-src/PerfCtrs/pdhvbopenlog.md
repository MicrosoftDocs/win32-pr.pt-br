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
# <a name="pdhvbopenlog-function"></a><span data-ttu-id="6ad34-104">Função PdhVbOpenLog</span><span class="sxs-lookup"><span data-stu-id="6ad34-104">PdhVbOpenLog function</span></span>

<span data-ttu-id="6ad34-105">A função **PdhVbOpenLog** abre o arquivo de log especificado para leitura e gravação.</span><span class="sxs-lookup"><span data-stu-id="6ad34-105">The **PdhVbOpenLog** function opens the specified log file for reading and writing.</span></span> <span data-ttu-id="6ad34-106">Essa função chama [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga).</span><span class="sxs-lookup"><span data-stu-id="6ad34-106">This function calls [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6ad34-107">A função que este tópico descreve pode ser alterada ou indisponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="6ad34-107">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="6ad34-108">Em vez disso, a Microsoft recomenda que você use as funções descritas em [funções de contadores de desempenho](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="6ad34-108">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="6ad34-109">A função PdhVbOpenLog ( \_ ByVal SzLogFileName as LPCTSTR, \_ ByVal DWACCESSFLAGS as DWORD, \_ ByVal lpdwLogType as LPDWORD, \_ ByVal hQuery as PDH \_ HQUERY, \_ ByVal DwMaxSize as DWORD, \_ ByVal SZUSERCAPTION as LPCSTR, \_ ByRef phLog as PDH \_ HLOG \_ ) como DWORD</span><span class="sxs-lookup"><span data-stu-id="6ad34-109">Function PdhVbOpenLog( \_ ByVal szLogFileName As LPCTSTR, \_ ByVal dwAccessFlags As DWORD, \_ ByVal lpdwLogType As LPDWORD, \_ ByVal hQuery As PDH\_HQUERY, \_ ByVal dwMaxSize As DWORD, \_ ByVal szUserCaption As LPCSTR, \_ ByRef phLog As PDH\_HLOG \_ ) As DWORD</span></span>

## <a name="parameters"></a><span data-ttu-id="6ad34-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6ad34-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ad34-111">*szLogFileName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6ad34-111">*szLogFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ad34-112">Ponteiro para uma cadeia de caracteres que especifica o nome do arquivo de log a ser aberto.</span><span class="sxs-lookup"><span data-stu-id="6ad34-112">Pointer to a string that specifies the name of the log file to be opened.</span></span>

<span data-ttu-id="6ad34-113">Se o arquivo de log contiver dados SQL, o formato do nome do arquivo de log será **SQL:**_DataSourceName_*_!_* _LogFileName_.</span><span class="sxs-lookup"><span data-stu-id="6ad34-113">If the log file contains SQL data, the format of the name of the log file is **SQL:**_DataSourceName_*_!_*_LogFileName_.</span></span> <span data-ttu-id="6ad34-114">Nesse caso, o valor do parâmetro *lpdwLogType* é o tipo de \_ log \_ PDH \_ SQL.</span><span class="sxs-lookup"><span data-stu-id="6ad34-114">In this case, the value of the *lpdwLogType* parameter is PDH\_LOG\_TYPE\_SQL.</span></span>

</dd> <dt>

<span data-ttu-id="6ad34-115">*dwAccessFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6ad34-115">*dwAccessFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ad34-116">Tipo de acesso a ser especificado quando o arquivo de log é aberto.</span><span class="sxs-lookup"><span data-stu-id="6ad34-116">Type of access to be specified when the log file is opened.</span></span> <span data-ttu-id="6ad34-117">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="6ad34-117">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="6ad34-118">Valor</span><span class="sxs-lookup"><span data-stu-id="6ad34-118">Value</span></span>                                                                                                                                                                                   | <span data-ttu-id="6ad34-119">Significado</span><span class="sxs-lookup"><span data-stu-id="6ad34-119">Meaning</span></span>                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="PDH_LOG_READ_ACCESS"></span><span id="pdh_log_read_access"></span><dl> <span data-ttu-id="6ad34-120"><dt>**\_acesso de \_ leitura do log de PDH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6ad34-120"><dt>**PDH\_LOG\_READ\_ACCESS**</dt></span></span> </dl>       | <span data-ttu-id="6ad34-121">Um arquivo de log é aberto para uma operação de leitura.</span><span class="sxs-lookup"><span data-stu-id="6ad34-121">A log file is opened for a read operation.</span></span><br/>            |
| <span id="PDH_LOG_WRITE_ACCESS"></span><span id="pdh_log_write_access"></span><dl> <span data-ttu-id="6ad34-122"><dt>**\_acesso de \_ gravação de log de PDH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6ad34-122"><dt>**PDH\_LOG\_WRITE\_ACCESS**</dt></span></span> </dl>    | <span data-ttu-id="6ad34-123">Um novo arquivo de log é aberto para uma operação de gravação.</span><span class="sxs-lookup"><span data-stu-id="6ad34-123">A new log file is opened for a write operation.</span></span><br/>       |
| <span id="PDH_LOG_UPDATE_ACCESS"></span><span id="pdh_log_update_access"></span><dl> <span data-ttu-id="6ad34-124"><dt>**\_acesso de \_ atualização de log PDH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6ad34-124"><dt>**PDH\_LOG\_UPDATE\_ACCESS**</dt></span></span> </dl> | <span data-ttu-id="6ad34-125">Um arquivo de log existente é aberto para uma operação de gravação.</span><span class="sxs-lookup"><span data-stu-id="6ad34-125">An existing log file is opened for a write operation.</span></span><br/> |



 

<span data-ttu-id="6ad34-126">O valor selecionado na tabela anterior pode ser combinado usando o operador OR com um dos seguintes sinalizadores de acesso de criação.</span><span class="sxs-lookup"><span data-stu-id="6ad34-126">The value selected from the previous table can be combined using the OR operator with one of the following create access flags.</span></span>



| <span data-ttu-id="6ad34-127">Valor</span><span class="sxs-lookup"><span data-stu-id="6ad34-127">Value</span></span>                                                                                                                                                                                   | <span data-ttu-id="6ad34-128">Significado</span><span class="sxs-lookup"><span data-stu-id="6ad34-128">Meaning</span></span>                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PDH_LOG_CREATE_NEW"></span><span id="pdh_log_create_new"></span><dl> <span data-ttu-id="6ad34-129"><dt>**\_ \_ criar novo log \_ de PDH**</dt></span><span class="sxs-lookup"><span data-stu-id="6ad34-129"><dt>**PDH\_LOG\_CREATE\_NEW**</dt></span></span> </dl>          | <span data-ttu-id="6ad34-130">Um novo arquivo de log com o nome especificado é criado.</span><span class="sxs-lookup"><span data-stu-id="6ad34-130">A new log file with the specified name is created.</span></span><br/>                                                                                                    |
| <span id="PDH_LOG_CREATE_ALWAYS"></span><span id="pdh_log_create_always"></span><dl> <span data-ttu-id="6ad34-131"><dt>**\_ \_ criar sempre log \_ de PDH**</dt></span><span class="sxs-lookup"><span data-stu-id="6ad34-131"><dt>**PDH\_LOG\_CREATE\_ALWAYS**</dt></span></span> </dl> | <span data-ttu-id="6ad34-132">Um novo arquivo de log com o nome especificado é criado e qualquer arquivo de log existente com o mesmo nome é apagado.</span><span class="sxs-lookup"><span data-stu-id="6ad34-132">A new log file with the specified name is created and any existing log file with the same name is erased.</span></span><br/>                                             |
| <span id="PDH_LOG_OPEN_EXISTING"></span><span id="pdh_log_open_existing"></span><dl> <span data-ttu-id="6ad34-133"><dt>**LOG de PDH \_ \_ aberto \_ existente**</dt></span><span class="sxs-lookup"><span data-stu-id="6ad34-133"><dt>**PDH\_LOG\_OPEN\_EXISTING**</dt></span></span> </dl> | <span data-ttu-id="6ad34-134">Um arquivo de log existente com o nome especificado é aberto.</span><span class="sxs-lookup"><span data-stu-id="6ad34-134">An existing log file with the specified name is opened.</span></span> <span data-ttu-id="6ad34-135">Se um arquivo de log com o nome especificado não existir, isso será igual ao log de PDH \_ \_ criar \_ novo.</span><span class="sxs-lookup"><span data-stu-id="6ad34-135">If a log file with the specified name does not exist, this is equal to PDH\_LOG\_CREATE\_NEW.</span></span><br/> |
| <span id="PDH_LOG_OPEN_ALWAYS"></span><span id="pdh_log_open_always"></span><dl> <span data-ttu-id="6ad34-136"><dt>**\_ \_ abrir sempre o log de PDH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6ad34-136"><dt>**PDH\_LOG\_OPEN\_ALWAYS**</dt></span></span> </dl>       | <span data-ttu-id="6ad34-137">Um arquivo de log existente com o nome especificado é aberto ou um novo arquivo de log com o nome especificado é criado.</span><span class="sxs-lookup"><span data-stu-id="6ad34-137">An existing log file with the specified name is opened or a new log file with the specified name is created.</span></span><br/>                                          |



 

</dd> <dt>

<span data-ttu-id="6ad34-138">*lpdwLogType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6ad34-138">*lpdwLogType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ad34-139">Ponteiro para uma variável que indica o tipo de arquivo de log a ser aberto.</span><span class="sxs-lookup"><span data-stu-id="6ad34-139">Pointer to a variable that indicates the type of log file to be opened.</span></span> <span data-ttu-id="6ad34-140">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="6ad34-140">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="6ad34-141">Valor</span><span class="sxs-lookup"><span data-stu-id="6ad34-141">Value</span></span>                                                                                                                                                                                      | <span data-ttu-id="6ad34-142">Significado</span><span class="sxs-lookup"><span data-stu-id="6ad34-142">Meaning</span></span>                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span id="PDH_LOG_TYPE_UNDEFINED"></span><span id="pdh_log_type_undefined"></span><dl> <span data-ttu-id="6ad34-143"><dt>**\_tipo de log PDH \_ \_ indefinido**</dt></span><span class="sxs-lookup"><span data-stu-id="6ad34-143"><dt>**PDH\_LOG\_TYPE\_UNDEFINED**</dt></span></span> </dl> | <span data-ttu-id="6ad34-144">Formato de arquivo de log indefinido.</span><span class="sxs-lookup"><span data-stu-id="6ad34-144">Undefined log file format.</span></span><br/>                                                                                   |
| <span id="PDH_LOG_TYPE_CSV"></span><span id="pdh_log_type_csv"></span><dl> <span data-ttu-id="6ad34-145"><dt>**tipo de log de PDH \_ \_ \_ CSV**</dt></span><span class="sxs-lookup"><span data-stu-id="6ad34-145"><dt>**PDH\_LOG\_TYPE\_CSV**</dt></span></span> </dl>                   | <span data-ttu-id="6ad34-146">Arquivos de texto que contêm cabeçalhos de coluna na primeira linha e exemplos de dados individuais em cada linha subsequente.</span><span class="sxs-lookup"><span data-stu-id="6ad34-146">Text files containing column headers in the first line, and individual data samples in each subsequent line.</span></span><br/> |
| <span id="PDH_LOG_TYPE_SQL"></span><span id="pdh_log_type_sql"></span><dl> <span data-ttu-id="6ad34-147"><dt>**tipo de log de PDH \_ \_ \_ SQL**</dt></span><span class="sxs-lookup"><span data-stu-id="6ad34-147"><dt>**PDH\_LOG\_TYPE\_SQL**</dt></span></span> </dl>                   | <span data-ttu-id="6ad34-148">Os dados no arquivo de log estão em SQL.</span><span class="sxs-lookup"><span data-stu-id="6ad34-148">The data in the log file is in SQL.</span></span><br/>                                                                          |
| <span id="PDH_LOG_TYPE_TSV"></span><span id="pdh_log_type_tsv"></span><dl> <span data-ttu-id="6ad34-149"><dt>**tipo de log de PDH \_ \_ \_ TSV**</dt></span><span class="sxs-lookup"><span data-stu-id="6ad34-149"><dt>**PDH\_LOG\_TYPE\_TSV**</dt></span></span> </dl>                   | <span data-ttu-id="6ad34-150">Mesmo que o \_ tipo de log de PDH \_ \_ CSV.</span><span class="sxs-lookup"><span data-stu-id="6ad34-150">Same as PDH\_LOG\_TYPE\_CSV.</span></span><br/>                                                                                 |
| <span id="PDH_LOG_TYPE_BINARY"></span><span id="pdh_log_type_binary"></span><dl> <span data-ttu-id="6ad34-151"><dt>**\_binário de \_ tipo de log PDH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6ad34-151"><dt>**PDH\_LOG\_TYPE\_BINARY**</dt></span></span> </dl>          | <span data-ttu-id="6ad34-152">Formato do arquivo de log binário.</span><span class="sxs-lookup"><span data-stu-id="6ad34-152">Binary log file format.</span></span> <span data-ttu-id="6ad34-153">Inclui arquivos de log circulares.</span><span class="sxs-lookup"><span data-stu-id="6ad34-153">Includes circular log files.</span></span><br/>                                                         |
| <span id="PDH_LOG_TYPE_PERFMON"></span><span id="pdh_log_type_perfmon"></span><dl> <span data-ttu-id="6ad34-154"><dt>**\_tipo de log PDH \_ \_ Perfmon**</dt></span><span class="sxs-lookup"><span data-stu-id="6ad34-154"><dt>**PDH\_LOG\_TYPE\_PERFMON**</dt></span></span> </dl>       | <span data-ttu-id="6ad34-155">Formato do arquivo de log Perfmon.</span><span class="sxs-lookup"><span data-stu-id="6ad34-155">Perfmon log file format.</span></span><br/>                                                                                     |



 

</dd> <dt>

<span data-ttu-id="6ad34-156">*hQuery* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6ad34-156">*hQuery* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ad34-157">Identificador de consulta.</span><span class="sxs-lookup"><span data-stu-id="6ad34-157">Query handle.</span></span> <span data-ttu-id="6ad34-158">Esse identificador é retornado pela função [**PdhVbOpenQuery**](pdhvbopenquery.md) .</span><span class="sxs-lookup"><span data-stu-id="6ad34-158">This handle is returned by the [**PdhVbOpenQuery**](pdhvbopenquery.md) function.</span></span>

<span data-ttu-id="6ad34-159">Esse parâmetro poderá ser **nulo** se o arquivo de log for aberto para leitura.</span><span class="sxs-lookup"><span data-stu-id="6ad34-159">This parameter can be **NULL** if the log file is to be opened for reading.</span></span>

</dd> <dt>

<span data-ttu-id="6ad34-160">*dwMaxSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6ad34-160">*dwMaxSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ad34-161">Tamanho máximo do arquivo de log, em bytes.</span><span class="sxs-lookup"><span data-stu-id="6ad34-161">Maximum size of the log file, in bytes.</span></span> <span data-ttu-id="6ad34-162">Esse valor será usado somente se o arquivo de log for um arquivo de log circular ou de tamanho limitado.</span><span class="sxs-lookup"><span data-stu-id="6ad34-162">This value is used only if the log file is a limited-size or circular log file.</span></span>

</dd> <dt>

<span data-ttu-id="6ad34-163">*szUserCaption* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6ad34-163">*szUserCaption* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ad34-164">Ponteiro para uma cadeia de caracteres que especifica a legenda definida pelo usuário do arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="6ad34-164">Pointer to a string that specifies the user-defined caption of the log file.</span></span> <span data-ttu-id="6ad34-165">Uma legenda do arquivo de log geralmente descreve o conteúdo do arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="6ad34-165">A log file caption generally describes the contents of the log file.</span></span> <span data-ttu-id="6ad34-166">Quando um arquivo de log existente é aberto, o valor desse parâmetro é ignorado.</span><span class="sxs-lookup"><span data-stu-id="6ad34-166">When an existing log file is opened, the value of this parameter is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="6ad34-167">*phLog* \[ em, ref\]</span><span class="sxs-lookup"><span data-stu-id="6ad34-167">*phLog* \[in, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="6ad34-168">Ponteiro para um buffer que recebe um identificador para o arquivo de log aberto.</span><span class="sxs-lookup"><span data-stu-id="6ad34-168">Pointer to a buffer that receives a handle to the opened log file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ad34-169">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6ad34-169">Return value</span></span>

<span data-ttu-id="6ad34-170">Se a função for realizada com sucesso, ela retornará 0.</span><span class="sxs-lookup"><span data-stu-id="6ad34-170">If the function succeeds, it returns 0.</span></span>

<span data-ttu-id="6ad34-171">Se a função falhar, o valor de retorno será um [código de erro do sistema](/windows/desktop/Debug/system-error-codes) ou um código de [erro PDH](pdh-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="6ad34-171">If the function fails, the return value is a [system error code](/windows/desktop/Debug/system-error-codes) or a [PDH error code](pdh-error-codes.md).</span></span> <span data-ttu-id="6ad34-172">Os valores a seguir são possíveis.</span><span class="sxs-lookup"><span data-stu-id="6ad34-172">The following are possible values.</span></span>



| <span data-ttu-id="6ad34-173">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="6ad34-173">Return code</span></span>                                                                                                | <span data-ttu-id="6ad34-174">Descrição</span><span class="sxs-lookup"><span data-stu-id="6ad34-174">Description</span></span>                                                                                            |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6ad34-175"><dt>**\_buffer insuficiente de PDH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6ad34-175"><dt>**PDH\_INSUFFICIENT\_BUFFER**</dt></span></span> </dl>   | <span data-ttu-id="6ad34-176">Os dados solicitados são maiores que o buffer fornecido.</span><span class="sxs-lookup"><span data-stu-id="6ad34-176">The requested data is larger than the buffer supplied.</span></span> <span data-ttu-id="6ad34-177">Não é possível retornar os dados solicitados.</span><span class="sxs-lookup"><span data-stu-id="6ad34-177">Unable to return the requested data.</span></span><br/> |
| <dl> <span data-ttu-id="6ad34-178"><dt>**\_argumento inválido de PDH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6ad34-178"><dt>**PDH\_INVALID\_ARGUMENT**</dt></span></span> </dl>      | <span data-ttu-id="6ad34-179">Um ou mais dos buffers de cadeia de caracteres não tem o tamanho correto.</span><span class="sxs-lookup"><span data-stu-id="6ad34-179">One or more of the string buffers is not the correct size.</span></span><br/>                                  |
| <dl> <span data-ttu-id="6ad34-180"><dt>**\_identificador inválido de PDH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6ad34-180"><dt>**PDH\_INVALID\_HANDLE**</dt></span></span> </dl>        | <span data-ttu-id="6ad34-181">O identificador não é um objeto PDH válido.</span><span class="sxs-lookup"><span data-stu-id="6ad34-181">The handle is not a valid PDH object.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="6ad34-182"><dt>**\_ \_ \_ erro ao abrir arquivo de log PDH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6ad34-182"><dt>**PDH\_LOG\_FILE\_OPEN\_ERROR**</dt></span></span> </dl> | <span data-ttu-id="6ad34-183">Não é possível abrir o arquivo de log especificado.</span><span class="sxs-lookup"><span data-stu-id="6ad34-183">Unable to open the specified log file.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="6ad34-184"><dt>**\_arquivo PDH \_ não \_ encontrado**</dt></span><span class="sxs-lookup"><span data-stu-id="6ad34-184"><dt>**PDH\_FILE\_NOT\_FOUND**</dt></span></span> </dl>       | <span data-ttu-id="6ad34-185">Não é possível localizar o arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="6ad34-185">Unable to find the specified file.</span></span><br/>                                                          |



 

## <a name="remarks"></a><span data-ttu-id="6ad34-186">Comentários</span><span class="sxs-lookup"><span data-stu-id="6ad34-186">Remarks</span></span>

<span data-ttu-id="6ad34-187">Ao usar essa função para gravar dados de desempenho em um arquivo de log, uma consulta deve ser aberta primeiro usando [**PdhVbOpenQuery**](pdhvbopenquery.md).</span><span class="sxs-lookup"><span data-stu-id="6ad34-187">When using this function to write performance data to a log file, a query must first be opened using [**PdhVbOpenQuery**](pdhvbopenquery.md).</span></span>

<span data-ttu-id="6ad34-188">Deve haver uma consulta aberta no momento e os contadores desejados devem ser adicionados a ela, antes que essa função seja chamada.</span><span class="sxs-lookup"><span data-stu-id="6ad34-188">There must be a currently opened query, and the desired counters must be added to it, before this function is called.</span></span>

<span data-ttu-id="6ad34-189">Observe que os arquivos de log no formato Perfmon só podem ser abertos para leitura.</span><span class="sxs-lookup"><span data-stu-id="6ad34-189">Note that log files in the Perfmon format can only be opened for reading.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ad34-190">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ad34-190">Requirements</span></span>



| <span data-ttu-id="6ad34-191">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ad34-191">Requirement</span></span> | <span data-ttu-id="6ad34-192">Valor</span><span class="sxs-lookup"><span data-stu-id="6ad34-192">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6ad34-193">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6ad34-193">Minimum supported client</span></span><br/> | <span data-ttu-id="6ad34-194">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6ad34-194">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6ad34-195">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6ad34-195">Minimum supported server</span></span><br/> | <span data-ttu-id="6ad34-196">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6ad34-196">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6ad34-197">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6ad34-197">Library</span></span><br/>                  | <dl> <span data-ttu-id="6ad34-198"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6ad34-198"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="6ad34-199">DLL</span><span class="sxs-lookup"><span data-stu-id="6ad34-199">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ad34-200"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ad34-200"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ad34-201">Confira também</span><span class="sxs-lookup"><span data-stu-id="6ad34-201">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ad34-202">**PdhOpenLog**</span><span class="sxs-lookup"><span data-stu-id="6ad34-202">**PdhOpenLog**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga)
</dt> <dt>

[<span data-ttu-id="6ad34-203">**PdhVbGetLogFileSize**</span><span class="sxs-lookup"><span data-stu-id="6ad34-203">**PdhVbGetLogFileSize**</span></span>](pdhvbgetlogfilesize.md)
</dt> <dt>

[<span data-ttu-id="6ad34-204">**PdhVbUpdateLog**</span><span class="sxs-lookup"><span data-stu-id="6ad34-204">**PdhVbUpdateLog**</span></span>](pdhvbupdatelog.md)
</dt> </dl>

 

