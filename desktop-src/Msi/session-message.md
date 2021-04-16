---
description: O método Message do objeto Session executa qualquer operação de registro em log habilitada e adia a execução para o objeto manipulador de interface do usuário associado ao mecanismo. O registro em log pode ser habilitado seletivamente para os vários tipos de mensagem. Consulte o método EnableLog.
ms.assetid: 09053700-a641-4970-bf55-d7c81f345257
title: Método Session. Message
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.Message
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e20cfebe0a3359a99770cbd242501649bf93f86e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750217"
---
# <a name="sessionmessage-method"></a>Método Session. Message

O método **Message** do objeto [**Session**](session-object.md) executa qualquer operação de registro em log habilitada e adia a execução para o objeto manipulador de interface do usuário associado ao mecanismo. O registro em log pode ser habilitado seletivamente para os vários tipos de mensagem. Consulte o método [**EnableLog**](installer-enablelog.md) .

Se o campo de registro 0 contiver uma cadeia de caracteres de formatação, ela será usada para formatar os dados nos outros campos. Caso contrário, se a mensagem for um erro, aviso ou mensagem de usuário, será feita uma tentativa de localizar um modelo de mensagem na tabela de erros do banco de dados atual usando o número de erro encontrado no campo 1 do registro para tipos de mensagem e valores de retorno.

## <a name="syntax"></a>Sintaxe


