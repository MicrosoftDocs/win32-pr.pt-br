---
description: O código \_ de controle DA GET \_ NFS \_ ATTRIBUTES consulta informações adicionais sobre um compartilhamento NFS.
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
ms.openlocfilehash: e3e2b974d58888c35c24e18f16e1e75da46a180bb8123e9745170e074cd448de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956105"
---
# <a name="da_get_nfs_attributes-control-code"></a>Código \_ de controle DE ATRIBUTOS GET \_ NFS \_

O **código de controle DA GET \_ \_ NFS \_ ATTRIBUTES** consulta informações adicionais sobre um compartilhamento NFS.

Para executar essa operação, chame a [**função DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) com os parâmetros a seguir.


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

*hDevice* \[ Em\]
</dt> <dd>

Um handle para um arquivo no compartilhamento NFS. Para obter esse handle, chame a [**função CreateFile.**](/windows/win32/api/fileapi/nf-fileapi-createfilea)

</dd> <dt>

*dwIoControlCode* \[ Em\]
</dt> <dd>

O código de controle para a operação. Use **ATRIBUTOS \_ GET \_ NFS \_ da DA** para esta operação.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Não usado com essa operação; definido como **NULL.**

</dd> <dt>

*nInBufferSize* \[ Em\]
</dt> <dd>

Não usado com essa operação; definido como zero.

</dd> <dt>

*lpOutBuffer* \[ out\]
</dt> <dd>

Um ponteiro para o buffer de saída, que contém uma estrutura **NFS \_ FILE \_ ATTRIBUTES.** Para obter mais informações, consulte a seção Comentários.

</dd> <dt>

*nOutBufferSize* \[ Em\]
</dt> <dd>

O tamanho do buffer de saída em bytes.

</dd> <dt>

*lpBytesReturned* \[ out\]
</dt> <dd>

Um ponteiro para uma variável que recebe o tamanho dos dados armazenados no buffer de saída, em bytes.

Se o buffer de saída for muito pequeno, a chamada falhará, [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) **retornará ERROR \_ INSUFFICIENT \_ BUFFER** e *lpBytesReturned* será zero.

Se *lpOverlapped for* **NULL,** *lpBytesReturned* não poderá ser **NULL.** Mesmo quando uma operação não retorna dados de saída e *lpOutBuffer* é **NULL,** [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) usa *lpBytesReturned*. Após essa operação, o valor de *lpBytesReturned* não tem sentido.

Se *lpOverlapped não* for **NULL,** *lpBytesReturned* poderá ser **NULL.** Se esse parâmetro não for **NULL e** a operação retornar dados, *lpBytesReturned* não terá sentido até que a operação sobrecarregada seja concluída. Para recuperar o número de bytes retornados, chame [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult). Se o *parâmetro hDevice* estiver associado a uma porta de conclusão de E/S, você poderá recuperar o número de bytes retornados chamando [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus).

</dd> <dt>

*lpOverlapped* \[ Em\]
</dt> <dd>

Um ponteiro para uma [**estrutura OVERLAPPED.**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped)

Se *hDevice* foi aberto sem especificar **FILE FLAG \_ \_ OVERLAPPED,** *lpOverlapped* será ignorado.

Se *hDevice* tiver sido aberto com o sinalizador **FILE FLAG \_ \_ OVERLAPPED,** a operação será executada como uma operação sobressalo (assíncrona). Nesse caso, *lpOverlapped* deve apontar para uma estrutura [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) válida que contém um identificador para um objeto de evento. Caso contrário, a função falhará de maneiras imprevisíveis.

Para operações sobreporadas, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) retorna imediatamente e o objeto de evento é sinalizado quando a operação é concluída. Caso contrário, a função não retornará até que a operação seja concluída ou ocorra um erro.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a operação for concluída com êxito, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) retornará um valor diferente de zero.

