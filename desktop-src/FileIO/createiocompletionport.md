---
description: Cria uma porta de conclusão de entrada/saída (e/s) e a associa a um identificador de arquivo especificado ou cria uma porta de conclusão de e/s que ainda não está associada a um identificador de arquivo, permitindo a associação em um momento posterior.
ms.assetid: 40cb47fc-7b15-47f6-bee2-2611d4686053
title: Função CreateIoCompletionPort (IoAPI. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateIoCompletionPort
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-0.dll
- KernelBase.dll
- MinKernelBase.dll
- API-MS-Win-Core-io-l1-1-1.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: 6612c3087841aa0c13f131581f8a05c29403e4fccf81bd6f0dc338b1dd9e42a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083156"
---
# <a name="createiocompletionport-function"></a>Função CreateIoCompletionPort

Cria uma porta de conclusão de entrada/saída (e/s) e a associa a um identificador de arquivo especificado ou cria uma porta de conclusão de e/s que ainda não está associada a um identificador de arquivo, permitindo a associação em um momento posterior.

A associação de uma instância de um identificador de arquivo aberto a uma porta de conclusão de e/s permite que um processo receba notificações sobre a conclusão de operações de e/s assíncronas envolvendo esse identificador de arquivo.

> [!Note]
>
> O termo *identificador de arquivo* conforme usado aqui refere-se a uma abstração de sistema que representa um ponto de extremidade de e/s sobreposto, não apenas um arquivo no disco. Todos os objetos do sistema que dão suporte a e/s sobreposta, como pontos de extremidade de rede, soquetes TCP, pipes nomeados e slots de email, podem ser usados como identificadores de arquivo. Para obter informações adicionais, consulte a seção comentários.

 

## <a name="syntax"></a>Sintaxe


```C++
HANDLE WINAPI CreateIoCompletionPort(
  _In_     HANDLE    FileHandle,
  _In_opt_ HANDLE    ExistingCompletionPort,
  _In_     ULONG_PTR CompletionKey,
  _In_     DWORD     NumberOfConcurrentThreads
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Identificador de fileHandle* \[ no\]
</dt> <dd>

Um identificador de arquivo aberto ou um **\_ \_ valor de identificador inválido**.

O identificador deve ser para um objeto que dá suporte a e/s sobreposta.

Se um identificador for fornecido, ele precisará ter sido aberto para a conclusão de e/s sobreposta. Por exemplo, você deve especificar o **sinalizador \_ \_ sobreposto do sinalizador de arquivo** ao usar a função [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) para obter o identificador.

Se **o \_ \_ valor de identificador inválido** for especificado, a função criará uma porta de conclusão de e/s sem associá-la a um identificador de arquivo. Nesse caso, o parâmetro *ExistingCompletionPort* deve ser **nulo** e o parâmetro *CompletionKey* é ignorado.

</dd> <dt>

*ExistingCompletionPort* \[ em, opcional\]
</dt> <dd>

Um identificador para uma porta de conclusão de e/s existente ou **nulo**.

Se esse parâmetro especificar uma porta de conclusão de e/s existente, a função a associará ao identificador especificado pelo parâmetro *fileHandle* . A função retorna o identificador da porta de conclusão de e/s existente, se for bem-sucedida; Ele não cria uma nova porta de conclusão de e/s.

Se esse parâmetro for **nulo**, a função criará uma nova porta de conclusão de e/s e, se o parâmetro *fileHandle* for válido, o associará à nova porta de conclusão de e/s. Caso contrário, não ocorrerá nenhuma associação de identificador de arquivo. A função retornará o identificador para a nova porta de conclusão de e/s se for bem-sucedida.

</dd> <dt>

*CompletionKey* \[ no\]
</dt> <dd>

A chave de conclusão por identificador definida pelo usuário que é incluída em cada pacote de conclusão de e/s para o identificador de arquivo especificado. Para obter mais informações, consulte a seção Comentários.

</dd> <dt>

*NumberOfConcurrentThreads* \[ no\]
</dt> <dd>

O número máximo de threads que o sistema operacional pode permitir para processar simultaneamente os pacotes de conclusão de e/s para a porta de conclusão de e/s. Esse parâmetro será ignorado se o parâmetro *ExistingCompletionPort* não for **nulo**.

Se esse parâmetro for zero, o sistema permitirá o máximo de threads em execução simultaneamente, pois há processadores no sistema.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for realizada com sucesso, o valor de retorno será o identificador para uma porta de conclusão de e/s:

-   Se o parâmetro *ExistingCompletionPort* era **nulo**, o valor de retorno será um novo identificador.

-   Se o parâmetro *ExistingCompletionPort* era um identificador de porta de conclusão de e/s válido, o valor de retorno é o mesmo identificador.

-   Se o parâmetro *fileHandle* era um identificador válido, esse identificador de arquivo agora está associado à porta de conclusão de e/s retornada.

Se a função falhar, o valor de retorno será **nulo**. Para obter informações de erro estendidas, chame a função [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

## <a name="remarks"></a>Comentários

O sistema de e/s pode ser instruído a enviar pacotes de notificação de conclusão de e/s para portas de conclusão de e/s, onde eles são enfileirados. A função **CreateIoCompletionPort** fornece essa funcionalidade.

Uma porta de conclusão de e/s e seu identificador estão associados ao processo que a criou e não podem ser compartilhadas entre os processos. No entanto, um único identificador é compartilhável entre threads no mesmo processo.

**CreateIoCompletionPort** pode ser usado em três modos distintos:

-   Crie apenas uma porta de conclusão de e/s sem associá-la a um identificador de arquivo.
-   Associe uma porta de conclusão de e/s existente a um identificador de arquivo.
-   Execute a criação e a associação em uma única chamada.

Para criar uma porta de conclusão de e/s sem associá-la, defina o parâmetro *fileHandle* como **\_ \_ valor de identificador inválido**, o parâmetro *ExistingCompletionPort* como **NULL** e o parâmetro *CompletionKey* como zero (que é ignorado nesse caso). Defina o parâmetro *NumberOfConcurrentThreads* para o valor de simultaneidade desejado para a nova porta de conclusão de e/s ou zero para o padrão (o número de processadores no sistema).

O identificador passado no parâmetro *fileHandle* pode ser qualquer identificador que ofereça suporte a e/s sobreposta. Normalmente, trata-se de um identificador aberto pela função [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) usando o **sinalizador \_ \_ sobreposto do sinalizador de arquivo** (por exemplo, arquivos, slots de email e Pipes). Os objetos criados por outras funções, como [**soquete**](/windows/desktop/api/winsock2/nf-winsock2-socket) , também podem ser associados a uma porta de conclusão de e/s. Para obter um exemplo usando soquetes, consulte [**AcceptEx**](/windows/desktop/api/mswsock/nf-mswsock-acceptex). Um identificador pode ser associado a apenas uma porta de conclusão de e/s e, depois que a associação é feita, o identificador permanece associado a essa porta de conclusão de e/s até que seja fechado.

Para obter mais informações sobre a teoria, uso e funções associadas da porta de conclusão de e/s, consulte [portas de conclusão de e/s](i-o-completion-ports.md).

Vários identificadores de arquivo podem ser associados a uma única porta de conclusão de e/s chamando **CreateIoCompletionPort** várias vezes com o mesmo identificador de porta de conclusão de e/s no parâmetro *ExistingCompletionPort* e um identificador de arquivo diferente no parâmetro *fileHandle* a cada vez.

Use o parâmetro *CompletionKey* para ajudar o aplicativo a controlar quais operações de e/s foram concluídas. Esse valor não é usado pelo **CreateIoCompletionPort** para controle funcional; em vez disso, ele é anexado ao identificador de arquivo especificado no parâmetro *fileHandle* no momento da associação com uma porta de conclusão de e/s. Essa chave de conclusão deve ser exclusiva para cada identificador de arquivo e acompanha o identificador de arquivo em todo o processo de enfileiramento de conclusão interno. Ele é retornado na chamada de função [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) quando um pacote de conclusão chega. O parâmetro *CompletionKey* também é usado pela função [**PostQueuedCompletionStatus**](postqueuedcompletionstatus.md) para enfileirar seus próprios pacotes de conclusão de finalidade especial.

Depois que uma instância de um identificador aberto está associada a uma porta de conclusão de e/s, ela não pode ser usada na função [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) ou [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) porque essas funções têm seus próprios mecanismos de e/s assíncronos.

É melhor não compartilhar um identificador de arquivo associado a uma porta de conclusão de e/s usando a herança de identificador ou uma chamada para a função [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) . As operações executadas com esses identificadores duplicados geram notificações de conclusão. É recomendável considerar atentamente.

O identificador de porta de conclusão de e/s e todos os identificadores de arquivo associados a essa porta de conclusão de e/s específica são conhecidos como *referências à porta de conclusão de e/s*. A porta de conclusão de e/s é liberada quando não há mais referências a ela. Portanto, todos esses identificadores devem ser fechados corretamente para liberar a porta de conclusão de e/s e seus recursos de sistema associados. Depois que essas condições forem satisfeitas, feche o identificador da porta de conclusão de e/s chamando a função [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) .

em Windows 8 e Windows Server 2012, essa função é suportada pelas seguintes tecnologias.



| Tecnologia                                           | Com suporte      |
|------------------------------------------------------|----------------|
| Protocolo SMB (Server Message Block) 3,0<br/>   | Sim<br/> |
| Failover transparente SMB 3,0 (TFO)<br/>        | Sim<br/> |
| SMB 3,0 com compartilhamentos de arquivos de escalabilidade horizontal (SO)<br/>   | Sim<br/> |
| Sistema de arquivos Volume Compartilhado Clusterizado (CsvFS)<br/> | Sim<br/> |
| ReFS (Sistema de Arquivos Resiliente)<br/>              | Sim<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Aplicativos de aplicativos de desktop do XP \[ \| UWP\]<br/>                                                                                                                                                                                                                                                       |
| Servidor mínimo com suporte<br/> | Windows \[Aplicativos da área de trabalho do servidor 2003 \| aplicativo UWP\]<br/>                                                                                                                                                                                                                                              |
| Cabeçalho<br/>                   | <dl> <dt>IoAPI. h (incluir Windows. h);</dt> <dt>WinBase. h no Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 e Windows XP (inclua o Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl>                                                                                                                                                                                                                  |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>                                                                                                                                                                                                                  |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Tópicos de visão geral**
</dt> <dt>

[Funções de gerenciamento de arquivos](file-management-functions.md)
</dt> <dt>

[Portas de conclusão de e/s](i-o-completion-ports.md)
</dt> <dt>

[usando os cabeçalhos de Windows](/windows/desktop/WinProg/using-the-windows-headers)
</dt> <dt>

[Windows Soquetes 2](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

**Funções**
</dt> <dt>

[**AcceptEx**](/windows/desktop/api/mswsock/nf-mswsock-acceptex)
</dt> <dt>

[**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[**Duplicatehandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle)
</dt> <dt>

[**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)
</dt> <dt>

[**GetQueuedCompletionStatusEx**](getqueuedcompletionstatusex-func.md)
</dt> <dt>

[**PostQueuedCompletionStatus**](postqueuedcompletionstatus.md)
</dt> <dt>

[**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex)
</dt> <dt>

[**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex)
</dt> </dl>

 

