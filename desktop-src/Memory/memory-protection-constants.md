---
Description: A seguir estão as opções de proteção de memória; você deve especificar um dos valores a seguir ao alocar ou proteger uma página na memória. Os atributos de proteção não podem ser atribuídos a uma parte de uma página; eles só podem ser atribuídos a uma página inteira.
ms.assetid: 09839db7-2118-4a7d-a707-a08c92bd600c
title: Constantes de proteção de memória (WinNT.h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 187e8e1f4e137823451771309c9cce19db2e7fbd9c5b57597b51cfc58ca61297
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067686"
---
# <a name="memory-protection-constants"></a>Constantes de proteção de memória

A seguir estão as opções de proteção de memória; você deve especificar um dos valores a seguir ao alocar ou proteger uma página na memória. Os atributos de proteção não podem ser atribuídos a uma parte de uma página; eles só podem ser atribuídos a uma página inteira.

## <a name="example"></a>Exemplo

```cpp
STDMETHODIMP CExtBuffer::FInit
    (
    ULONG cItemMax,     //@parm IN | Maximum number of items ever
    ULONG cbItem,       //@parm IN | Size of each item, in bytes
    ULONG cbPage        //@parm IN | Size of system page size (from SysInfo)
    )
{
    BYTE  *pb;

    m_cbReserved = ((cbItem *cItemMax) / cbPage + 1) *cbPage;
    m_rgItem = (BYTE *) VirtualAlloc( NULL, m_cbReserved, MEM_RESERVE, PAGE_READWRITE );

    if (m_rgItem == NULL)
        return ResultFromScode( E_OUTOFMEMORY );

    m_cbItem  = cbItem;
    m_dbAlloc = (cbItem / cbPage + 1) *cbPage;
    pb = (BYTE *) VirtualAlloc( m_rgItem, m_dbAlloc, MEM_COMMIT, PAGE_READWRITE );
    if (pb == NULL)
        {
        VirtualFree((VOID *) m_rgItem, 0, MEM_RELEASE );
        m_rgItem = NULL;
        return ResultFromScode( E_OUTOFMEMORY );
        }

    m_cbAlloc = m_dbAlloc;
    return ResultFromScode( S_OK );
}
```
Exemplo de exemplo [Windows exemplos clássicos](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/dataaccess/oledb/sampprov/extbuff.cpp) em GitHub.

## <a name="constants"></a>Constantes


| Constante/valor                                                                                                                                                                                                                                             | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PAGE_EXECUTE"></span><span id="page_execute"></span><dl> <dt>**PAGE \_ EXECUTE**</dt> <dt>0x10</dt> </dl>                                       | Habilita o acesso de execução à região de páginas comprometida. Uma tentativa de gravar na região comprometida resulta em uma violação de acesso.<br/> Não há suporte para esse sinalizador na [**função CreateFileMapping.**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="PAGE_EXECUTE_READ"></span><span id="page_execute_read"></span><dl> <dt>**PAGE \_ EXECUTE \_ READ**</dt> <dt>0x20</dt> </dl>                       | Habilita o acesso somente leitura ou execução à região de páginas comprometida. Uma tentativa de gravar na região comprometida resulta em uma violação de acesso.<br/> **Windows Server 2003 e Windows XP:** Esse atributo não é suportado pela [**função CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) até que Windows XP com SP2 e Windows Server 2003 com SP1.<br/>                                                                                                                                                                                                                                                                                                                                |
| <span id="PAGE_EXECUTE_READWRITE"></span><span id="page_execute_readwrite"></span><dl> <dt>**PAGE \_ EXECUTE \_ READWRITE**</dt> <dt>0x40</dt> </dl>        | Habilita o acesso de execução, somente leitura ou leitura/gravação à região de páginas comprometida.<br/> **Windows Server 2003 e Windows XP:** Esse atributo não é suportado pela [**função CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) até que Windows XP com SP2 e Windows Server 2003 com SP1.<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="PAGE_EXECUTE_WRITECOPY"></span><span id="page_execute_writecopy"></span><dl> <dt>**PAGE \_ EXECUTE \_ WRITECOPY**</dt> <dt>0x80</dt> </dl>        | Habilita o acesso de execução, somente leitura ou cópia em gravação a uma exibição mapeada de um objeto de mapeamento de arquivo. Uma tentativa de gravar em uma página de cópia na gravação comprometida resulta em uma cópia privada da página que está sendo feita para o processo. A página privada é marcada como **PAGE \_ EXECUTE \_ READWRITE** e a alteração é escrita na nova página.<br/> Não há suporte para esse sinalizador nas [**funções VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) ou [**VirtualAllocEx.**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) **Windows Vista, Windows Server 2003 e Windows XP:** Esse atributo não é suportado pela [**função CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) até Windows Vista com SP1 e Windows Server 2008.<br/> <br/> |
| <span id="PAGE_NOACCESS"></span><span id="page_noaccess"></span><dl> <dt>**PAGE \_ NOACCESS**</dt> <dt>0x01</dt> </dl>                                    | Desabilita todo o acesso à região de páginas comprometida. Uma tentativa de ler, gravar ou executar a região comprometida resulta em uma violação de acesso.<br/> Não há suporte para esse sinalizador na [**função CreateFileMapping.**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="PAGE_READONLY"></span><span id="page_readonly"></span><dl> <dt>**PAGE \_ READONLY**</dt> <dt>0x02</dt> </dl>                                    | Habilita o acesso somente leitura à região de páginas comprometida. Uma tentativa de gravar na região comprometida resulta em uma violação de acesso. Se [a Prevenção de](data-execution-prevention.md) Execução de Dados estiver habilitada, uma tentativa de executar o código na região comprometida resulta em uma violação de acesso.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="PAGE_READWRITE"></span><span id="page_readwrite"></span><dl> <dt>**PAGE \_ READWRITE**</dt> <dt>0x04</dt> </dl>                                 | Habilita o acesso somente leitura ou leitura/gravação à região de páginas comprometida. Se [a Prevenção de Execução](data-execution-prevention.md) de Dados estiver habilitada, a tentativa de executar o código na região comprometida resulta em uma violação de acesso.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="PAGE_WRITECOPY"></span><span id="page_writecopy"></span><dl> <dt>**PAGE \_ WRITECOPY**</dt> <dt>0x08</dt> </dl>                                 | Habilita o acesso somente leitura ou cópia em gravação a uma exibição mapeada de um objeto de mapeamento de arquivo. Uma tentativa de gravar em uma página de cópia na gravação comprometida resulta em uma cópia privada da página que está sendo feita para o processo. A página privada é marcada como **PAGE \_ READWRITE** e a alteração é escrita na nova página. Se [a Prevenção de Execução](data-execution-prevention.md) de Dados estiver habilitada, a tentativa de executar o código na região comprometida resulta em uma violação de acesso.<br/> Não há suporte para esse sinalizador nas [**funções VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) ou [**VirtualAllocEx.**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex)<br/>                                                                               |
| <span id="PAGE_TARGETS_INVALID"></span><span id="page_targets_invalid"></span><dl> <dt>**PAGE \_ DESTINOS \_ INVÁLIDOS**</dt> <dt>0X40000000</dt> </dl>        | Define todos os locais nas páginas como destinos inválidos para CFG. Usado junto com qualquer proteção de página de execução, como **PAGE \_ EXECUTE**, **PAGE EXECUTE \_ \_ READ**, **PAGE EXECUTE \_ \_ READWRITE** e **PAGE EXECUTE \_ \_ WRITECOPY**. Qualquer chamada indireta para locais nessas páginas falhará nas verificações do CFG e o processo será encerrado. O comportamento padrão para páginas executáveis alocadas deve ser marcado como destinos de chamada válidos para CFG.<br/> Não há suporte para esse sinalizador nas [**funções VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect) [**ou CreateFileMapping.**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga)<br/>                                                                                                              |
| <span id="PAGE_TARGETS_NO_UPDATE"></span><span id="page_targets_no_update"></span><dl> <dt>**PAGE \_ DESTINOS \_ SEM \_ ATUALIZAÇÃO**</dt> <dt>0X40000000</dt> </dl> | As páginas na região não terão suas informações de CFG atualizadas enquanto a proteção mudar [**para o VirtualProtect.**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect) Por exemplo, se as páginas na região foram alocadas usando **PAGE \_ TARGETS \_ INVALID**, as informações inválidas serão mantidas enquanto a proteção de página for mudada. Esse sinalizador só é válido quando a proteção muda para um tipo executável como **PAGE \_ EXECUTE**, **PAGE EXECUTE \_ \_ READ**, **PAGE EXECUTE \_ \_ READWRITE** **e PAGE EXECUTE \_ \_ WRITECOPY**. O comportamento padrão para a alteração **da proteção do VirtualProtect** para executável é marcar todos os locais como destinos de chamada válidos para CFG. <br/>                                           |



A seguir estão os modificadores que podem ser usados além das opções fornecidas na tabela anterior, exceto conforme o que foi feito.



| Constante/valor                                                                                                                                                                                                                       | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PAGE_GUARD"></span><span id="page_guard"></span><dl> <dt>**PAGE \_ Proteção**</dt> <dt>0x100</dt> </dl>                      | As páginas na região se tornam páginas de proteção. Qualquer tentativa de acessar uma página de proteção faz com que o sistema aumente uma exceção DE VIOLAÇÃO DE **PÁGINA DO STATUS \_ \_ \_ GUARD** e desligue o status da página de proteção. Portanto, as páginas de proteção atuam como um alarme de acesso único. Para obter mais informações, consulte [Criando páginas de proteção](creating-guard-pages.md).<br/> Quando uma tentativa de acesso leva o sistema a desligar o status da página de proteção, a proteção de página subjacente assume o controle.<br/> Se ocorrer uma exceção de página de proteção durante um serviço do sistema, o serviço normalmente retornará um indicador de status de falha.<br/> Esse valor não pode ser usado **com PAGE \_ NOACCESS**.<br/> Não há suporte para esse sinalizador na [**função CreateFileMapping.**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga)<br/>                                                                                                                                                                                                                              |
| <span id="PAGE_NOCACHE"></span><span id="page_nocache"></span><dl> <dt>**PAGE \_ NOCACHE**</dt> <dt>0x200</dt> </dl>                | Define todas as páginas como não cachable. Os aplicativos não devem usar esse atributo, exceto quando explicitamente necessário para um dispositivo. Usar as funções entrelaçadas com a memória mapeada com **SEC \_ NOCACHE** pode resultar em uma **exceção EXCEPTION \_ ILLEGAL \_ INSTRUCTION.**<br/> O **sinalizador \_ PAGE NOCACHE** não pode ser usado com os sinalizadores **PAGE \_ GUARD**, **PAGE \_ NOACCESS** ou **PAGE \_ WRITECOMBINE.**<br/> O **sinalizador \_ PAGE NOCACHE** pode ser usado somente ao alocar memória privada com as funções [**VirtualAlloc,**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex)ou [**VirtualAllocExNuma.**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma) Para habilitar o acesso à memória não armazenada em cache para memória compartilhada, especifique o sinalizador **\_ SEC NOCACHE** ao chamar a [**função CreateFileMapping.**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga)<br/>                                                                                                                                                   |
| <span id="PAGE_WRITECOMBINE"></span><span id="page_writecombine"></span><dl> <dt>**PAGE \_ WRITECOMBINE**</dt> <dt>0x400</dt> </dl> | Define todas as páginas a serem combinadas por gravação. <br/> Os aplicativos não devem usar esse atributo, exceto quando explicitamente necessário para um dispositivo. O uso das funções interlocked com a memória mapeada como combinação de gravação pode resultar em uma exceção **EXCEPTION \_ ILLEGAL \_ INSTRUCTION.** <br/> O **sinalizador \_ PAGE WRITECOMBINE** não pode ser especificado com os **sinalizadores PAGE \_ NOACCESS,** **PAGE \_ GUARD** e **PAGE \_ NOCACHE.** <br/> O **sinalizador \_ PAGE WRITECOMBINE** pode ser usado somente ao alocar memória privada com as funções [**VirtualAlloc,**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex)ou [**VirtualAllocExNuma.**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma) Para habilitar o acesso à memória combinada por gravação para memória compartilhada, especifique o sinalizador **\_ WRITECOMBINE da SEC** ao chamar a função [**CreateFileMapping.**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga)<br/> **Windows Server 2003 e Windows XP:** Esse sinalizador não tem suporte até Windows Server 2003 com SP1.<br/> |



As constantes a seguir só podem ser usadas com a função [**LoadEnclaveData**](/windows/desktop/api/enclaveapi/nf-enclaveapi-loadenclavedata) quando você especifica um enclave que tem a arquitetura intel Software Guard Extensions (SGX).



| Constante                                                                                                                                                                                                  | Descrição                                                                                                                                 |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PAGE_ENCLAVE_THREAD_CONTROL"></span><span id="page_enclave_thread_control"></span><dl> <dt>**CONTROLE DE \_ THREAD DE ENCLAVE \_ DE \_ PÁGINA**</dt> </dl> | A página contém uma estrutura de controle de thread (TCS).<br/>                                                                              |
| <span id="PAGE_ENCLAVE_UNVALIDATED"></span><span id="page_enclave_unvalidated"></span><dl> <dt>**\_ENCLAVE \_ DE PÁGINA NÃOVALIDADO**</dt> </dl>           | O conteúdo da página que você fornece é excluído da medida com a instrução EEXTEND do modelo de programação Intel SGX.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                   |
| Cabeçalho<br/>                   | <dl> <dt>WinNT.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Createfilemapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga)
</dt> <dt>

[Proteção de memória](memory-protection.md)
</dt> <dt>

[**Virtualalloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)
</dt> <dt>

[**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex)
</dt> <dt>

[**LoadEnclaveData**](/windows/desktop/api/enclaveapi/nf-enclaveapi-loadenclavedata)
</dt> </dl>

 

 
