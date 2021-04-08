---
description: A função FindNextPrinterChangeNotification recupera informações sobre a notificação de alteração mais recente para um objeto de notificação de alteração associado a um servidor de impressão ou impressora.
ms.assetid: ea7774ae-361f-41e4-bbc6-3f100028b22a
title: Função FindNextPrinterChangeNotification (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindNextPrinterChangeNotification
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: ef3ece0d4831409d79e2152cf7b6a37d6bbdc8b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828920"
---
# <a name="findnextprinterchangenotification-function"></a>Função FindNextPrinterChangeNotification

A função **FindNextPrinterChangeNotification** recupera informações sobre a notificação de alteração mais recente para um objeto de notificação de alteração associado a um servidor de impressão ou impressora. Chame essa função quando uma operação de espera no objeto de notificação de alteração for satisfeita.

A função também redefine o objeto de notificação de alteração para o estado não sinalizado. Você pode usar o objeto em outra operação de espera para continuar a monitorar a impressora ou o servidor de impressão. O sistema operacional definirá o objeto para o estado sinalizado na próxima vez que um de um conjunto especificado de alterações ocorrer na impressora ou no servidor de impressão. A função [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) cria o objeto de notificação de alteração e especifica o conjunto de alterações a ser monitorado.

## <a name="syntax"></a>Sintaxe


```C++
BOOL FindNextPrinterChangeNotification(
  _In_      HANDLE hChange,
  _Out_opt_ PDWORD pdwChange,
  _In_opt_  LPVOID pPrinterNotifyOptions,
  _Out_opt_ LPVOID *ppPrinterNotifyInfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hChange* \[ no\]
</dt> <dd>

Um identificador para um objeto de notificação de alteração associado a uma impressora ou a um servidor de impressão. Você obtém esse identificador chamando a função [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) . O sistema operacional define esse objeto de notificação de alteração para o estado sinalizado quando detecta uma das alterações especificadas no filtro de notificação de alteração do objeto.

</dd> <dt>

*pdwChange* \[ out, opcional\]
</dt> <dd>

Um ponteiro para uma variável cujos bits são definidos para indicar as alterações que ocorreram para causar a notificação mais recente. Os sinalizadores de bit que podem ser definidos correspondem àqueles especificados no parâmetro *fdwFilter* da chamada [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) . O sistema define um ou mais dos seguintes sinalizadores de bits.



| Valor                                                                                                                                                                                                                                             | Significado                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span id="PRINTER_CHANGE_ADD_FORM"></span><span id="printer_change_add_form"></span><dl> <dt>**\_ \_ Adicionar formulário de alteração de impressora \_**</dt> </dl>                                                     | Um formulário foi adicionado ao servidor.<br/>                |
| <span id="PRINTER_CHANGE_ADD_JOB"></span><span id="printer_change_add_job"></span><dl> <dt>**\_ \_ Adicionar trabalho de alteração de impressora \_**</dt> </dl>                                                        | Um trabalho de impressão foi enviado para a impressora.<br/>           |
| <span id="PRINTER_CHANGE_ADD_PORT"></span><span id="printer_change_add_port"></span><dl> <dt>**\_ \_ Adicionar porta alterar \_ impressora**</dt> </dl>                                                     | Uma porta ou monitor foi adicionado ao servidor.<br/>     |
| <span id="PRINTER_CHANGE_ADD_PRINT_PROCESSOR"></span><span id="printer_change_add_print_processor"></span><dl> <dt>**mudança de impressora \_ \_ Adicionar \_ processador de impressão \_**</dt> </dl>                   | Um processador de impressão foi adicionado ao servidor.<br/>     |
| <span id="PRINTER_CHANGE_ADD_PRINTER"></span><span id="printer_change_add_printer"></span><dl> <dt>**\_ \_ Adicionar impressora alterar \_ impressora**</dt> </dl>                                            | Uma impressora foi adicionada ao servidor.<br/>             |
| <span id="PRINTER_CHANGE_ADD_PRINTER_DRIVER"></span><span id="printer_change_add_printer_driver"></span><dl> <dt>**\_alterar impressora \_ Adicionar \_ Driver de impressora \_**</dt> </dl>                      | Um driver de impressora foi adicionado ao servidor.<br/>      |
| <span id="PRINTER_CHANGE_CONFIGURE_PORT"></span><span id="printer_change_configure_port"></span><dl> <dt>**\_porta de \_ configuração de alteração da impressora \_**</dt> </dl>                                   | Uma porta foi configurada no servidor.<br/>           |
| <span id="PRINTER_CHANGE_DELETE_FORM"></span><span id="printer_change_delete_form"></span><dl> <dt>**\_formulário de \_ exclusão de alteração de impressora \_**</dt> </dl>                                            | Um formulário foi excluído do servidor.<br/>            |
| <span id="PRINTER_CHANGE_DELETE_JOB"></span><span id="printer_change_delete_job"></span><dl> <dt>**\_trabalho de \_ exclusão de alteração de impressora \_**</dt> </dl>                                               | Um trabalho foi excluído.<br/>                             |
| <span id="PRINTER_CHANGE_DELETE_PORT"></span><span id="printer_change_delete_port"></span><dl> <dt>**\_porta de \_ exclusão de alteração de impressora \_**</dt> </dl>                                            | Uma porta ou monitor foi excluído do servidor.<br/> |
| <span id="PRINTER_CHANGE_DELETE_PRINT_PROCESSOR"></span><span id="printer_change_delete_print_processor"></span><dl> <dt>**\_processador de \_ exclusão de alteração \_ de impressora \_**</dt> </dl>          | Um processador de impressão foi excluído do servidor.<br/> |
| <span id="PRINTER_CHANGE_DELETE_PRINTER"></span><span id="printer_change_delete_printer"></span><dl> <dt>**impressora de \_ exclusão de alteração de impressora \_ \_**</dt> </dl>                                   | Uma impressora foi excluída.<br/>                         |
| <span id="PRINTER_CHANGE_DELETE_PRINTER_DRIVER"></span><span id="printer_change_delete_printer_driver"></span><dl> <dt>**\_Driver de \_ impressora de exclusão de alteração de impressora \_ \_**</dt> </dl>             | Um driver de impressora foi excluído do servidor.<br/>  |
| <span id="PRINTER_CHANGE_FAILED_CONNECTION_PRINTER"></span><span id="printer_change_failed_connection_printer"></span><dl> <dt>**impressora de conexão de alteração de impressora \_ \_ com falha \_ \_**</dt> </dl> | Falha em uma conexão de impressora.<br/>               |
| <span id="PRINTER_CHANGE_SET_FORM"></span><span id="printer_change_set_form"></span><dl> <dt>**\_formulário do \_ conjunto de alterações da impressora \_**</dt> </dl>                                                     | Um formulário foi definido no servidor.<br/>                  |
| <span id="PRINTER_CHANGE_SET_JOB"></span><span id="printer_change_set_job"></span><dl> <dt>**\_trabalho do \_ conjunto de alterações da impressora \_**</dt> </dl>                                                        | Um trabalho foi definido.<br/>                                 |
| <span id="PRINTER_CHANGE_SET_PRINTER"></span><span id="printer_change_set_printer"></span><dl> <dt>**\_impressora do \_ conjunto de alterações da impressora \_**</dt> </dl>                                            | Uma impressora foi definida.<br/>                             |
| <span id="PRINTER_CHANGE_SET_PRINTER_DRIVER"></span><span id="printer_change_set_printer_driver"></span><dl> <dt>**\_Driver de \_ impressora do conjunto de alterações de impressora \_ \_**</dt> </dl>                      | Um driver de impressora foi definido.<br/>                      |
| <span id="PRINTER_CHANGE_WRITE_JOB"></span><span id="printer_change_write_job"></span><dl> <dt>**\_trabalho de \_ gravação de alteração de impressora \_**</dt> </dl>                                                  | Os dados do trabalho foram gravados.<br/>                          |
| <span id="PRINTER_CHANGE_TIMEOUT"></span><span id="printer_change_timeout"></span><dl> <dt>**\_tempo limite de alteração da impressora \_**</dt> </dl>                                                         | O tempo limite do trabalho foi atingido.<br/>                             |
| <span id="PRINTER_CHANGE_SERVER"></span><span id="printer_change_server"></span><dl> <dt>**\_servidor de alteração de impressora \_**</dt> </dl>                                                            | Windows 7: ocorreu uma alteração no servidor.<br/>    |



 

</dd> <dt>

*pPrinterNotifyOptions* \[ em, opcional\]
</dt> <dd>

Um ponteiro para uma estrutura de [**\_ \_ Opções de notificação de impressora**](printer-notify-options.md) . Defina o membro **flags** desta estrutura para **Opções de \_ notificação de impressora \_ \_ Atualizar**, para fazer com que a função retorne os dados atuais para todos os campos de informações de impressora monitorados. A função ignora todos os outros membros da estrutura. Este parâmetro pode ser **NULL**.

</dd> <dt>

*ppPrinterNotifyInfo* \[ out, opcional\]
</dt> <dd>

Um ponteiro para uma variável de ponteiro que recebe um ponteiro para um buffer somente leitura alocado pelo sistema. Chame a função [**FreePrinterNotifyInfo**](freeprinternotifyinfo.md) para liberar o buffer quando tiver terminado de fazê-lo. Esse parâmetro poderá ser **nulo** se nenhuma informação for necessária.

O buffer contém uma estrutura de [**\_ \_ informações de notificação de impressora**](printer-notify-info.md) , que contém uma matriz de estruturas de [**\_ \_ \_ dados de informações de notificação de impressora**](printer-notify-info-data.md) . Cada elemento da matriz contém informações sobre um dos campos especificados no parâmetro *pPrinterNotifyOptions* da chamada [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) . Normalmente, a função fornece dados somente para os campos que foram alterados para causar a notificação mais recente. No entanto, se a estrutura apontada pelo parâmetro *pPrinterNotifyOptions* especificar **Opções de notificação de impressora \_ \_ \_ Atualizar**, a função fornecerá dados para todos os campos monitorados.

Se o bit de **notificação de informação de impressora \_ \_ \_ descartada** estiver definido no membro **flags** da estrutura de [**\_ \_ informações de notificação da impressora**](printer-notify-info.md) , ocorrerá um estouro ou erro e as notificações podem ter sido perdidas. Nesse caso, nenhuma notificação adicional será enviada até que você faça uma segunda chamada **FindNextPrinterChangeNotification** que especifica a **\_ atualização das \_ opções \_ de notificação de impressora**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.

Se a função falhar, o valor retornado será zero.

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

Chame a função **FindNextPrinterChangeNotification** depois que uma operação de espera em um objeto de notificação criado por [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) tiver sido satisfeita. Chamar **FindNextPrinterChangeNotification** permite que você obtenha informações sobre a alteração que satisfez a operação de espera e redefine o objeto de notificação para que ele possa ser sinalizado quando ocorrer a próxima alteração.

Com uma exceção, não chame a função **FindNextPrinterChangeNotification** se o objeto de notificação de alteração não estiver no estado sinalizado. Se uma função Wait retornar o **\_ tempo limite de espera** de valor, o objeto de alteração não estará no estado sinalizado. Chame a função **FindNextPrinterChangeNotification** somente se a função Wait for realizada com sucesso sem tempo limite. A exceção é quando **FindNextPrinterChangeNotification** é chamado com o bit de **\_ \_ \_ atualização opções de notificação de impressora** definido no parâmetro *pPrinterNotifyOptions* . Observe que mesmo quando esse sinalizador é definido, ainda é possível que o sinalizador **de \_ \_ informações de \_ notificação de impressora** seja definido no parâmetro *ppPrinterNotifyInfo* .

Para continuar a monitorar as alterações na impressora ou no servidor de impressão, repita o ciclo de chamar uma das [funções de espera](/windows/desktop/Sync/wait-functions) e, em seguida, chamando a função **FindNextPrinterChangeNotification** para examinar a alteração e redefinir o objeto de notificação.

**FindNextPrinterChangeNotification** pode combinar várias alterações no mesmo campo de informações de impressora em uma única notificação. Quando isso ocorre, a função normalmente recolhe todas as alterações do campo em uma única entrada na matriz de estruturas de [**\_ dados de \_ informações \_ de notificação de impressora**](printer-notify-info-data.md) em *ppPrinterNotifyInfo*; a única entrada relata apenas as informações mais atuais. No entanto, para alguns campos de informações de trabalho e impressora, a função pode retornar várias entradas de matriz para o mesmo campo. Nesse caso, a última entrada de matriz para o campo relata os dados atuais e as entradas anteriores contêm os dados para os estágios intermediários.

Quando você não precisar mais do objeto de notificação de alteração, feche-o chamando a função [**FindClosePrinterChangeNotification**](findcloseprinterchangenotification.md) .

> [!Note]  
> No Windows XP com Service Pack 2 (SP2) e posterior, o firewall de conexão com a Internet (ICF) bloqueia as portas de impressora por padrão, mas uma exceção para o compartilhamento de arquivos e impressoras pode ser habilitada. Se um usuário fizer uma conexão de impressora com outro computador e a exceção não estiver habilitada, o usuário não receberá notificações de alteração de impressora do servidor. Um administrador de máquina precisará habilitar a exceção.

 

## <a name="examples"></a>Exemplos

O exemplo de código a seguir ilustra como você pode monitorar o status da impressora usando essas funções.


```C++
// Get change notification handle for the printer   
chgObject = FindFirstPrinterChangeNotification( 
                hPrinter, 
                PRINTER_CHANGE_JOB, 
                0, 
                NULL); 

if (chgObject != INVALID_HANDLE_VALUE) {
    while (bKeepMonitoring) {
        // Wait for the change notification 
        WaitForSingleObject(chgObject, INFINITE);

        fcnreturn = FindNextPrinterChangeNotification(
                        chgObject, 
                        pdwChange, 
                        NULL, 
                        NULL);

        if (fcnreturn) {
            // Check value of *pdwChange and 
            //  deal with the indicated change 
        }
        // Insert some mechanism to stop monitoring
        //  such as: 
        //
        // if (something happens) {
        //     bKeepMonitoring = false; 
        // }
        //
    }
    // Close Printer Change Notification handle when finished. 
    FindClosePrinterChangeNotification(chgObject);
} else {
    // Unable to open printer change notification handle 
    dwStatus = GetLastError();
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**FindClosePrinterChangeNotification**](findcloseprinterchangenotification.md)
</dt> <dt>

[**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md)
</dt> <dt>

[**\_informações de notificação da impressora \_**](printer-notify-info.md)
</dt> <dt>

[**\_dados de \_ informações de notificação da impressora \_**](printer-notify-info-data.md)
</dt> <dt>

[**\_Opções de notificação de impressora \_**](printer-notify-options.md)
</dt> </dl>

 

