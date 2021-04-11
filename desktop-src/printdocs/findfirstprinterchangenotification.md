---
description: A função FindFirstPrinterChangeNotification cria um objeto de notificação de alteração e retorna um identificador para o objeto. Você pode usar esse identificador em uma chamada para uma das funções de espera para monitorar as alterações na impressora ou no servidor de impressão.
ms.assetid: 4155ef5c-cd96-4960-919b-d9a495bb73a5
title: Função FindFirstPrinterChangeNotification (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindFirstPrinterChangeNotification
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 2da6a2ae73aa5b987ea3b8f8789f81ed0b4cdf06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169465"
---
# <a name="findfirstprinterchangenotification-function"></a>Função FindFirstPrinterChangeNotification

A função **FindFirstPrinterChangeNotification** cria um objeto de notificação de alteração e retorna um identificador para o objeto. Você pode usar esse identificador em uma chamada para uma das funções de espera para monitorar as alterações na impressora ou no servidor de impressão.

A chamada **FindFirstPrinterChangeNotification** especifica o tipo de alterações a serem monitoradas. Você pode especificar um conjunto de condições para monitorar alterações, um conjunto de campos de informações de impressora para monitorar ou ambos.

Uma operação de espera no identificador de notificação de alteração é realizada com sucesso quando uma das alterações especificadas ocorre na impressora ou no servidor de impressão especificado. Em seguida, você chama a função [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) para recuperar informações sobre a alteração e para redefinir o objeto de notificação de alteração para uso na próxima operação de espera.

## <a name="syntax"></a>Sintaxe


```C++
HANDLE FindFirstPrinterChangeNotification(
  _In_     HANDLE hPrinter,
           DWORD  fdwFilter,
           DWORD  fdwOptions,
  _In_opt_ LPVOID pPrinterNotifyOptions
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hPrinter* \[ no\]
</dt> <dd>

Um identificador para a impressora ou o servidor de impressão que você deseja monitorar. Use a função [**OpenPrinter**](openprinter.md) ou [**addprintr**](addprinter.md) para recuperar um identificador de impressora.

</dd> <dt>

*fdwFilter* 
</dt> <dd>

As condições que farão com que o objeto de notificação de alteração entre em um estado sinalizado. Uma notificação de alteração ocorre quando uma ou mais das condições especificadas são atendidas. O parâmetro *fdwFilter* pode ser zero se *PPrinterNotifyOptions* não for **nulo**.

Esse parâmetro pode ser um ou mais dos valores a seguir.



| Valor                                                                                                                                                                                                              | Significado                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PRINTER_CHANGE_FORM"></span><span id="printer_change_form"></span><dl> <dt>**\_formulário de alteração de impressora \_**</dt> </dl>                                   | Notificação de qualquer alteração em um formulário. Você pode definir esse sinalizador geral ou um ou mais dos seguintes sinalizadores específicos:<br/> <dl> <dd>\_ \_ Adicionar formulário de alteração de impressora \_</dd> <dd>\_formulário do \_ conjunto de alterações da impressora \_</dd> <dd>\_formulário de \_ exclusão de alteração de impressora \_</dd> </dl>                                                                              |
| <span id="PRINTER_CHANGE_JOB"></span><span id="printer_change_job"></span><dl> <dt>**\_trabalho de alteração de impressora \_**</dt> </dl>                                      | Notificação de qualquer alteração em um trabalho. Você pode definir esse sinalizador geral ou um ou mais dos seguintes sinalizadores específicos:<br/> <dl> <dd>\_ \_ Adicionar trabalho de alteração de impressora \_</dd> <dd>\_trabalho do \_ conjunto de alterações da impressora \_</dd> <dd>\_trabalho de \_ exclusão de alteração de impressora \_</dd> <dd>\_trabalho de \_ gravação de alteração de impressora \_</dd> </dl>                                  |
| <span id="PRINTER_CHANGE_PORT"></span><span id="printer_change_port"></span><dl> <dt>**\_porta de alteração de impressora \_**</dt> </dl>                                   | Notificação de qualquer alteração em uma porta. Você pode definir esse sinalizador geral ou um ou mais dos seguintes sinalizadores específicos:<br/> <dl> <dd>\_ \_ Adicionar porta alterar \_ impressora</dd> <dd>\_porta de \_ configuração de alteração da impressora \_ </dd> <dd>\_porta de \_ exclusão de alteração de impressora \_</dd> </dl>                                                                       |
| <span id="PRINTER_CHANGE_PRINT_PROCESSOR"></span><span id="printer_change_print_processor"></span><dl> <dt>**\_processador de \_ impressão de alteração de impressora \_**</dt> </dl> | Notificação de qualquer alteração em um processador de impressão. Você pode definir esse sinalizador geral ou um ou mais dos seguintes sinalizadores específicos: <br/> <dl> <dd>mudança de impressora \_ \_ Adicionar \_ processador de impressão \_ </dd> <dd>\_processador de \_ exclusão de alteração \_ de impressora \_</dd> </dl>                                                                                        |
| <span id="PRINTER_CHANGE_PRINTER"></span><span id="printer_change_printer"></span><dl> <dt>**impressora de alteração de impressora \_ \_**</dt> </dl>                          | Notificação de qualquer alteração em uma impressora. Você pode definir esse sinalizador geral ou um ou mais dos seguintes sinalizadores específicos:<br/> <dl> <dd>\_ \_ Adicionar impressora alterar \_ impressora</dd> <dd>\_impressora do \_ conjunto de alterações da impressora \_</dd> <dd>impressora de \_ exclusão de alteração de impressora \_ \_</dd> <dd>impressora de conexão de alteração de impressora \_ \_ com falha \_ \_</dd> </dl> |
| <span id="PRINTER_CHANGE_PRINTER_DRIVER"></span><span id="printer_change_printer_driver"></span><dl> <dt>**IMPRESSORA \_ alterar \_ Driver de impressora \_**</dt> </dl>    | Notificação de qualquer alteração em um driver de impressora. Você pode definir esse sinalizador geral ou um ou mais dos seguintes sinalizadores específicos:<br/> <dl> <dd>\_alterar impressora \_ Adicionar \_ Driver de impressora \_</dd> <dd>\_Driver de \_ impressora do conjunto de alterações de impressora \_ \_</dd> <dd>\_Driver de \_ impressora de exclusão de alteração de impressora \_ \_</dd> </dl>                                   |
| <span id="PRINTER_CHANGE_ALL"></span><span id="printer_change_all"></span><dl> <dt>**IMPRESSORA \_ alterar \_ tudo**</dt> </dl>                                      | Notifique se alguma das alterações anteriores ocorrer.<br/>                                                                                                                                                                                                                                                                                                                     |
| <span id="PRINTER_CHANGE_SERVER"></span><span id="printer_change_server"></span><dl> <dt>**\_servidor de alteração de impressora \_**</dt> </dl>                             | Windows 7: notificar quaisquer alterações no servidor.<br/> Esse sinalizador não é incluído nas alterações monitoradas pela definição da **opção \_ alterar a impressora \_ todos os** valores.<br/>                                                                                                                                                                                                      |



 

Para obter descrições dos sinalizadores mais específicos na tabela anterior, consulte a função [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) .

</dd> <dt>

*fdwOptions* 
</dt> <dd>

O sinalizador que determina a categoria de impressoras para as quais as notificações funcionarão.



| Valor                                                                                                                                                                                                                                                               | Significado                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PRINTER_NOTIFY_CATEGORY_ALL"></span><span id="printer_notify_category_all"></span><dl> <dt>**Impressora \_ NOTIFICAr \_ categoria \_ todos os**</dt> <dt>0x001000</dt> </dl> | [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) retorna notificações para impressoras 2D e 3D.<br/> |
| <span id="PRINTER_NOTIFY_CATEGORY_3D"></span><span id="printer_notify_category_3d"></span><dl> <dt>**Impressora \_ NOTIFICAr \_ categoria \_ 3D**</dt> <dt>0x002000</dt> </dl>    | [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) retorna notificações somente para impressoras 3D.<br/>        |



 

Quando esse sinalizador é definido como zero (0), **FindFirstPrinterChangeNotification** só funcionará para impressoras 2D. Esse é o valor padrão.

</dd> <dt>

*pPrinterNotifyOptions* \[ em, opcional\]
</dt> <dd>

Um ponteiro para uma estrutura de [**\_ \_ Opções de notificação de impressora**](printer-notify-options.md) . O membro **pTypes** dessa estrutura é uma matriz de uma ou mais [**Opções de \_ \_ \_ tipo de opção de notificação de impressora**](printer-notify-options-type.md) , cada uma delas especifica um campo de informações de impressora a ser monitorado. Uma notificação de alteração ocorre quando um ou mais campos especificados são alterados. Quando ocorre uma alteração, a função [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) pode recuperar as novas informações da impressora. Esse parâmetro poderá ser **nulo** se *fdwFilter* for diferente de zero.

Para obter uma lista de campos que podem ser monitorados, consulte [**Opções de notificação de impressora \_ \_ \_ tipo**](printer-notify-options-type.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, o valor de retorno será um identificador para um objeto de notificação de alteração associado à impressora ou ao servidor de impressão especificado.

Se a função falhar, o valor de retorno será um \_ valor de identificador inválido \_ .

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

Para monitorar uma impressora ou um servidor de impressão, chame a função **FindFirstPrinterChangeNotification** e, em seguida, use o identificador de objeto de notificação de alteração retornado em uma chamada para uma das [funções de espera](/windows/desktop/Sync/wait-functions). Uma operação de espera em um objeto de notificação de alteração é satisfeita quando o objeto de notificação de alteração entra no estado sinalizado. O sistema sinaliza o objeto quando uma ou mais das alterações especificadas por *fdwFilter* ou *pPrinterNotifyOptions* ocorre na impressora monitorada ou no servidor de impressão.

Quando você chama **FindFirstPrinterChangeNotification**, *fdwFilter* deve ser diferente de zero ou o *pPrinterNotifyOptions* deve ser não **nulo**. Se ambos forem especificados, as notificações ocorrerão para ambos.

Quando uma operação de espera em um objeto de notificação de alteração de impressora for satisfeita, chame a função [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) para determinar a causa da notificação. Para uma condição especificada por *fdwFilter*, **FindNextPrinterChangeNotification** relata a condição ou condições que foram alteradas. Para um campo de informações de impressora especificado por *pPrinterNotifyOptions*, **FindNextPrinterChangeNotification** relata o campo ou os campos que foram alterados, bem como as novas informações para esses campos. **FindNextPrinterChangeNotification** também redefine o objeto de notificação de alteração para o estado não sinalizado para que você possa usá-lo em outra operação de espera para continuar a monitorar a impressora ou o servidor de impressão.

Com uma exceção, não chame a função [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) se o objeto de notificação de alteração não estiver no estado sinalizado. Se a função Wait retornar o tempo limite de espera de valor \_ , o objeto de alteração não estará no estado sinalizado. Chame a função **FindNextPrinterChangeNotification** somente se a função Wait for realizada com sucesso sem tempo limite. A exceção é quando **FindNextPrinterChangeNotification** é chamado com o \_ bit de atualização opções de notificação de impressora \_ \_ definido no parâmetro *pPrinterNotifyOptions* .

Quando você não precisar mais do objeto de notificação de alteração, feche-o chamando a função [**FindClosePrinterChangeNotification**](findcloseprinterchangenotification.md) .

Os chamadores de **FindFirstPrinterChangeNotification** devem garantir que o identificador da impressora passado para **FindFirstPrinterChangeNotification** permaneça válido até que [**FindClosePrinterChangeNotification**](findcloseprinterchangenotification.md) seja chamado. Se o identificador da impressora for fechado antes do identificador de notificação de alteração da impressora, outras notificações não serão entregues.

**FindFirstPrinterChangeNotification** não enviará notificações de alteração para impressoras 3D para identificadores do servidor.

> [!Note]  
> No Windows XP com Service Pack 2 (SP2) e posterior, o firewall de conexão com a Internet (ICF) bloqueia as portas de impressora por padrão, mas uma exceção para o compartilhamento de arquivos e impressoras pode ser habilitada. Se um usuário fizer uma conexão de impressora com outro computador e a exceção não estiver habilitada, o usuário não receberá notificações de alteração de impressora do servidor. Um administrador de máquina precisará habilitar a exceção.

 

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

[**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**\_Opções de notificação de impressora \_**](printer-notify-options.md)
</dt> <dt>

[**\_tipo de \_ Opções de notificação de impressora \_**](printer-notify-options-type.md)
</dt> </dl>

 

