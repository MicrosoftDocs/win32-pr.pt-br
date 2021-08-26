---
description: A função SetJob pausa, retoma, cancela ou reinicia um trabalho de impressão em uma impressora especificada. Você também pode usar a função SetJob para definir parâmetros de trabalho de impressão, como a prioridade do trabalho de impressão e o nome do documento.
ms.assetid: 21947c69-c517-4962-8eb7-b45ed4211d9a
title: Função SetJob (WinSpool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetJob
- SetJobA
- SetJobW
api_type:
- DllExport
api_location:
- WinSpool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 9259429a7696e832bbbe6d0dd4bbb6fb46e7bce2bf7157122c10ca47656af346
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060016"
---
# <a name="setjob-function"></a>Função SetJob

A função **SetJob** pausa, retoma, cancela ou reinicia um trabalho de impressão em uma impressora especificada. Você também pode usar a função **SetJob** para definir parâmetros de trabalho de impressão, como a prioridade do trabalho de impressão e o nome do documento.

Você pode usar a função **SetJob** para fornecer um comando para um trabalho de impressão ou para definir os parâmetros do trabalho de impressão ou para fazer ambos na mesma chamada. O valor do parâmetro *Command* não afeta como a função usa os parâmetros *Level* e *pJob* . Além disso, você pode usar **SetJob** com [**informações de trabalho \_ \_ 3**](job-info-3.md) para vincular um conjunto de trabalhos de impressão. Consulte comentários para obter mais informações.

## <a name="syntax"></a>Sintaxe


```C++
BOOL SetJob(
  _In_ HANDLE hPrinter,
  _In_ DWORD  JobId,
  _In_ DWORD  Level,
  _In_ LPBYTE pJob,
  _In_ DWORD  Command
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hPrinter* \[ no\]
</dt> <dd>

Um identificador para o objeto de impressora de interesse. Use a função [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md)ou [**AddPrinter**](addprinter.md) para recuperar um identificador de impressora.

</dd> <dt>

*JobID* \[ no\]
</dt> <dd>

Identificador que especifica o trabalho de impressão. Você Obtém um identificador de trabalho de impressão chamando a função [**AddJob**](addjob.md) ou a função [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) .

Se o parâmetro *Level* for definido como 3, o parâmetro *JobID* deverá corresponder ao membro **JobID** da estrutura [**info do trabalho \_ \_ 3**](job-info-3.md) apontada por *pJob*

</dd> <dt>

*Nível* \[ do no\]
</dt> <dd>

O tipo de estrutura de informações do trabalho apontado pelo parâmetro *pJob* .

**todas as versões do Windows**: você pode definir o parâmetro *Level* como 0, 1 ou 2. Quando você define *nível* como 0, *PJob* deve ser **nulo**. Use esses valores quando você não estiver definindo nenhum parâmetro de trabalho de impressão.

Você também pode definir o parâmetro *Level* como 3.

a partir do **Windows Vista**: você também pode definir o parâmetro *Level* como 4.

</dd> <dt>

*pJob* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura que define os parâmetros do trabalho de impressão.

**todas as versões do Windows**: *pJob* podem apontar para uma estrutura de [**informações de trabalho \_ \_ 1**](job-info-1.md) ou de [**\_ informações \_ 2**](job-info-2.md) .

*pJob* também pode apontar para uma estrutura de [**informações de trabalho \_ \_ 3**](job-info-3.md) . Você deve ter **acesso ao trabalho \_ \_ administrar** permissão de acesso para os trabalhos especificados pelos membros **JobID** e **NextJobId** da **estrutura \_ informações \_ do trabalho 3** .

a partir do **Windows Vista**: *pJob* também pode apontar para uma estrutura de [**informações do trabalho \_ \_ 4**](job-info-4.md) .

Se o parâmetro *Level* for 0, *PJob* deverá ser **NULL**.

</dd> <dt>

*Comando* \[ no\]
</dt> <dd>

A operação de trabalho de impressão a ser executada. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                                                            | Significado                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="JOB_CONTROL_CANCEL"></span><span id="job_control_cancel"></span><dl> <dt>**cancelamento do controle de trabalho \_ \_**</dt> </dl>                                    | Não use. Para excluir um trabalho de impressão, use a **\_ \_ exclusão de controle de trabalho**.<br/>        |
| <span id="JOB_CONTROL_PAUSE"></span><span id="job_control_pause"></span><dl> <dt>**\_pausa de controle de trabalho \_**</dt> </dl>                                       | Pausar o trabalho de impressão.<br/>                                                    |
| <span id="JOB_CONTROL_RESTART"></span><span id="job_control_restart"></span><dl> <dt>**reinicialização do controle de trabalho \_ \_**</dt> </dl>                                 | Reinicie o trabalho de impressão. Um trabalho só poderá ser reiniciado se tiver sido impresso.<br/>  |
| <span id="JOB_CONTROL_RESUME"></span><span id="job_control_resume"></span><dl> <dt>**retomada do controle de trabalho \_ \_**</dt> </dl>                                    | Retomar um trabalho de impressão em pausa.<br/>                                              |
| <span id="JOB_CONTROL_DELETE"></span><span id="job_control_delete"></span><dl> <dt>**\_exclusão de controle de trabalho \_**</dt> </dl>                                    | Exclua o trabalho de impressão.<br/>                                                   |
| <span id="JOB_CONTROL_SENT_TO_PRINTER"></span><span id="job_control_sent_to_printer"></span><dl> <dt>**\_controle \_ de trabalho enviado \_ para a \_ impressora**</dt> </dl>       | Usado por monitores de porta para finalizar o trabalho de impressão.<br/>                             |
| <span id="JOB_CONTROL_LAST_PAGE_EJECTED"></span><span id="job_control_last_page_ejected"></span><dl> <dt>**\_última página de controle de trabalho \_ \_ \_ ejetada**</dt> </dl> | Usado por monitores de idioma para finalizar o trabalho de impressão.<br/>                         |
| <span id="JOB_CONTROL_RETAIN"></span><span id="job_control_retain"></span><dl> <dt>**\_retenção de controle de trabalho \_**</dt> </dl>                                    | **Windows Vista e posterior**: manter o trabalho na fila depois que ele for impresso.<br/> |
| <span id="JOB_CONTROL_RELEASE"></span><span id="job_control_release"></span><dl> <dt>**\_versão de controle de trabalho \_**</dt> </dl>                                 | **Windows Vista e posterior**: libere o trabalho de impressão.<br/>                     |



 

Você pode usar a mesma chamada para a função **SetJob** para definir parâmetros de trabalho de impressão e para dar um comando a um trabalho de impressão. Portanto, o *comando* não precisa ser 0 se você estiver definindo parâmetros de trabalho de impressão, embora possa ser.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.

Se a função falhar, o valor retornado será zero.

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

Você pode usar a função **SetJob** para definir vários parâmetros de trabalho de impressão fornecendo um ponteiro para uma estrutura [**informações de trabalho \_ \_ 1**](job-info-1.md), [**informações do trabalho \_ \_ 2**](job-info-2.md), [**informações do trabalho \_ \_ 3**](job-info-3.md)ou informações do trabalho [**\_ \_ 4**](job-info-4.md) que contém os dados necessários.

Para remover ou excluir todos os trabalhos de impressão de uma impressora específica, chame a função [**Setprintr**](setprinter.md) com seu parâmetro de *comando* definido **como \_ \_ limpeza de controle da impressora**.

Os seguintes membros de uma [**estrutura \_ informações \_ de trabalho 1**](job-info-1.md), [**\_ informações sobre o trabalho \_ 2**](job-info-2.md)ou [**informações do trabalho \_ \_ 4**](job-info-4.md) são ignorados em uma chamada para **SetJob**: **JobID**, **pPrinterName**, **pMachineName**, **pUserName**, **pDrivername**, **tamanho**, **enviado**, **hora** e **TotalPages**.

Você deve ter **\_ acesso à impressora \_ administrar** permissão de acesso para uma impressora a fim de alterar a posição de um trabalho de impressão na fila de impressão.

Se você não quiser definir a posição de um trabalho de impressão na fila de impressão, defina o membro **posição** da estrutura informações do [**trabalho \_ \_ 1**](job-info-1.md), [**informações do \_ trabalho \_ 2**](job-info-2.md)ou [**informações do \_ trabalho \_ 4**](job-info-4.md) para a **posição do trabalho \_ \_ não especificado**.

Use a função **SetJob** com a estrutura [**informações do trabalho \_ \_ 3**](job-info-3.md) para vincular um conjunto de trabalhos de impressão (também conhecido como cadeia). Isso é útil em situações em que um único documento consiste em várias partes que você deseja renderizar separadamente. Para imprimir trabalhos A, B, C e D em ordem, chame **SetJob** com as [**informações do trabalho \_ \_ 4**](job-info-4.md) para vincular a a B, B a c e c a D.

Se você vincular trabalhos de impressão, observe o seguinte:

-   Os trabalhos podem ser adicionados ao início ou ao fim de uma cadeia.
-   Todos os trabalhos na cadeia devem ter o mesmo tipo de dados.
-   A cadeia deve estar completamente vinculada antes do início do spool, caso contrário, o spooler pode imprimir e excluir trabalhos em spool antes de vincular todos eles. Há duas maneiras de manter a cadeia de impressão prematuramente:

    -   Pause o primeiro trabalho na cadeia até que a cadeia seja completamente vinculada. O estado de pausa do primeiro trabalho governa o estado de todos os trabalhos na cadeia.
    -   Mantenha o primeiro trabalho incompleto, ou seja, não chame [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) ou [**ScheduleJob**](schedulejob.md) para o primeiro trabalho. No entanto, se ' Imprimir durante o spool ' estiver habilitado (o padrão), esse método bloqueará a porta enquanto a cadeia for criada, o que também impedirá a impressão de trabalhos não relacionados.

-   O aplicativo deve lidar com o caso em que o usuário exclui um trabalho na cadeia antes de a cadeia terminar de ser impressa. [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retorna **um \_ parâmetro inválido** quando um JobID não existe.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>WinSpool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WinSpool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>WinSpool. drv</dt> </dl>                   |
| Nomes Unicode e ANSI<br/>   | **SetJobW** (Unicode) e **SetJobA** (ANSI)<br/>                                                   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Addjob**](addjob.md)
</dt> <dt>

[**Getjob**](getjob.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**INFORMAÇÕES \_ DO TRABALHO \_ 1**](job-info-1.md)
</dt> <dt>

[**INFORMAÇÕES \_ DO TRABALHO \_ 2**](job-info-2.md)
</dt> <dt>

[**INFORMAÇÕES \_ DO \_ TRABALHO 3**](job-info-3.md)
</dt> <dt>

[**INFORMAÇÕES \_ DO TRABALHO \_ 4**](job-info-4.md)
</dt> </dl>

 

