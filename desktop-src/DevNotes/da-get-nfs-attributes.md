---
description: O \_ código de controle da obtenção de atributos do \_ NFS \_ consulta informações adicionais sobre um compartilhamento NFS.
ms.assetid: BC9E0E19-7D78-4AE7-A3E6-9FD9212B2B83
title: DA_GET_NFS_ATTRIBUTES código de controle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DA_GET_NFS_ATTRIBUTES
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4427dd48190bd12f7837c4841a98e15f7ddaff5f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500880"
---
# <a name="da_get_nfs_attributes-control-code"></a>\_Código de controle da obtenção de \_ \_ atributos NFS

O código de controle da **\_ obtenção de \_ \_ atributos do NFS** consulta informações adicionais sobre um compartilhamento NFS.

Para executar essa operação, chame a função [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) com os parâmetros a seguir.


```C++
BOOL 
   WINAPI 
   DeviceIoControl( (HANDLE)       hDevice,               // handle to device
                    (DWORD)        DA_GET_NFS_ATTRIBUTES, // dwIoControlCode
                                   NULL,                  // lpInBuffer
                                   0,                     // nInBufferSize
                    (LPDWORD)      lpOutBuffer,           // output buffer
                    (DWORD)        nOutBufferSize,        // size of output buffer
                    (LPDWORD)      lpBytesReturned,       // number of bytes returned
                    (LPOVERLAPPED) lpOverlapped );        // OVERLAPPED structure
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDevice* \[ no\]
</dt> <dd>

Um identificador para um arquivo no compartilhamento NFS. Para obter esse identificador, chame a função [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) .

</dd> <dt>

*dwIoControlCode* \[ no\]
</dt> <dd>

O código de controle para a operação. Use **\_ \_ \_ atributos de obter NFS** para esta operação.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Não usado com esta operação; Defina como **nulo**.

</dd> <dt>

*nInBufferSize* \[ no\]
</dt> <dd>

Não usado com esta operação; definido como zero.

</dd> <dt>

*lpOutBuffer* \[ fora\]
</dt> <dd>

Um ponteiro para o buffer de saída, que contém uma estrutura de **\_ \_ atributos de arquivo NFS** . Para obter mais informações, consulte a seção Comentários.

</dd> <dt>

*nOutBufferSize* \[ no\]
</dt> <dd>

O tamanho do buffer de saída em bytes.

</dd> <dt>

*lpBytesReturned* \[ fora\]
</dt> <dd>

Um ponteiro para uma variável que recebe o tamanho dos dados armazenados no buffer de saída, em bytes.

Se o buffer de saída for muito pequeno, a chamada falhará, [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará um **erro de \_ \_ buffer insuficiente** e *lpBytesReturned* será zero.

Se *lpOverlapped* for **nulo**, *lpBytesReturned* não poderá ser **nulo**. Mesmo quando uma operação não retorna dados de saída e *lpOutBuffer* é **nula**, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) faz uso de *lpBytesReturned*. Após tal operação, o valor de *lpBytesReturned* é inútil.

Se *lpOverlapped* não for **nulo**, *lpBytesReturned* poderá ser **nulo**. Se esse parâmetro não for **nulo** e a operação retornar dados, *lpBytesReturned* será inútil até que a operação sobreposta seja concluída. Para recuperar o número de bytes retornados, chame [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult). Se o parâmetro *hDevice* estiver associado a uma porta de conclusão de e/s, você poderá recuperar o número de bytes retornados chamando [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus).

</dd> <dt>

*lpOverlapped* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura [**sobreposta**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) .

Se *hDevice* tiver sido aberto sem especificar o **sinalizador de arquivo \_ \_ sobreposto**, *lpOverlapped* será ignorado.

Se *hDevice* tiver sido aberto com o sinalizador de **sinalizador de arquivo \_ \_ sobreposto** , a operação será executada como uma operação sobreposta (assíncrona). Nesse caso, *lpOverlapped* deve apontar para uma estrutura [**sobreposta**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) válida que contém um identificador para um objeto de evento. Caso contrário, a função falhará de maneiras imprevisíveis.

Para operações sobrepostas, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) retorna imediatamente e o objeto de evento é sinalizado quando a operação é concluída. Caso contrário, a função não retorna até que a operação seja concluída ou um erro ocorra.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a operação for concluída com êxito, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) retornará um valor diferente de zero.

Se a operação falhar ou estiver pendente, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) retornará zero. Para obter informações de erro estendidas, chame [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentários

Este código de controle não tem nenhum arquivo de cabeçalho associado. Você deve definir o código de controle e as estruturas de dados da seguinte maneira.

``` syntax
#define DEVICE_DA_RDR 0x80000  
 
