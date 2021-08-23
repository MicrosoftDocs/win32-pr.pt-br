---
description: Executa uma operação em um arquivo especificado.
ms.assetid: ce652565-40b6-4f69-bd2a-9e05e3f360ac
title: Função WOWShellExecute
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WOWShellExecute
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 4389c348a06b7c54dc899da8114eee09e740681f043084bb0c32ab9f7163772e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119591826"
---
# <a name="wowshellexecute-function"></a>Função WOWShellExecute

\[essa função está disponível por meio do Windows XP com Service Pack 2 (SP2) e Windows Server 2003. Ele pode ser alterado ou indisponível nas versões subsequentes do Windows.\]

Executa uma operação em um arquivo especificado. **WOWShellExecute** existe apenas para uso com o Ntvdm.exe (computador Virtual dos) da Microsoft Windows NT, que permite que o sistema operacional de disco (dos) e o software de 16 bits sejam executados em um sistema Windows e não deve ser usado por outras pessoas. Em vez disso, use [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) .

## <a name="syntax"></a>Sintaxe


```C++
HINSTANCE WOWShellExecute(
  _In_ HWND    hwnd,
  _In_ LPCTSTR lpOperation,
  _In_ LPCTSTR lpFile,
  _In_ LPCTSTR lpParameters,
  _In_ LPCTSTR lpDirectory,
  _In_ INT     nShowCmd,
       void    *lpfnCBWinExec
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HWND* \[ no\]
</dt> <dd>

Digite: **HWND**

Um identificador para a janela do proprietário usado para exibir uma interface do usuário ou mensagens de erro. Esse valor pode ser **nulo** se a operação não estiver associada a uma janela.

</dd> <dt>

*lpOperation* \[ no\]
</dt> <dd>

Tipo: **LPCTSTR**

Um ponteiro para uma cadeia de caracteres terminada em **nulo**, referido neste caso como um *verbo*, que especifica a ação a ser executada. O conjunto de verbos disponíveis depende do arquivo ou da pasta em particular. Em geral, as ações disponíveis no menu de atalho de um objeto são verbos disponíveis. Para obter mais informações sobre verbos e sua disponibilidade, consulte a seção *verbos de objeto* de [iniciando aplicativos](launch.md). Consulte [estendendo menus de atalho](context.md) para mais discussões sobre menus de atalho. Os verbos a seguir são usados com frequência.

<dt>

<span id="edit"></span><span id="EDIT"></span>

<span id="edit"></span><span id="EDIT"></span>**editar**


</dt> <dd>

Inicia um editor e abre o documento para edição. Se *lpFile* não for um arquivo de documento, a função falhará.

</dd> <dt>

<span id="explore"></span><span id="EXPLORE"></span>

<span id="explore"></span><span id="EXPLORE"></span>**apresenta**


</dt> <dd>

Explora a pasta especificada por *lpFile*.

</dd> <dt>

<span id="find"></span><span id="FIND"></span>

<span id="find"></span><span id="FIND"></span>**considerar**


</dt> <dd>

Inicia uma pesquisa a partir do diretório especificado.

</dd> <dt>

<span id="open"></span><span id="OPEN"></span>

<span id="open"></span><span id="OPEN"></span>**abrir**


</dt> <dd>

Abre o arquivo especificado pelo parâmetro *lpFile* . O arquivo pode ser um arquivo executável, um arquivo de documento ou uma pasta.

</dd> <dt>

<span id="print"></span><span id="PRINT"></span>

<span id="print"></span><span id="PRINT"></span>**imprimir**


</dt> <dd>

Imprime o arquivo de documento especificado por *lpFile*. Se *lpFile* não for um arquivo de documento, a função falhará.

</dd> <dt>

<span id="NULL"></span><span id="null"></span>

<span id="NULL"></span><span id="null"></span>**NULO**


</dt> <dd>

para sistemas anteriores à Windows 2000, o verbo padrão será usado se ele for válido e disponível no registro. Caso contrário, o verbo "Open" será usado.

para os sistemas Windows 2000 e posteriores, o verbo padrão é usado, se disponível. Caso contrário, o verbo "Open" será usado. Se nenhum verbo estiver disponível, o sistema usará o primeiro verbo listado no registro.

</dd> </dl> </dd> <dt>

*lpFile* \[ no\]
</dt> <dd>

Tipo: **LPCTSTR**

Um ponteiro para uma cadeia de caracteres terminada em **nulo** que especifica o arquivo ou objeto no qual executar o verbo especificado. Para especificar um objeto de namespace de Shell, passe o nome de análise totalmente qualificado. Observe que nem todos os verbos têm suporte em todos os objetos. Por exemplo, nem todos os tipos de documento dão suporte ao verbo "Print".

</dd> <dt>

*lpParameters* \[ no\]
</dt> <dd>

Tipo: **LPCTSTR**

Se o parâmetro *lpFile* especificar um arquivo executável, *lpParameters* será um ponteiro para uma cadeia de caracteres terminada em **nulo** que especifica os parâmetros a serem passados para o aplicativo. O formato dessa cadeia de caracteres é determinado pelo verbo a ser invocado. Se *lpFile* especificar um arquivo de documento, *LpParameters* deverá ser **nulo**.

</dd> <dt>

*lpDirectory* \[ no\]
</dt> <dd>

Tipo: **LPCTSTR**

Um ponteiro para uma cadeia de caracteres terminada em **nulo** que especifica o diretório padrão.

</dd> <dt>

*nShowCmd* \[ no\]
</dt> <dd>

Tipo: **int**

Os sinalizadores que especificam como um aplicativo deve ser exibido quando ele é aberto. Se *lpFile* especificar um arquivo de documento, o sinalizador será simplesmente passado para o aplicativo associado. Cabe ao aplicativo decidir como tratá-lo. Pode ser qualquer um dos valores que podem ser especificados no parâmetro *nCmdShow* para a função de [janela](/windows/desktop/api/winuser/nf-winuser-showwindow) .

</dd> <dt>

*lpfnCBWinExec* 
</dt> <dd>

Tipo: **void \***

Função de retorno de chamada usada para chamar [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) no kernel de 16 bits.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HINSTANCE**

Retorna um valor maior que 32 se for bem-sucedido ou um valor de erro menor ou igual a 32, caso contrário. A tabela a seguir lista os valores de erro. o valor de retorno é convertido como um HINSTANCE para compatibilidade com versões anteriores com aplicativos de Windows de 16 bits. No entanto, não é um verdadeiro HINSTANCE. A única coisa que pode ser feita com o HINSTANCE retornado é convertê-lo em um **int** e compará-lo com o valor 32 ou um dos códigos de erro abaixo.



| Código de retorno                                                                                             | Descrição                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**0**</dt> </dl>                        | O sistema operacional está sem memória ou recursos.<br/>                                                                                                           |
| <dl> <dt>**arquivo de erro \_ \_ não \_ encontrado**</dt> </dl>  | O arquivo especificado não foi encontrado.<br/>                                                                                                                             |
| <dl> <dt>**caminho de erro \_ \_ não \_ encontrado**</dt> </dl>  | O caminho especificado não foi encontrado.<br/>                                                                                                                             |
| <dl> <dt>**ERRO \_ de \_ formato inadequado**</dt> </dl>       | O arquivo de .exe é inválido (.exe não Win32 ou erro na imagem .exe).<br/>                                                                                             |
| <dl> <dt>**ES \_ ACCESSDENIED de erro \_**</dt> </dl>    | O sistema operacional negou o acesso ao arquivo especificado.<br/>                                                                                                     |
| <dl> <dt>**ES \_ ASSOCINCOMPLETE de erro \_**</dt> </dl> | A associação de nome de arquivo está incompleta ou inválida.<br/>                                                                                                           |
| <dl> <dt>**ES \_ DDEBUSY de erro \_**</dt> </dl>         | A transação DDE não pôde ser concluída porque outras transações DDE estavam sendo processadas.<br/>                                                               |
| <dl> <dt>**ES \_ DDEFAIL de erro \_**</dt> </dl>         | Falha na transação DDE.<br/>                                                                                                                                   |
| <dl> <dt>**ES \_ DDETIMEOUT de erro \_**</dt> </dl>      | A transação DDE não pôde ser concluída porque o tempo limite da solicitação foi atingido.<br/>                                                                                     |
| <dl> <dt>**ES \_ DLLNOTFOUND de erro \_**</dt> </dl>     | A DLL especificada não foi encontrada.<br/>                                                                                                                              |
| <dl> <dt>**ES \_ FNF de erro \_**</dt> </dl>             | O arquivo especificado não foi encontrado.<br/>                                                                                                                             |
| <dl> <dt>**ES \_ ERR \_ NOassoc**</dt> </dl>         | Não há nenhum aplicativo associado à extensão de nome de arquivo fornecida. Esse erro também será retornado se você tentar imprimir um arquivo que não seja imprimível.<br/> |
| <dl> <dt>**ES \_ Oom de erro \_**</dt> </dl>             | Não havia memória suficiente para concluir a operação.<br/>                                                                                                        |
| <dl> <dt>**\_ES ERR \_ PNF**</dt> </dl>             | O caminho especificado não foi encontrado.<br/>                                                                                                                             |
| <dl> <dt>**\_ES ERR \_ SHARE**</dt> </dl>           | Ocorreu uma violação de compartilhamento.<br/>                                                                                                                                 |



 

## <a name="remarks"></a>Comentários

**WOWShellExecute** não está incluído em um arquivo .lib ou de header. Ele é exportado do Shell32.dll por nome.

Esse método permite que você execute comandos no menu de atalho de uma pasta ou armazenados no Registro.

Se *lpOperation* for **NULL,** a função abrirá o arquivo especificado por *lpFile*. Se *lpOperation* for "open" ou "explore", a função tentará abrir ou explorar a pasta.

Para obter informações sobre o aplicativo que é lançado como resultado da chamada **a WOWShellExecute,** use [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).

> [!Note]  
> As **janelas Iniciar pasta em uma configuração de processo** separada em Opções de Pasta afetam **WOWShellExecute**. Se essa opção estiver desabilitada (a configuração padrão), **WOWShellExecute** usará uma janela aberta do Explorer em vez de iniciar uma nova. Se nenhuma janela do Explorer estiver aberta, **WOWShellExecute** iniciará uma nova.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)
</dt> </dl>

 

 
