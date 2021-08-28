---
description: A função FindNextPrinterChangeNotification recupera informações sobre a notificação de alteração mais recente para um objeto de notificação de alteração associado a uma impressora ou servidor de impressão.
ms.assetid: ea7774ae-361f-41e4-bbc6-3f100028b22a
title: Função FindNextPrinterChangeNotification (Winspool.h)
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
ms.openlocfilehash: 37b05603a75f7bc8e68ead2d0dffdec2e99e7618e5461360760f2d9c89ae52da
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112476"
---
# <a name="findnextprinterchangenotification-function"></a>Função FindNextPrinterChangeNotification

A **função FindNextPrinterChangeNotification** recupera informações sobre a notificação de alteração mais recente para um objeto de notificação de alteração associado a uma impressora ou servidor de impressão. Chame essa função quando uma operação de espera no objeto de notificação de alteração for atendida.

A função também redefine o objeto de notificação de alteração para o estado não sinalizado. Em seguida, você pode usar o objeto em outra operação de espera para continuar monitorando a impressora ou o servidor de impressão. O sistema operacional definirá o objeto como o estado sinalizado na próxima vez que ocorrer uma das alterações especificadas no servidor de impressão ou impressora. A [**função FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) cria o objeto de notificação de alteração e especifica o conjunto de alterações a serem monitoradas.

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

*hChange* \[ Em\]
</dt> <dd>

Um identificador para um objeto de notificação de alteração associado a uma impressora ou servidor de impressão. Você obtém esse tipo de alça chamando a [**função FindFirstPrinterChangeNotification.**](findfirstprinterchangenotification.md) O sistema operacional define esse objeto de notificação de alteração para o estado sinalizado quando detecta uma das alterações especificadas no filtro de notificação de alteração do objeto.

</dd> <dt>

*pdwChange* \[ out, opcional\]
</dt> <dd>

Um ponteiro para uma variável cujos bits são definidos para indicar as alterações que ocorreram para causar a notificação mais recente. Os sinalizadores de bit que podem ser definidos correspondem aos especificados no parâmetro *fdwFilter* da [**chamada FindFirstPrinterChangeNotification.**](findfirstprinterchangenotification.md) O sistema define um ou mais dos sinalizadores de bits a seguir.