#define DA_GET_NFS_ATTRIBUTES CTL_CODE(DEVICE_DA_RDR, 0x804, METHOD_BUFFERED, FILE_ANY_ACCESS)

typedef struct _NFS_SPEC_DATA {  
    ULONG               SpecData1;
    ULONG               SpecData2;
} NFS_SPEC_DATA, *PNFS_SPEC_DATA;

typedef struct _NFS_TIME {
    ULONG        Seconds;
    ULONG        nSeconds;
} NFS_TIME, *PNFS_TIME;

#define NFS_TYPE_REG         1
#define NFS_TYPE_DIR         2
#define NFS_TYPE_BLK         3
#define NFS_TYPE_CHR         4
#define NFS_TYPE_LNK         5
#define NFS_TYPE_SOCK        6
#define NFS_TYPE_FIFO        7

typedef struct _NFS_FILE_ATTRIBUTES {  
    ULONG               FileType;  
    ULONG               Mode;  
    ULONG               NLink;  
    ULONG               Uid;  
    ULONG               Gid;  
    ULONGLONG           Size;  
    ULONGLONG           Used;
    NFS_SPEC_DATA       Rdev;
    ULONGLONG           Fsid;  
    ULONGLONG           FileId;  
    NFS_TIME            AccessTime;  
    NFS_TIME            ModifyTime;  
    NFS_TIME            ChangeTime;  
} NFS_FILE_ATTRIBUTES, *PNFS_FILE_ATTRIBUTES;