```JScript
Session.Message(
  kind,
  record
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*quase* 
</dt> <dd>

O parâmetro *Kind* é necessário para ser um dos valores a seguir. Para exibir uma caixa de mensagem com botões e ícones de push, calcule o valor de *tipo* adicionando os estilos de caixa de mensagem padrão usados por [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) e [**MessageBoxEx**](/windows/win32/api/winuser/nf-winuser-messageboxexa) a **msiMessageTypeError**, **msiMessageTypeWarning** ou **msiMessageTypeUser**. Para obter mais informações, consulte a seção comentários abaixo.



| Constante                                                                                                                                                                                                                                                                                                                 | Significado                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiMessageTypeFatalExit"></span><span id="msimessagetypefatalexit"></span><span id="MSIMESSAGETYPEFATALEXIT"></span><dl> <dt>**msiMessageTypeFatalExit**</dt> <dt>&H00000000</dt> </dl>                     | Encerramento prematuro, possivelmente fatal de memória insuficiente.<br/>                                                                              |
| <span id="msiMessageTypeError"></span><span id="msimessagetypeerror"></span><span id="MSIMESSAGETYPEERROR"></span><dl> <dt>**msiMessageTypeError**</dt> <dt>&H01000000</dt> </dl>                                     | Mensagem de erro formatada, \[ 1 \] é o número da mensagem na [tabela de erros](error-table.md).<br/>                                               |
| <span id="msiMessageTypeWarning"></span><span id="msimessagetypewarning"></span><span id="MSIMESSAGETYPEWARNING"></span><dl> <dt>**msiMessageTypeWarning**</dt> <dt>&H02000000</dt> </dl>                             | Mensagem de aviso formatada, \[ 1 \] é o número da mensagem na [tabela de erros](error-table.md).<br/>                                             |
| <span id="msiMessageTypeUser_"></span><span id="msimessagetypeuser_"></span><span id="MSIMESSAGETYPEUSER_"></span><dl> <dt> **msiMessageTypeUser**</dt> <dt>&H03000000</dt> </dl>                                     | Mensagem de solicitação do usuário, \[ 1 \] é o número da mensagem na [tabela de erros](error-table.md).<br/>                                                  |
| <span id="msiMessageTypeInfo"></span><span id="msimessagetypeinfo"></span><span id="MSIMESSAGETYPEINFO"></span><dl> <dt>**msiMessageTypeInfo**</dt> <dt>&H04000000</dt> </dl>                                         | Mensagem informativa para log, não a ser exibida.<br/>                                                                                 |
| <span id="msiMessageTypeFilesInUse"></span><span id="msimessagetypefilesinuse"></span><span id="MSIMESSAGETYPEFILESINUSE"></span><dl> <dt>**msiMessageTypeFilesInUse**</dt> <dt>&H05000000</dt> </dl>                 | Lista de arquivos em uso que precisam ser substituídos.<br/>                                                                                    |
| <span id="msiMessageTypeResolveSource"></span><span id="msimessagetyperesolvesource"></span><span id="MSIMESSAGETYPERESOLVESOURCE"></span><dl> <dt>**msiMessageTypeResolveSource**</dt> <dt>&H06000000</dt> </dl>     | Solicitação para determinar um local de origem válido.<br/>                                                                                     |
| <span id="msiMessageTypeOutOfDiskSpace"></span><span id="msimessagetypeoutofdiskspace"></span><span id="MSIMESSAGETYPEOUTOFDISKSPACE"></span><dl> <dt>**msiMessageTypeOutOfDiskSpace**</dt> <dt>&H07000000</dt> </dl> | Mensagem de espaço em disco insuficiente.<br/>                                                                                                  |
| <span id="msiMessageTypeActionStart"></span><span id="msimessagetypeactionstart"></span><span id="MSIMESSAGETYPEACTIONSTART"></span><dl> <dt>**msiMessageTypeActionStart**</dt> <dt>&H08000000</dt> </dl>             | Início da ação, \[ 1 \] nome da ação \[ , \] 2 Descrição, \[ 3 \] modelo para mensagens ACTIONDATA.<br/>                                    |
| <span id="msiMessageTypeActionData"></span><span id="msimessagetypeactiondata"></span><span id="MSIMESSAGETYPEACTIONDATA"></span><dl> <dt>**msiMessageTypeActionData**</dt> <dt>&H09000000</dt> </dl>                 | Dados de ação. Campos de registro correspondem ao modelo de mensagem ACTIONSTART.<br/>                                                     |
| <span id="msiMessageTypeProgress"></span><span id="msimessagetypeprogress"></span><span id="MSIMESSAGETYPEPROGRESS"></span><dl> <dt>**msiMessageTypeProgress**</dt> <dt>&H0A000000</dt> </dl>                         | Informações da barra de progresso. Consulte a descrição dos campos de registro abaixo.<br/>                                                             |
| <span id="msiMessageTypeCommonData_"></span><span id="msimessagetypecommondata_"></span><span id="MSIMESSAGETYPECOMMONDATA_"></span><dl> <dt> **msiMessageTypeCommonData**</dt> <dt>&H0B000000</dt> </dl>             | Para habilitar o botão Cancelar \[ , defina 1 \] como 2 e \[ 2 \] como 1. <br/> Para desabilitar o botão Cancelar \[ , defina 1 \] como 2 e \[ 2 \] como 0<br/> |



 

</dd> <dt>

*gravável* 
</dt> <dd>

Objeto de [**registro**](record-object.md) necessário contendo um campo específico da mensagem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor



| Constante                                                                                              | Valor         |
|-------------------------------------------------------------------------------------------------------|---------------|
| <dl> <dt>**msiMessageStatusError**</dt> </dl>  | -1<br/> |
| <dl> <dt>**msiMessageStatusNone**</dt> </dl>   | 0<br/>  |
| <dl> <dt>**msiMessageStatusOk**</dt> </dl>     | 1<br/>  |
| <dl> <dt>**msiMessageStatusCancel**</dt> </dl> | 2<br/>  |
| <dl> <dt>**msiMessageStatusAbort**</dt> </dl>  | 3<br/>  |
| <dl> <dt>**msiMessageStatusRetry**</dt> </dl>  | 4<br/>  |
| <dl> <dt>**msiMessageStatusIgnore**</dt> </dl> | 5<br/>  |
| <dl> <dt>**msiMessageStatusYes**</dt> </dl>    | 6<br/>  |
| <dl> <dt>**msiMessageStatusNo**</dt> </dl>     | 7<br/>  |



 

## <a name="remarks"></a>Comentários

**Campos de registro de mensagem**

O seguinte descreve as definições de campo de registro quando msiMessageTypeProgress é passado como o tipo de mensagem.

O campo 1 especifica o tipo da mensagem de progresso. O significado dos outros campos dependem do valor neste campo. Os valores possíveis que podem ser definidos no campo 1 são os seguintes.



| Nome da mensagem     | Valor | Descrição do campo 1                                                                                                 |
|------------------|-------|---------------------------------------------------------------------------------------------------------------------|
| MasterReset      | 0     | Redefine a barra de progresso e define o número total esperado de tiques na barra.                                         |
| ActionInfo       | 1     | Fornece informações relacionadas às mensagens de progresso a serem enviadas pela ação atual.                                 |
| ProgressReport   | 2     | Incrementa a barra de progresso.                                                                                        |
| ProgressAddition | 3     | Habilita uma ação (como CustomAction) para adicionar tiques ao número total esperado de progresso da barra de progresso. |



 

O significado do campo 2 depende do valor no campo 1, como a seguir.



| Valor do campo 1 | Descrição do campo 2                                                                                        |
|---------------|------------------------------------------------------------------------------------------------------------|
| 0             | Número total esperado de tiques na barra de progresso.                                                        |
| 1             | Número de tiques que a barra de progresso move para cada mensagem ActionData. Esse campo será ignorado se o campo 3 for 0. |
| 2             | Número de tiques movidos pela barra de progresso.                                                                |
| 3             | Número de tiques a serem adicionados ao progresso total esperado.                                                         |



 

O significado do campo 3 depende do valor no campo 1, como a seguir.



| Valor do campo 1 | Valor do campo 3 | Descrição do campo 3                                                                                             |
|---------------|---------------|-----------------------------------------------------------------------------------------------------------------|
| 0             | 0             | Barra de progresso de encaminhamento (da esquerda para a direita)                                                                            |
|               | 1             | Barra de progresso de retrocesso (direita para esquerda)                                                                           |
| 1             | 0             | A ação atual enviará mensagens ProgressReport explícitas.                                                  |
|               | 1             | Incrementar a barra de progresso pelo número de tiques especificado no campo 2 sempre que uma mensagem ActionData for enviada. |
| 2             | Não usado        |                                                                                                                 |
| 3             | Não usado        |                                                                                                                 |



 

O significado do campo 4 depende do valor no campo 1, como a seguir.



| Valor do campo 1 | Valor do campo 4 | Descrição do campo 4                                                                                                                                 |
|---------------|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| 0             | 0             | A execução está em andamento. Nesse caso, a interface do usuário pode calcular e exibir o tempo restante.                                                      |
|               | 1             | Criando o script de execução. Nesse caso, a interface do usuário pode exibir uma mensagem para aguardar enquanto o instalador termina de preparar a instalação. |
| 1             | Não usado        |                                                                                                                                                     |
| 2             | Não usado        |                                                                                                                                                     |
| 3             | Não usado        |                                                                                                                                                     |



 

**Exibindo caixas de mensagens**

Para exibir uma caixa de mensagem com botões e ícones de push, calcule o valor de *tipo* adicionando os estilos de caixa de mensagem padrão usados por **MessageBox** e **MessageBoxEx** a **msiMessageTypeError**, **msiMessageTypeWarning** ou **msiTypeUser**. As opções de botão de ação disponíveis para VBScript são vbOKOnly (MB \_ OK), vbOKCancel (MB \_ OKCANCEL), VBABORTRETRYIGNORE (MB \_ ABORTRETRYIGNORE), vbYesNoCancel (MB \_ YESNOCANCEL), vbYesNo (MB \_ YesNo) e vbRetryCancel (MB \_ RETRYCANCEL). As opções de ícone disponíveis para VBScript são vbCritical (MB \_ ICONERROR), vbQuestion (MB \_ ICONQUESTION), VBEXCLAMATION (MB \_ ICONWARNING) e vbInformation (MB \_ ICONINFORMATION).

Por exemplo, a chamada a seguir envia uma mensagem **msiMessageTypeError** com os botões ícone VbExclamation e vbYesNo.


```VB
Session.Message &H01000034, record
```



Se uma ação personalizada chamar o método **Message** , a ação personalizada deverá ser capaz de manipular um cancelamento pelo usuário e deve retornar **msiDoActionStatusUserExit**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession é definido como 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 