Se a operação falhar ou estiver pendente, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) retornará zero. Para obter informações de erro estendidas, chame [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentários

Esse código de controle não tem nenhum arquivo de header associado. Você deve definir o código de controle e as estruturas de dados da seguinte forma.

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

Os membros da estrutura podem ser descritos da seguinte forma.

<dl> <dt>

<span id="SpecData1"></span><span id="specdata1"></span><span id="SPECDATA1"></span>**SpecData1**
</dt> <dd>

Um valor opaco que é usado para tipos de arquivo especiais, como arquivos ESPECIAIS de bloco, especiais de caracteres e FIFO.

</dd> <dt>

<span id="SpecData2"></span><span id="specdata2"></span><span id="SPECDATA2"></span>**SpecData2**
</dt> <dd>

Um valor opaco que é usado para tipos de arquivo especiais, como arquivos ESPECIAIS de bloco, especiais de caracteres e FIFO.

</dd> <dt>

<span id="Seconds"></span><span id="seconds"></span><span id="SECONDS"></span>**Segundos**
</dt> <dd>

Um valor de 64 bits que representa os segundos desde 1º de janeiro de 1970 (UTC).

</dd> <dt>

<span id="nSeconds"></span><span id="nseconds"></span><span id="NSECONDS"></span>**nSeconds**
</dt> <dd>

O número de nanossegundos a serem adicionados ao **membro Seconds.**

</dd> <dt>

<span id="FileType"></span><span id="filetype"></span><span id="FILETYPE"></span>**Filetype**
</dt> <dd>

O tipo de arquivo NFS do compartilhamento.



| Tipo de arquivo NFS                                                                              | Descrição                          |
|--------------------------------------------------------------------------------------------|--------------------------------------|
| <span id="NFS_TYPE_REG"></span><span id="nfs_type_reg"></span>REG DE TIPO NFS \_ \_<br/>    | Um arquivo regular.<br/>           |
| <span id="NFS_TYPE_DIR"></span><span id="nfs_type_dir"></span>DIR DO TIPO NFS \_ \_<br/>    | Um diretório.<br/>              |
| <span id="NFS_TYPE_BLK"></span><span id="nfs_type_blk"></span>TIPO NFS \_ \_ BLK<br/>    | Um arquivo especial de bloco.<br/>     |
| <span id="NFS_TYPE_CHR"></span><span id="nfs_type_chr"></span>CHR DE TIPO \_ \_ NFS<br/>    | Um arquivo especial de caractere.<br/> |
| <span id="NFS_TYPE_LNK"></span><span id="nfs_type_lnk"></span>TIPO NFS \_ \_ LNK<br/>    | Um link simbólico.<br/>          |
| <span id="NFS_TYPE_SOCK"></span><span id="nfs_type_sock"></span>TIPO NFS \_ \_ SOCK<br/> | Um soquete Windows de dados.<br/>         |
| <span id="NFS_TYPE_FIFO"></span><span id="nfs_type_fifo"></span>TIPO NFS \_ \_ FIFO<br/> | Um arquivo FIFO.<br/>              |



 

</dd> <dt>

<span id="Mode"></span><span id="mode"></span><span id="MODE"></span>**Modo**
</dt> <dd>

O modo de arquivo.

</dd> <dt>

<span id="NLink"></span><span id="nlink"></span><span id="NLINK"></span>**NLink**
</dt> <dd>

O número de links para o compartilhamento.

</dd> <dt>

<span id="Uid"></span><span id="uid"></span><span id="UID"></span>**Uid**
</dt> <dd>

O UNIX identificador de usuário (UID).

</dd> <dt>

<span id="Gid"></span><span id="gid"></span><span id="GID"></span>**Gid**
</dt> <dd>

O GID (identificador UNIX grupo de dados).

</dd> <dt>

<span id="Size"></span><span id="size"></span><span id="SIZE"></span>**Tamanho**
</dt> <dd>

O tamanho do arquivo, em bytes.

</dd> <dt>

<span id="Used"></span><span id="used"></span><span id="USED"></span>**Usado**
</dt> <dd>

O tamanho do arquivo usado, em bytes. Isso é o mesmo que o tamanho do arquivo.

</dd> <dt>

<span id="Rdev"></span><span id="rdev"></span><span id="RDEV"></span>**Ãov**
</dt> <dd>

O identificador do dispositivo.

</dd> <dt>

<span id="Fsid"></span><span id="fsid"></span><span id="FSID"></span>**Fsid**
</dt> <dd>

O identificador do sistema de arquivos.

</dd> <dt>

<span id="FileId"></span><span id="fileid"></span><span id="FILEID"></span>**Idarquivo**
</dt> <dd>

O identificador de arquivo.

</dd> <dt>

<span id="AccessTime"></span><span id="accesstime"></span><span id="ACCESSTIME"></span>**AccessTime**
</dt> <dd>

A hora do último acesso.

</dd> <dt>

<span id="ModifyTime"></span><span id="modifytime"></span><span id="MODIFYTIME"></span>**ModifyTime**
</dt> <dd>

A hora da última modificação.

</dd> <dt>

<span id="ChangeTime"></span><span id="changetime"></span><span id="CHANGETIME"></span>**ChangeTime**
</dt> <dd>

A hora da última alteração.

</dd> <dt>

<span id="FileAttributes"></span><span id="fileattributes"></span><span id="FILEATTRIBUTES"></span>**Fileattributes**
</dt> <dd>

Uma **estrutura de ATRIBUTOS DE \_ ARQUIVO \_ NFS.**

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

 

 