typedef struct _DA_FILE_ATTRIBUTES {  
    NFS_FILE_ATTRIBUTES FileAttributes;  
    ULONG               Version;  
} DA_FILE_ATTRIBUTES, *PDA_FILE_ATTRIBUTES;
```

Os membros da estrutura podem ser descritos da seguinte maneira.

<dl> <dt>

<span id="SpecData1"></span><span id="specdata1"></span><span id="SPECDATA1"></span>**SpecData1**
</dt> <dd>

Um valor opaco que é usado para tipos de arquivo especiais, como arquivos de bloco especial, caracteres especiais e FIFO.

</dd> <dt>

<span id="SpecData2"></span><span id="specdata2"></span><span id="SPECDATA2"></span>**SpecData2**
</dt> <dd>

Um valor opaco que é usado para tipos de arquivo especiais, como arquivos de bloco especial, caracteres especiais e FIFO.

</dd> <dt>

<span id="Seconds"></span><span id="seconds"></span><span id="SECONDS"></span>**Seg**
</dt> <dd>

Um valor de 64 bits que representa os segundos desde 1º de janeiro de 1970 (UTC).

</dd> <dt>

<span id="nSeconds"></span><span id="nseconds"></span><span id="NSECONDS"></span>**nSeconds**
</dt> <dd>

O número de nanossegundos a ser adicionado ao membro de **segundos** .

</dd> <dt>

<span id="FileType"></span><span id="filetype"></span><span id="FILETYPE"></span>**Talvez**
</dt> <dd>

O tipo de arquivo NFS do compartilhamento.



| Tipo de arquivo NFS                                                                              | Descrição                          |
|--------------------------------------------------------------------------------------------|--------------------------------------|
| <span id="NFS_TYPE_REG"></span><span id="nfs_type_reg"></span>tipo de NFS \_ \_ reg<br/>    | Um arquivo regular.<br/>           |
| <span id="NFS_TYPE_DIR"></span><span id="nfs_type_dir"></span>Dir. de \_ tipo NFS \_<br/>    | Um diretório.<br/>              |
| <span id="NFS_TYPE_BLK"></span><span id="nfs_type_blk"></span>tipo de NFS \_ \_ BLK<br/>    | Um arquivo especial de bloco.<br/>     |
| <span id="NFS_TYPE_CHR"></span><span id="nfs_type_chr"></span>tipo de NFS \_ \_ Chr<br/>    | Um arquivo de caractere especial.<br/> |
| <span id="NFS_TYPE_LNK"></span><span id="nfs_type_lnk"></span>tipo de NFS \_ \_ lnk<br/>    | Um link simbólico.<br/>          |
| <span id="NFS_TYPE_SOCK"></span><span id="nfs_type_sock"></span>tipo de NFS \_ \_ Sock<br/> | Um soquete do Windows.<br/>         |
| <span id="NFS_TYPE_FIFO"></span><span id="nfs_type_fifo"></span>tipo de NFS \_ \_ FIFO<br/> | Um arquivo FIFO.<br/>              |



 

</dd> <dt>

<span id="Mode"></span><span id="mode"></span><span id="MODE"></span>**Moda**
</dt> <dd>

O modo de arquivo.

</dd> <dt>

<span id="NLink"></span><span id="nlink"></span><span id="NLINK"></span>**NLink**
</dt> <dd>

O número de links para o compartilhamento.

</dd> <dt>

<span id="Uid"></span><span id="uid"></span><span id="UID"></span>**UID**
</dt> <dd>

O UID (identificador de usuário do UNIX).

</dd> <dt>

<span id="Gid"></span><span id="gid"></span><span id="GID"></span>**GID**
</dt> <dd>

O GID (identificador de grupo do UNIX).

</dd> <dt>

<span id="Size"></span><span id="size"></span><span id="SIZE"></span>**Tamanho**
</dt> <dd>

O tamanho do arquivo, em bytes.

</dd> <dt>

<span id="Used"></span><span id="used"></span><span id="USED"></span>**Utiliza**
</dt> <dd>

O tamanho do arquivo usado, em bytes. Isso é o mesmo que o tamanho do arquivo.

</dd> <dt>

<span id="Rdev"></span><span id="rdev"></span><span id="RDEV"></span>**Rdev**
</dt> <dd>

O identificador do dispositivo.

</dd> <dt>

<span id="Fsid"></span><span id="fsid"></span><span id="FSID"></span>**Fsid**
</dt> <dd>

O identificador do sistema de arquivos.

</dd> <dt>

<span id="FileId"></span><span id="fileid"></span><span id="FILEID"></span>**FileId**
</dt> <dd>

O identificador de arquivo.

</dd> <dt>

<span id="AccessTime"></span><span id="accesstime"></span><span id="ACCESSTIME"></span>**Acesso ao**
</dt> <dd>

A hora do último acesso.

</dd> <dt>

<span id="ModifyTime"></span><span id="modifytime"></span><span id="MODIFYTIME"></span>**Modificartime**
</dt> <dd>

A hora da última modificação.

</dd> <dt>

<span id="ChangeTime"></span><span id="changetime"></span><span id="CHANGETIME"></span>**Changetime**
</dt> <dd>

A hora da última alteração.

</dd> <dt>

<span id="FileAttributes"></span><span id="fileattributes"></span><span id="FILEATTRIBUTES"></span>**FileAttributes**
</dt> <dd>

Uma estrutura de **\_ \_ atributos de arquivo NFS** .

> [!Note]  
> Para obter descrições mais detalhadas dos membros dessa estrutura, consulte a estrutura **fattr3** na especificação do protocolo NFS versão 3 (conforme definido em [RFC 1813](https://www.ietf.org/rfc/rfc1813.txt)).

 

</dd> <dt>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Versão**
</dt> <dd>

Especifica se a conexão na qual o identificador para o compartilhamento NFS foi criado é sobre o NFS versão 2 ou o protocolo NFS versão 3.



| Valor                            | Descrição              |
|----------------------------------|--------------------------|
| <span id="2"></span>2<br/> | NFS versão 2<br/> |
| <span id="3"></span>Beta<br/> | NFS versão 3<br/> |



 

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>         |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>    |
| Fim do suporte do cliente<br/>    | Nenhum compatível<br/>         |
| Fim do suporte do servidor<br/>    | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> </dl>

 

 