| Valor                                                                                                                                                                                                                                             | Significado                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span id="PRINTER_CHANGE_ADD_FORM"></span><span id="printer_change_add_form"></span><dl> <dt>**ALTERAÇÃO \_ DA IMPRESSORA ADICIONAR \_ \_ FORMULÁRIO**</dt> </dl>                                                     | Um formulário foi adicionado ao servidor.<br/>                |
| <span id="PRINTER_CHANGE_ADD_JOB"></span><span id="printer_change_add_job"></span><dl> <dt>**ALTERAÇÃO \_ DA IMPRESSORA ADICIONAR \_ \_ TRABALHO**</dt> </dl>                                                        | Um trabalho de impressão foi enviado para a impressora.<br/>           |
| <span id="PRINTER_CHANGE_ADD_PORT"></span><span id="printer_change_add_port"></span><dl> <dt>**ALTERAÇÃO \_ DA IMPRESSORA ADICIONAR \_ \_ PORTA**</dt> </dl>                                                     | Uma porta ou monitor foi adicionado ao servidor.<br/>     |
| <span id="PRINTER_CHANGE_ADD_PRINT_PROCESSOR"></span><span id="printer_change_add_print_processor"></span><dl> <dt>**ALTERAÇÃO \_ DA IMPRESSORA ADICIONAR PROCESSADOR DE \_ \_ \_ IMPRESSÃO**</dt> </dl>                   | Um processador de impressão foi adicionado ao servidor.<br/>     |
| <span id="PRINTER_CHANGE_ADD_PRINTER"></span><span id="printer_change_add_printer"></span><dl> <dt>**ALTERAÇÃO \_ DA IMPRESSORA ADICIONAR \_ \_ IMPRESSORA**</dt> </dl>                                            | Uma impressora foi adicionada ao servidor.<br/>             |
| <span id="PRINTER_CHANGE_ADD_PRINTER_DRIVER"></span><span id="printer_change_add_printer_driver"></span><dl> <dt>**ALTERAÇÃO \_ DA IMPRESSORA ADICIONAR DRIVER DE \_ \_ \_ IMPRESSORA**</dt> </dl>                      | Um driver de impressora foi adicionado ao servidor.<br/>      |
| <span id="PRINTER_CHANGE_CONFIGURE_PORT"></span><span id="printer_change_configure_port"></span><dl> <dt>**ALTERAÇÃO \_ DA IMPRESSORA CONFIGURAR \_ \_ PORTA**</dt> </dl>                                   | Uma porta foi configurada no servidor.<br/>           |
| <span id="PRINTER_CHANGE_DELETE_FORM"></span><span id="printer_change_delete_form"></span><dl> <dt>**FORMULÁRIO DE \_ EXCLUSÃO \_ DE ALTERAÇÃO DE \_ IMPRESSORA**</dt> </dl>                                            | Um formulário foi excluído do servidor.<br/>            |
| <span id="PRINTER_CHANGE_DELETE_JOB"></span><span id="printer_change_delete_job"></span><dl> <dt>**TRABALHO DE \_ EXCLUSÃO DE \_ ALTERAÇÃO DE \_ IMPRESSORA**</dt> </dl>                                               | Um trabalho foi excluído.<br/>                             |
| <span id="PRINTER_CHANGE_DELETE_PORT"></span><span id="printer_change_delete_port"></span><dl> <dt>**ALTERAR \_ A PORTA DE \_ \_ EXCLUSÃO DA IMPRESSORA**</dt> </dl>                                            | Uma porta ou monitor foi excluído do servidor.<br/> |
| <span id="PRINTER_CHANGE_DELETE_PRINT_PROCESSOR"></span><span id="printer_change_delete_print_processor"></span><dl> <dt>**ALTERAÇÃO DA \_ IMPRESSORA EXCLUIR PROCESSADOR DE \_ \_ \_ IMPRESSÃO**</dt> </dl>          | Um processador de impressão foi excluído do servidor.<br/> |
| <span id="PRINTER_CHANGE_DELETE_PRINTER"></span><span id="printer_change_delete_printer"></span><dl> <dt>**IMPRESSORA \_ DE \_ EXCLUSÃO DE ALTERAÇÃO DE \_ IMPRESSORA**</dt> </dl>                                   | Uma impressora foi excluída.<br/>                         |
| <span id="PRINTER_CHANGE_DELETE_PRINTER_DRIVER"></span><span id="printer_change_delete_printer_driver"></span><dl> <dt>**ALTERAÇÃO DA \_ IMPRESSORA EXCLUIR DRIVER DE \_ \_ \_ IMPRESSORA**</dt> </dl>             | Um driver de impressora foi excluído do servidor.<br/>  |
| <span id="PRINTER_CHANGE_FAILED_CONNECTION_PRINTER"></span><span id="printer_change_failed_connection_printer"></span><dl> <dt>**IMPRESSORA COM \_ FALHA NA ALTERAÇÃO DA \_ \_ \_ IMPRESSORA**</dt> </dl> | Falha em uma conexão de impressora.<br/>               |
| <span id="PRINTER_CHANGE_SET_FORM"></span><span id="printer_change_set_form"></span><dl> <dt>**FORMULÁRIO DO \_ CONJUNTO DE ALTERAÇÕES DA \_ \_ IMPRESSORA**</dt> </dl>                                                     | Um formulário foi definido no servidor.<br/>                  |
| <span id="PRINTER_CHANGE_SET_JOB"></span><span id="printer_change_set_job"></span><dl> <dt>**TRABALHO DO \_ CONJUNTO DE ALTERAÇÕES DA \_ \_ IMPRESSORA**</dt> </dl>                                                        | Um trabalho foi definido.<br/>                                 |
| <span id="PRINTER_CHANGE_SET_PRINTER"></span><span id="printer_change_set_printer"></span><dl> <dt>**IMPRESSORA DO \_ CONJUNTO DE ALTERAÇÕES DA \_ \_ IMPRESSORA**</dt> </dl>                                            | Uma impressora foi definida.<br/>                             |
| <span id="PRINTER_CHANGE_SET_PRINTER_DRIVER"></span><span id="printer_change_set_printer_driver"></span><dl> <dt>**DRIVER DE \_ IMPRESSORA DO CONJUNTO DE ALTERAÇÕES DA \_ \_ \_ IMPRESSORA**</dt> </dl>                      | Um driver de impressora foi definido.<br/>                      |
| <span id="PRINTER_CHANGE_WRITE_JOB"></span><span id="printer_change_write_job"></span><dl> <dt>**TRABALHO DE \_ GRAVAÇÃO DE ALTERAÇÃO DE \_ \_ IMPRESSORA**</dt> </dl>                                                  | Os dados do trabalho foram gravados.<br/>                          |
| <span id="PRINTER_CHANGE_TIMEOUT"></span><span id="printer_change_timeout"></span><dl> <dt>**TEMPO DE \_ TEMPO DE ALTERAÇÃO DA \_ IMPRESSORA**</dt> </dl>                                                         | O trabalho foi eliminado.<br/>                             |
| <span id="PRINTER_CHANGE_SERVER"></span><span id="printer_change_server"></span><dl> <dt>**SERVIDOR DE \_ ALTERAÇÃO DE \_ IMPRESSORA**</dt> </dl>                                                            | Windows 7: ocorreu uma alteração no servidor.<br/>    |



 

</dd> <dt>

*pPrinterNotifyOptions* \[ in, opcional\]
</dt> <dd>

