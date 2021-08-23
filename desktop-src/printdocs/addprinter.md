---
description: A função AddPrinter adiciona uma impressora à lista de impressoras com suporte para um servidor especificado.
ms.assetid: ffc4fee8-46c6-47ad-803d-623bf8efdefd
title: Função AddPrinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinter
- AddPrinterA
- AddPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 6034c330da19f5982e9bbacbf75cc16f0a7d10dd65f9c8bded2efa5cbda70835
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119601136"
---
# <a name="addprinter-function"></a>Função AddPrinter

A função **AddPrinter** adiciona uma impressora à lista de impressoras com suporte para um servidor especificado.

## <a name="syntax"></a>Sintaxe


```C++
HANDLE AddPrinter(
  _In_ LPTSTR *pName,
  _In_ DWORD  Level,
  _In_ LPBYTE pPrinter
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pname* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do servidor no qual a impressora deve ser instalada. Se essa cadeia de caracteres for **nula**, a impressora será instalada localmente.

</dd> <dt>

*Nível* \[ do no\]
</dt> <dd>

A versão da estrutura à qual o *pPrinter* aponta. Esse valor deve ser 2.

</dd> <dt>

*pPrinter* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura de [**informações da impressora \_ \_ 2**](printer-info-2.md) que contém informações sobre a impressora. Você deve especificar valores não **nulos** para os membros **pPrinterName**, **pPortName**, **pDriverName** e **pPrintProcessor** dessa estrutura antes de chamar **AddPrinter**.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for realizada com sucesso, o valor de retorno será um identificador (não seguro para thread) para um novo objeto de impressora. Quando você terminar com o identificador, passe-o para a função [**ClosePrinter**](closeprinter.md) para fechá-lo.

Se a função falhar, o valor de retorno será **nulo**.

## <a name="remarks"></a>Comentários

Não chame esse método em [**DllMain**](/windows/desktop/Dlls/dllmain).

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

O chamador deve ter o [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).

O identificador retornado não é thread-safe. Se os chamadores precisarem usá-lo simultaneamente em vários threads, eles deverão fornecer acesso de sincronização personalizado ao identificador da impressora usando as [funções de sincronização](/windows/desktop/Sync/synchronization-functions). Para evitar escrever código personalizado, o aplicativo pode abrir um identificador de impressora em cada thread, conforme necessário.

A seguir estão os membros da estrutura [**\_ info \_ 2 da impressora**](printer-info-2.md) que podem ser definidos antes que a função **AddPrinter** seja chamada:

-   **Atributos**
-   **pPrintProcessor**
-   **Defaultanteriority**
-   **Prioridade**
-   **pComment**
-   **pSecurityDescriptor**
-   **pDatatype**
-   **pSepFile**
-   **pDevMode**
-   **pShareName**
-   **pLocation**
-   **StartTime**
-   **pParameters**
-   **UntilTime**

Os membros **status**, **cJobs** e **AveragePPM** da estrutura [**informações da \_ impressora \_ 2**](printer-info-2.md) são reservados para uso pela função [**getprinter**](getprinter.md) . Eles não devem ser definidos antes de chamar **AddPrinter**.

Se **pSecurityDescriptor** for **NULL**, o sistema atribuirá um descritor de segurança padrão à impressora. O descritor de segurança padrão tem as seguintes permissões.



| Valor                          | Descrição                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Administradores e Usuários Avançados | Controle total na fila de impressão. Isso significa que os membros desses grupos podem imprimir, gerenciar a fila (pode excluir a fila, alterar qualquer configuração da fila, incluindo o descritor de segurança) e gerenciar os trabalhos de impressão de todos os usuários (excluir, pausar, retomar e reiniciar trabalhos). observe que os usuários avançados não existem antes de Windows XP Professional.<br/> |
| Criador/Proprietário                  | Pode gerenciar trabalhos próprios. Isso significa que o usuário que envia trabalhos pode gerenciar (excluir, pausar, retomar, reiniciar) seus próprios trabalhos.                                                                                                                                                                                                                                  |
| Todos                       | Execute e controle de leitura padrão. Isso significa que os membros do grupo Everyone podem imprimir e ler as propriedades da fila de impressão.                                                                                                                                                                                                                     |



 

Depois que um aplicativo cria um objeto de impressora com a função **AddPrinter** , ele deve usar a função [**printerproperties**](printerproperties.md) para especificar as configurações corretas para o driver de impressora associado ao objeto de impressora.

A função **AddPrinter** retornará um erro se um objeto de impressora com o mesmo nome já existir, a menos que esse objeto esteja marcado como exclusão pendente. Nesse caso, a impressora existente não é excluída, e os parâmetros de criação **Addimprimíer** são usados para alterar as configurações de impressora existentes (como se o aplicativo tivesse usado a função [**setprintr**](setprinter.md) ).

Use a função [**EnumPrintProcessors**](enumprintprocessors.md) para enumerar o conjunto de processadores de impressão instalados em um servidor. Use a função [**EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md) para enumerar o conjunto de tipos de dados que um processador de impressão suporta. Use a função [**EnumPorts**](enumports.md) para enumerar o conjunto de portas disponíveis. Use a função [**EnumPrinterDrivers**](enumprinterdrivers.md) para enumerar os drivers de impressora instalados.

O chamador da função **AddPrinter** deve ter acesso \_ ao servidor \_ administrar o acesso ao servidor no qual a impressora será criada. O identificador retornado pela função terá toda a permissão de acesso à impressora \_ \_ e poderá ser usado para executar operações administrativas na impressora.

Se a função **DrvPrinterEvent** for passada, o sinalizador de evento de impressora \_ \_ \_ sem sinalizador de interface do \_ usuário não deverá usar uma chamada de interface do usuário durante o **DrvPrinterEvent**. Para fazer trabalhos relacionados à interface do usuário, o instalador deve usar a entrada **VendorSetup** no arquivo. inf da impressora ou, para dispositivos plug and Play, o instalador pode usar um coinstalador específico do dispositivo. para obter mais informações sobre o **VendorSetup**, consulte o Microsoft Windows Driver Development Kit (DDK).

O firewall de conexão com a Internet (ICF) bloqueia as portas de impressora por padrão, mas uma exceção para o compartilhamento de arquivos e impressoras é habilitada quando você executa o **AddPrinter**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nomes Unicode e ANSI<br/>   | **AddPrinterW** (Unicode) e **addprintera** (ANSI)<br/>                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**ClosePrinter**](closeprinter.md)
</dt> <dt>

[**DeletePrinter**](deleteprinter.md)
</dt> <dt>

[**EnumPorts**](enumports.md)
</dt> <dt>

[**EnumPrinterDrivers**](enumprinterdrivers.md)
</dt> <dt>

[**EnumPrintProcessors**](enumprintprocessors.md)
</dt> <dt>

[**EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md)
</dt> <dt>

[**Getprinter**](getprinter.md)
</dt> <dt>

[**Informações da impressora \_ \_ 2**](printer-info-2.md)
</dt> <dt>

[**Impressoras**](printerproperties.md)
</dt> <dt>

[**Setprinter**](setprinter.md)
</dt> </dl>

 

