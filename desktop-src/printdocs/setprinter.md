---
description: A função setprinter define os dados de uma impressora especificada ou define o estado da impressora especificada pausando a impressão, retomando a impressão ou limpando todos os trabalhos de impressão.
ms.assetid: ade367c5-20d6-4da9-bb52-ce6768cf7537
title: Função setprinter (WinSpool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetPrinter
- SetPrinterA
- SetPrinterW
api_type:
- DllExport
api_location:
- WinSpool.drv
- Ext-MS-Win-printer-WinSpool-l1-1-0.dll
- Ext-MS-Win-printer-WinSpool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 5f2c58d97315ff108c8f12bd029849993a307025
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764213"
---
# <a name="setprinter-function"></a>Função setprinter

A função **Setprinter** define os dados de uma impressora especificada ou define o estado da impressora especificada pausando a impressão, retomando a impressão ou limpando todos os trabalhos de impressão.

## <a name="syntax"></a>Sintaxe


```C++
BOOL SetPrinter(
  _In_ HANDLE hPrinter,
  _In_ DWORD  Level,
  _In_ LPBYTE pPrinter,
  _In_ DWORD  Command
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hPrinter* \[ no\]
</dt> <dd>

Um identificador para a impressora. Use a função [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md)ou [**AddPrinter**](addprinter.md) para recuperar um identificador de impressora.

</dd> <dt>

*Nível* \[ do no\]
</dt> <dd>

O tipo de dados que a função armazena no buffer apontado por *pPrinter*. Se o parâmetro de *comando* não for igual a zero, o parâmetro *Level* deverá ser zero.

Esse valor pode ser 0, 2, 3, 4, 5, 6, 7, 8 ou 9.

</dd> <dt>

*pPrinter* \[ no\]
</dt> <dd>

Um ponteiro para um buffer que contém dados a serem definidos para a impressora ou que contêm informações para o comando especificado pelo parâmetro de *comando* . O tipo de dados no buffer é determinado pelo valor do *nível*.



| Nível                                                                                                | Estrutura                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Se o parâmetro de *comando* for **Printer \_ Control \_ set \_ status**, *pPrinter* deverá conter um valor **DWORD** que especifica o novo status da impressora a ser definido. Para obter uma lista dos possíveis valores de status, consulte o membro **status** da [**estrutura \_ info \_ 2 da impressora**](printer-info-2.md) . Observe que o **status da impressora em \_ \_ pausa** e a **\_ exclusão do status da impressora \_ pendente \_** não são valores de status válidos a serem definidos.<br/> Se o *nível* for 0, mas o parâmetro de *comando* não for um status de  **conjunto de controle de impressora \_ \_ \_**, pPrinter deverá ser **nulo**.<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Uma estrutura de [**informações da impressora \_ \_ 2**](printer-info-2.md) que contém informações detalhadas sobre a impressora.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | Uma estrutura de [**informações da impressora \_ \_ 3**](printer-info-3.md) que contém as informações de segurança da impressora.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="4"></span><dl> <dt>**quatro**</dt> </dl> | Uma estrutura de [**informações da impressora \_ \_ 4**](printer-info-4.md) que contém informações de impressora mínimas, incluindo o nome da impressora, o nome do servidor e se a impressora é remota ou local.<br/>                                                                                                                                                                                                                                                                                                                                         |
| <span id="5"></span><dl> <dt>**05**</dt> </dl> | Uma estrutura de [**informações da impressora \_ \_ 5**](printer-info-5.md) que contém informações de impressora, como atributos de impressora e configurações de tempo limite.<br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="6"></span><dl> <dt>**6**</dt> </dl> | Uma estrutura de [**informações da impressora \_ \_ 6**](printer-info-6.md) especificando o valor de status de uma impressora.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="7"></span><dl> <dt>**7**</dt> </dl> | Uma estrutura de [**informações da impressora \_ \_ 7**](printer-info-7.md) . O membro *dwAction* dessa estrutura indica se o **setimprimíer** deve publicar, cancelar a publicação, publicar novamente ou atualizar os dados da impressora no serviço de diretório.<br/>                                                                                                                                                                                                                                                                                                                |
| <span id="8"></span><dl> <dt>**8**</dt> </dl> | Uma estrutura de [**informações da impressora \_ \_ 8**](printer-info-8.md) especificando as configurações de impressora padrão globais.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="9"></span><dl> <dt>**9**</dt> </dl> | Uma estrutura de [**informações da impressora \_ \_ 9**](printer-info-9.md) especificando as configurações de impressora padrão por usuário.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

*Comando* \[ no\]
</dt> <dd>

a ação a ser executada.

Se o parâmetro de *nível* for diferente de zero, defina o valor desse parâmetro como zero. Nesse caso, a impressora retém seu estado atual e a função reconfigura os dados da impressora conforme especificado pelos parâmetros *Level* e *pPrinter* .

Se o parâmetro *Level* for zero, defina o valor desse parâmetro como um dos valores a seguir.



| Valor                                                                                                                                                                                                  | Significado                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PRINTER_CONTROL_PAUSE"></span><span id="printer_control_pause"></span><dl> <dt>**\_pausa de controle de impressora \_**</dt> </dl>                 | Pausar a impressora.<br/>                                                                                                                       |
| <span id="PRINTER_CONTROL_PURGE"></span><span id="printer_control_purge"></span><dl> <dt>**\_limpeza de controle de impressora \_**</dt> </dl>                 | Exclua todos os trabalhos de impressão na impressora.<br/>                                                                                                    |
| <span id="PRINTER_CONTROL_RESUME"></span><span id="printer_control_resume"></span><dl> <dt>**retomada de controle de impressora \_ \_**</dt> </dl>              | Retomar uma impressora pausada.<br/>                                                                                                                 |
| <span id="PRINTER_CONTROL_SET_STATUS"></span><span id="printer_control_set_status"></span><dl> <dt>**\_status do \_ conjunto de controle da impressora \_**</dt> </dl> | Defina o status da impressora.<br/> Defina o parâmetro *pPrinter* como um ponteiro para um valor **DWORD** que especifica o novo status da impressora.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.

Se a função falhar, o valor retornado será zero.

Se o *nível* for 7 e a ação de publicação falhar, **setprinter** retornará uma **\_ e/s de erro \_ pendente** e tentará concluir a ação em segundo plano. Se o *nível* for 7 e a ação de atualização falhar, o **setprinter** retornará o **arquivo de erro \_ \_ não \_ encontrado**.

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

Não é possível usar **Setprinter** para alterar a impressora padrão.

Para modificar as configurações atuais da impressora, chame a função [**Getprinter**](getprinter.md) para recuperar as configurações atuais em uma estrutura de [**informações da impressora \_ \_ 2**](printer-info-2.md) , modifique os membros dessa estrutura conforme necessário e, em seguida, chame **setprinter**.

A função **Setprinter** ignora os membros **pServerName**, **AveragePPM**, **status** e **cJobs** de uma estrutura de [**informações de impressora \_ \_ 2**](printer-info-2.md) .

Pausar uma impressora suspende o agendamento de todos os trabalhos de impressão para essa impressora, exceto para um trabalho de impressão que pode estar sendo impresso no momento. Os trabalhos de impressão podem ser enviados para uma impressora pausada, mas nenhum trabalho será agendado para impressão nessa impressora até que a impressão seja retomada. Se uma impressora for desmarcada, todos os trabalhos de impressão dessa impressora serão excluídos, exceto o trabalho de impressão atual.

Se você usar o **Setprinter** para modificar a estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) padrão de uma impressora (definindo globalmente os padrões da impressora), deverá primeiro chamar a função [**DocumentProperties**](documentproperties.md) para validar a estrutura **DEVMODE** .

Para as [**estruturas \_ informações \_ da impressora 2**](printer-info-2.md) e [**informações da impressora \_ \_ 3**](printer-info-3.md) que contêm um ponteiro para um descritor de segurança, a função pode definir somente os componentes do descritor de segurança que o chamador tem permissão para modificar. Para definir componentes específicos do descritor de segurança, você deve especificar os direitos de acesso necessários ao chamar a função [**OpenPrinter**](openprinter.md) ou [**OpenPrinter2**](openprinter2.md) para recuperar um identificador para a impressora. A tabela a seguir mostra os direitos de acesso necessários para modificar os vários componentes do descritor de segurança.



| Permissão de acesso            | Componente de descritor de segurança             |
|------------------------------|-------------------------------------------|
| **proprietário da gravação \_**             | Proprietário<br/> Grupo primário<br/> |
| **GRAVAR \_ DAC**               | DACL (lista de controle de acesso discricionário)  |
| **\_segurança do sistema de acesso \_** | Lista de controle de acesso (SACL) do sistema         |



 

Se o descritor de segurança contiver um componente que o chamador não tem o direito de acesso para modificar, o **Setprinter** falhará. Os componentes de um descritor de segurança que você não deseja modificar devem ser **nulos** ou não estar presentes, conforme apropriado. Se você não quiser modificar o descritor de segurança e chamar **Setprinter** com uma estrutura de [**informações da impressora \_ \_ 2**](printer-info-2.md) , defina o membro **pSecurityDescriptor** dessa estrutura como **NULL**.

O firewall de conexão com a Internet (ICF) bloqueia as portas de impressora por padrão, mas uma exceção para o compartilhamento de arquivos e impressoras pode ser habilitada. Se **Setprinter** for chamado por um administrador de máquina, ele habilitará a exceção. Se ele for chamado por um não administrador e a exceção ainda não tiver sido habilitada, a chamada falhará.

Você pode usar o nível 7 com a estrutura de [**informações da impressora \_ \_ 7**](printer-info-7.md) para publicar, cancelar a publicação ou atualizar os dados do serviço de diretório para a impressora. Os dados do serviço de diretório de uma impressora incluem todos os dados armazenados nas \_ \* chaves SPLDS por meio de chamadas para a função [**SetPrinterDataEx**](setprinterdataex.md) para a impressora. Antes de chamar **Setprinter**, defina o membro **pszObjectGUID** das **informações da impressora \_ \_ 7** como **NULL** e defina o membro *dwAction* como um dos valores a seguir.



| Valor                             | Descrição                                                                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **publicação do DSPRINT \_**<br/>   | Publica os dados do serviço de diretório.<br/>                                                                                                                                                                                                                                                                                                                                        |
| **republicação de DSPRINT \_**<br/> | Os dados do serviço de diretório da impressora não são publicados e, em seguida, publicados novamente, atualizando todas as propriedades na impressora publicada. A nova publicação também altera o GUID da impressora publicada. Use esse valor se você suspeitar de que os dados publicados da impressora estejam corrompidos.<br/>                                                                                         |
| **DSPRINT \_ Cancelar publicação**<br/> | Cancelar a publicação dos dados do serviço de diretório.<br/>                                                                                                                                                                                                                                                                                                                                      |
| **atualização do DSPRINT \_**<br/>    | Atualiza os dados do serviço de diretório. Isso é o mesmo que o **DSPRINT \_ Publish**, exceto que o **setprinter** falha com o **arquivo de erro \_ \_ não \_ encontrado** se a impressora ainda não estiver publicada.<br/> Use **a \_ atualização do DSPRINT** para atualizar as propriedades publicadas, mas não forçar a publicação. Os drivers de impressora sempre devem usar a **\_ atualização DSPRINT** em vez de **DSPRINT \_ Publish**.<br/> |



 

**DSPRINT \_ PENDENTE** não é um valor de *dwAction* válido para **setprinter**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>WinSpool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WinSpool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>WinSpool. drv</dt> </dl>                   |
| Nomes Unicode e ANSI<br/>   | **SetPrinterW** (Unicode) e **setprintera** (ANSI)<br/>                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinter**](addprinter.md)
</dt> <dt>

[**Getprinter**](getprinter.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**OpenPrinter2**](openprinter2.md)
</dt> <dt>

[**Informações da impressora \_ \_ 2**](printer-info-2.md)
</dt> <dt>

[**Informações da impressora \_ \_ 3**](printer-info-3.md)
</dt> <dt>

[**Informações da impressora \_ \_ 4**](printer-info-4.md)
</dt> <dt>

[**Informações da impressora \_ \_ 5**](printer-info-5.md)
</dt> <dt>

[**Informações da impressora \_ \_ 6**](printer-info-6.md)
</dt> <dt>

[**Informações da impressora \_ \_ 7**](printer-info-7.md)
</dt> <dt>

[**Informações da impressora \_ \_ 8**](printer-info-8.md)
</dt> <dt>

[**Informações da impressora \_ \_ 9**](printer-info-9.md)
</dt> <dt>

[**SetPrinterDataEx**](setprinterdataex.md)
</dt> </dl>

 

 