Um ponteiro para uma estrutura [**PRINTER \_ NOTIFY \_ OPTIONS.**](printer-notify-options.md) De definir **o membro Sinalizadores** dessa estrutura como **PRINTER NOTIFY OPTIONS \_ \_ \_ REFRESH**, para fazer com que a função retorne os dados atuais para todos os campos de informações de impressora monitorados. A função ignora todos os outros membros da estrutura. Este parâmetro pode ser **NULL**.

</dd> <dt>

*ppPrinterNotifyInfo* \[ out, opcional\]
</dt> <dd>

Um ponteiro para uma variável de ponteiro que recebe um ponteiro para um buffer somente leitura alocado pelo sistema. Chame a [**função FreePrinterNotifyInfo**](freeprinternotifyinfo.md) para liberar o buffer quando terminar de fazer isso. Esse parâmetro poderá ser **NULL** se nenhuma informação for necessária.

O buffer contém uma estrutura [**PRINTER \_ NOTIFY \_ INFO,**](printer-notify-info.md) que contém uma matriz de estruturas [**DE DADOS PRINTER NOTIFY \_ \_ \_ INFO.**](printer-notify-info-data.md) Cada elemento da matriz contém informações sobre um dos campos especificados no parâmetro *pPrinterNotifyOptions* da [**chamada FindFirstPrinterChangeNotification.**](findfirstprinterchangenotification.md) Normalmente, a função fornece dados somente para os campos que foram alterados para causar a notificação mais recente. No entanto, se a estrutura apontada pelo parâmetro *pPrinterNotifyOptions* especificar **PRINTER NOTIFY OPTIONS \_ \_ \_ REFRESH**, a função fornece dados para todos os campos monitorados.

Se o bit **PRINTER \_ NOTIFY INFO \_ \_ DISCARDED** estiver definido no membro **Flags** da estrutura [**PRINTER NOTIFY \_ \_ INFO,**](printer-notify-info.md) um estouro ou erro poderá ter sido perdido. Nesse caso, nenhuma notificação adicional será enviada até que você faça uma segunda chamada **FindNextPrinterChangeNotification** que especifique **PRINTER NOTIFY OPTIONS \_ \_ \_ REFRESH**.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será um valor não zero.

Se a função falhar, o valor retornado será zero.

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração do servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

Chame a **função FindNextPrinterChangeNotification** após uma operação de espera em um objeto de notificação criado por [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) ter sido atendida. Chamar **FindNextPrinterChangeNotification** permite obter informações sobre a alteração que atendia a operação de espera e redefine o objeto de notificação para que ele possa ser sinalizado quando a próxima alteração ocorrer.

Com uma exceção, não chame a **função FindNextPrinterChangeNotification** se o objeto de notificação de alteração não estiver no estado sinalizado. Se uma função wait retornar o **valor WAIT \_ TIMEOUT**, o objeto de alteração não está no estado sinalizado. Chame a **função FindNextPrinterChangeNotification** somente se a função de espera for bem-sucedida sem tempo de vida. A exceção é **quando FindNextPrinterChangeNotification** é chamado com o bit **REFRESH PRINTER NOTIFY \_ \_ \_ OPTIONS** definido no *parâmetro pPrinterNotifyOptions.* Observe que, mesmo quando esse sinalizador é definido, ainda é possível que o sinalizador **PRINTER \_ NOTIFY INFO \_ \_ DISCARDED** seja definido no *parâmetro ppPrinterNotifyInfo.*

Para continuar monitorando a impressora ou o servidor de impressão [](/windows/desktop/Sync/wait-functions) em busca de alterações, repita o ciclo de chamada a uma das funções de espera e, em seguida, chamando a função **FindNextPrinterChangeNotification** para examinar a alteração e redefinir o objeto de notificação.

**FindNextPrinterChangeNotification** pode combinar várias alterações no mesmo campo de informações da impressora em uma única notificação. Quando isso ocorre, a função normalmente colapsa todas as alterações do campo em uma única entrada na matriz de estruturas [**PRINTER \_ NOTIFY INFO \_ \_ DATA**](printer-notify-info-data.md) em *ppPrinterNotifyInfo*; a única entrada relata apenas as informações mais atuais. No entanto, para alguns campos de informações de trabalho e impressora, a função pode retornar várias entradas de matriz para o mesmo campo. Nesse caso, a última entrada de matriz para o campo relata os dados atuais e as entradas anteriores contêm os dados para os estágios intermediários.

Quando você não precisar mais do objeto de notificação de alteração, feche-o chamando a [**função FindClosePrinterChangeNotification.**](findcloseprinterchangenotification.md)

> [!Note]  
> No Windows XP com Service Pack 2 (SP2) e posterior, o Firewall de Conexão com a Internet (ICF) bloqueia as portas da impressora por padrão, mas uma exceção para Compartilhamento de Arquivos e Impressão pode ser habilitada. Se um usuário fizer uma conexão de impressora com outro computador e a exceção não estiver habilitada, o usuário não receberá notificações de alteração de impressora do servidor. Um administrador de computador terá que habilitar a exceção.

 

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

 

