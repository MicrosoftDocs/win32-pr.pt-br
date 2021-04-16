---
description: Lê dados de um arquivo aberto.
ms.assetid: 7EA2FE38-20DA-43E1-A764-66A81725D1EA
title: Função NtReadFile (WDM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtReadFile
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: be1a73c6451012dfd97d7d4c55c23f0842cf1551
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500831"
---
# <a name="ntreadfile-function"></a>Função NtReadFile

Lê dados de um arquivo aberto.

Essa função é o modo de usuário equivalente à função [**ZwReadFile**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntreadfile) documentada no WDK (Kit de driver do Windows).

## <a name="syntax"></a>Sintaxe


```C++
NTSTATUS NtReadFile(
  _In_     HANDLE           FileHandle,
  _In_opt_ HANDLE           Event,
  _In_opt_ PIO_APC_ROUTINE  ApcRoutine,
  _In_opt_ PVOID            ApcContext,
  _Out_    PIO_STATUS_BLOCK IoStatusBlock,
  _Out_    PVOID            Buffer,
  _In_     ULONG            Length,
  _In_opt_ PLARGE_INTEGER   ByteOffset,
  _In_opt_ PULONG           Key
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Identificador de fileHandle* \[ no\]
</dt> <dd>

Identificador para o objeto de arquivo. Esse identificador é criado por uma chamada bem-sucedida para [**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) ou [**NtOpenFile**](/windows/desktop/api/Winternl/nf-winternl-ntopenfile).

</dd> <dt>

*Evento* \[ de em, opcional\]
</dt> <dd>

Opcionalmente, um identificador para um objeto de evento a ser definido para o estado sinalizado após a operação de leitura ser concluída. Os drivers intermediários e de dispositivo devem definir esse parâmetro como **NULL**.

</dd> <dt>

*ApcRoutine* \[ em, opcional\]
</dt> <dd>

Esse parâmetro é reservado. Os drivers intermediários e de dispositivo devem definir esse ponteiro como **nulo**.

</dd> <dt>

*ApcContext* \[ em, opcional\]
</dt> <dd>

Esse parâmetro é reservado. Os drivers intermediários e de dispositivo devem definir esse ponteiro como **nulo**.

</dd> <dt>

*IoStatusBlock* \[ fora\]
</dt> <dd>

Ponteiro para uma estrutura de [**\_ \_ bloco de status de e/s**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_io_status_block) que recebe o status final de conclusão e informações sobre a operação de leitura solicitada. O membro de **informações** recebe o número de bytes realmente lidos do arquivo.

</dd> <dt>

*Buffer* \[ fora\]
</dt> <dd>

Ponteiro para um buffer alocado pelo chamador que recebe os dados lidos do arquivo.

</dd> <dt>

*Comprimento* \[ no\]
</dt> <dd>

O tamanho, em bytes, do buffer apontado pelo *buffer*.

</dd> <dt>

*ByteOffset* \[ em, opcional\]
</dt> <dd>

Ponteiro para uma variável que especifica o deslocamento de byte inicial no arquivo em que a operação de leitura será iniciada. Se for feita uma tentativa de leitura além do final do arquivo, **NtReadFile** retornará um erro.

Se a chamada para [**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) definir o alerta de e/s SÍNCRONA do arquivo de sinalizadores de *criaçãooptions* \_ ou o \_ \_ arquivo \_ de es síncrona de arquivos não \_ \_ alerta, o Gerenciador de e/s manterá a posição atual do arquivo. Nesse caso, o chamador de **NtReadFile** pode especificar que o deslocamento da posição atual do arquivo seja usado em vez de um valor *ByteOffset* explícito. Essa especificação pode ser feita usando um dos seguintes métodos:

-   Especifique um ponteiro para um **valor \_ inteiro grande** com o membro **HighPart** definido como-1 e o membro **LowPart** definido como o arquivo de valor definido pelo sistema use a posição do \_ ponteiro do \_ arquivo \_ \_ .

-   Passe um ponteiro **NULL** para *ByteOffset*.

O **NtReadFile** atualiza a posição atual do arquivo adicionando o número de bytes lidos quando concluir a operação de leitura, se estiver usando a posição atual do arquivo mantida pelo Gerenciador de e/s.

Mesmo quando o Gerenciador de e/s está mantendo a posição atual do arquivo, o chamador pode redefinir essa posição passando um valor *ByteOffset* explícito para **NtReadFile**. Fazer isso altera automaticamente a posição do arquivo atual para esse valor de *ByteOffset* , executa a operação de leitura e, em seguida, atualiza a posição de acordo com o número de bytes realmente lidos. Essa técnica fornece o serviço de busca e leitura atômica do chamador.

</dd> <dt>

*Chave* \[ em, opcional\]
</dt> <dd>

Os drivers intermediários e de dispositivo devem definir esse ponteiro como **nulo**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

**NtReadFile** retorna o status \_ Success ou o código de erro NTSTATUS apropriado.

## <a name="remarks"></a>Comentários

Os chamadores de **NtReadFile** devem já ter chamado [**NTCREATEFILE**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) com o arquivo de leitura de \_ \_ dados ou o valor de leitura genérico \_ definido no parâmetro *desiredAccess* .

Se a chamada anterior para [**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) definir o sinalizador do arquivo \_ sem \_ \_ buffer intermediário no parâmetro *CreateOptions* como **NtCreateFile**, os parâmetros *Length* e *ByteOffset* para **NtReadFile** devem ser múltiplos do tamanho do setor. Para obter mais informações, consulte **NtCreateFile**.

**NtReadFile** começa a ler da *ByteOffset* especificada ou da posição do arquivo atual para o *buffer* fornecido. Ele encerra a operação de leitura em uma das seguintes condições:

-   O buffer está cheio porque o número de bytes especificado pelo parâmetro de *comprimento* foi lido. Portanto, não é possível colocar mais dados no buffer sem um estouro.

-   O fim do arquivo é atingido durante a operação de leitura, portanto, não há mais dados no arquivo a serem transferidos para o buffer.

Se o chamador abrir o arquivo com o sinalizador SYNCHRONIZE definido em *desiredAccess*, o thread de chamada poderá sincronizar com a conclusão da operação de leitura aguardando o identificador do arquivo, *fileHandle*. O identificador é sinalizado cada vez que uma operação de e/s emitida no identificador é concluída. No entanto, o chamador não deve aguardar um identificador que foi aberto para acesso a arquivos síncronos (alerta de e/s de arquivo \_ síncrono de \_ es \_ \_ \_ \_ ). Nesse caso, **NtReadFile** aguarda em nome do chamador e não retorna até que a operação de leitura seja concluída. O chamador pode aguardar com segurança o identificador do arquivo somente se todas as três condições a seguir forem atendidas:

-   O identificador foi aberto para acesso assíncrono (ou seja, nenhum \_ sinalizador de \_ e/s SÍNCRONA de arquivo \_  foi especificado).

-   O identificador está sendo usado apenas para uma operação de e/s por vez.

-   **NtReadFile** retornou o status \_ pendente.

Um driver deve chamar **NtReadFile** no contexto do processo do sistema se qualquer uma das seguintes condições existir:

-   O driver criou o identificador de arquivo que ele passa para **NtReadFile**.

-   O **NtReadFile** notificará o driver de conclusão de e/s por meio de um evento criado pelo driver.

-   O **NtReadFile** notificará o driver de conclusão de e/s por meio de uma rotina de retorno de chamada da APC que o driver passa para **NtReadFile**.

Os identificadores de arquivo e de evento são válidos somente no contexto do processo em que os identificadores são criados. Portanto, para evitar brechas de segurança, o driver deve criar qualquer identificador de arquivo ou evento que ele passe para **NtReadFile** no contexto do processo do sistema, em vez do contexto do processo em que o driver está.

Da mesma forma, **NtReadFile** deve ser chamado no contexto do processo do sistema, caso ele notifique o driver de conclusão de e/s por meio de uma APC, porque o APCs sempre é acionado no contexto do thread que emite a solicitação de e/s. Se o driver chamar **NtReadFile** no contexto de um processo diferente do sistema um, a APC poderá ser atrasada indefinidamente ou pode não ser acionada.

Para obter mais informações sobre como trabalhar com arquivos, consulte [usando arquivos em um driver](/windows-hardware/drivers/kernel/using-files-in-a-driver).

Os chamadores de **NtReadFile** devem estar em execução em IRQL = \_ nível passivo e com o [kernel APCs especial habilitado](/windows-hardware/drivers/kernel/disabling-apcs).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                                                    |
| Plataforma de destino<br/>          | <dl> <dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt> </dl> |
| parâmetro<br/>                   | <dl> <dt>WDM. h (incluindo WDM. h, Ntddk. h ou Ntifs. h)</dt> </dl>                   |
| Biblioteca<br/>                  | <dl> <dt>Ntdll. lib</dt> </dl>                                                    |
| DLL<br/>                      | <dl> <dt>Ntdll.dll (modo de usuário)</dt> </dl>                                        |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**KeInitializeEvent**](/windows-hardware/drivers/ddi/wdm/nf-wdm-keinitializeevent)
</dt> <dt>

[**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile)
</dt> <dt>

[**NtQueryInformationFile**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntqueryinformationfile)
</dt> <dt>

[**NtSetInformationFile**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntsetinformationfile)
</dt> <dt>

[**NtWriteFile**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntwritefile)
</dt> </dl>

 

 
