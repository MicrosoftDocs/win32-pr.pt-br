---
Description: A seguir estão as opções de proteção de memória; Você deve especificar um dos valores a seguir ao alocar ou proteger uma página na memória. Atributos de proteção não podem ser atribuídos a uma parte de uma página; Eles só podem ser atribuídos a uma página inteira.
ms.assetid: 09839db7-2118-4a7d-a707-a08c92bd600c
title: Constantes de proteção de memória (WinNT. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 641fab68024d9db96f50327f7c78d51f3f9bca01
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783284"
---
# <a name="memory-protection-constants"></a>Constantes de proteção de memória

A seguir estão as opções de proteção de memória; Você deve especificar um dos valores a seguir ao alocar ou proteger uma página na memória. Atributos de proteção não podem ser atribuídos a uma parte de uma página; Eles só podem ser atribuídos a uma página inteira.

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
Exemplo, de [exemplos clássicos do Windows](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/dataaccess/oledb/sampprov/extbuff.cpp) no github.

## <a name="constants"></a>Constantes


| Constante/valor                                                                                                                                                                                                                                             | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PAGE_EXECUTE"></span><span id="page_execute"></span><dl> <dt>**Página \_ do EXECUTAR**</dt> <dt>0x10</dt> </dl>                                       | Habilita o acesso de execução à região confirmada de páginas. Uma tentativa de gravar na região confirmada resulta em uma violação de acesso.<br/> Não há suporte para esse sinalizador na função [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="PAGE_EXECUTE_READ"></span><span id="page_execute_read"></span><dl> <dt>**Página \_ do EXECUTAR \_ leitura**</dt> <dt>0x20</dt> </dl>                       | Habilita o acesso de execução ou somente leitura à região confirmada de páginas. Uma tentativa de gravar na região confirmada resulta em uma violação de acesso.<br/> **Windows Server 2003 e Windows XP:** Esse atributo não tem suporte da função [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) até o Windows XP com SP2 e o windows Server 2003 com SP1.<br/>                                                                                                                                                                                                                                                                                                                                |
| <span id="PAGE_EXECUTE_READWRITE"></span><span id="page_execute_readwrite"></span><dl> <dt>**Página \_ do EXECUTAR \_ ReadWrite**</dt> <dt>0x40</dt> </dl>        | Permite o acesso de execução, somente leitura ou de leitura/gravação à região confirmada de páginas.<br/> **Windows Server 2003 e Windows XP:** Esse atributo não tem suporte da função [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) até o Windows XP com SP2 e o windows Server 2003 com SP1.<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="PAGE_EXECUTE_WRITECOPY"></span><span id="page_execute_writecopy"></span><dl> <dt>**Página \_ do EXECUTAR \_ WRITECOPY**</dt> <dt>0x80</dt> </dl>        | Permite o acesso de execução, somente leitura ou de cópia em gravação a uma exibição mapeada de um objeto de mapeamento de arquivo. Uma tentativa de gravar em uma página de cópia em gravação confirmada resulta em uma cópia particular da página que está sendo feita para o processo. A página particular é marcada como **página \_ executar \_ ReadWrite** e a alteração é gravada na nova página.<br/> Não há suporte para esse sinalizador nas funções [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) ou [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) . **Windows Vista, Windows Server 2003 e Windows XP:** Esse atributo não tem suporte da função [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) até o Windows Vista com SP1 e o windows Server 2008.<br/> <br/> |
| <span id="PAGE_NOACCESS"></span><span id="page_noaccess"></span><dl> <dt>**Página \_ do Não acessar**</dt> <dt>0x01</dt> </dl>                                    | Desabilita todo o acesso à região confirmada de páginas. Uma tentativa de ler, gravar ou executar a região confirmada resulta em uma violação de acesso.<br/> Não há suporte para esse sinalizador na função [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="PAGE_READONLY"></span><span id="page_readonly"></span><dl> <dt>**Página \_ do 0x02 somente leitura**</dt> <dt></dt> </dl>                                    | Habilita o acesso somente leitura à região confirmada de páginas. Uma tentativa de gravar na região confirmada resulta em uma violação de acesso. Se a [prevenção de execução de dados](data-execution-prevention.md) estiver habilitada, uma tentativa de executar o código na região confirmada resultará em uma violação de acesso.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="PAGE_READWRITE"></span><span id="page_readwrite"></span><dl> <dt>**Página \_ do READWRITE**</dt> <dt>0x04</dt> </dl>                                 | Permite acesso somente leitura ou leitura/gravação à região confirmada de páginas. Se a [prevenção de execução de dados](data-execution-prevention.md) estiver habilitada, a tentativa de executar o código na região confirmada resultará em uma violação de acesso.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="PAGE_WRITECOPY"></span><span id="page_writecopy"></span><dl> <dt>**Página \_ do WRITECOPY**</dt> <dt>0x08</dt> </dl>                                 | Habilita o acesso somente leitura ou de cópia em gravação a uma exibição mapeada de um objeto de mapeamento de arquivo. Uma tentativa de gravar em uma página de cópia em gravação confirmada resulta em uma cópia particular da página que está sendo feita para o processo. A página particular é marcada como a **página \_ ReadWrite** e a alteração é gravada na nova página. Se a [prevenção de execução de dados](data-execution-prevention.md) estiver habilitada, a tentativa de executar o código na região confirmada resultará em uma violação de acesso.<br/> Não há suporte para esse sinalizador nas funções [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) ou [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) .<br/>                                                                               |
| <span id="PAGE_TARGETS_INVALID"></span><span id="page_targets_invalid"></span><dl> <dt>**Página \_ do DESTINOS \_**</dt> <dt>0x40000000</dt> inválido </dl>        | Define todos os locais nas páginas como destinos inválidos para CFG. Usado junto com qualquer proteção de página de execução como a **página \_ executar**, a **página \_ executar \_ leitura**, a **página \_ executar \_ ReadWrite** e a **página \_ executar \_ WRITECOPY**. Qualquer chamada indireta para locais nessas páginas falhará em CFG e o processo será encerrado. O comportamento padrão para páginas executáveis alocadas deve ser marcado como destinos de chamada válidos para CFG.<br/> Não há suporte para esse sinalizador nas funções [**usar VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect) ou [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) .<br/>                                                                                                              |
| <span id="PAGE_TARGETS_NO_UPDATE"></span><span id="page_targets_no_update"></span><dl> <dt>**Página \_ do DESTINOS \_ sem \_**</dt> <dt>0x40000000</dt> de atualização </dl> | As páginas na região não terão suas informações de CFG atualizadas enquanto a proteção for alterada para [**usar VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect). Por exemplo, se as páginas na região foram alocadas usando **destinos de página \_ \_ inválidos**, as informações inválidas serão mantidas enquanto a proteção de página for alterada. Esse sinalizador só é válido quando a proteção é alterada para um tipo de executável como a **página \_ executar**, a **página \_ executar \_ leitura**, a **página \_ executar \_ ReadWrite** e a **página \_ executar \_ WRITECOPY**. O comportamento padrão para a proteção de **usar VirtualProtect** mudar para executável é marcar todos os locais como destinos de chamada válidos para cfg. <br/>                                           |



Estes são os modificadores que podem ser usados além das opções fornecidas na tabela anterior, exceto quando observado.



| Constante/valor                                                                                                                                                                                                                       | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PAGE_GUARD"></span><span id="page_guard"></span><dl> <dt>**Página \_ do PROTEÇÃO**</dt> <dt>0x100</dt> </dl>                      | As páginas na região se tornam páginas de proteção. Qualquer tentativa de acessar uma página de proteção faz com que o sistema gere uma exceção de **violação de página de proteção de status \_ \_ \_** e desative o status da página de proteção. Assim, as páginas de proteção atuam como um alarme de acesso único. Para obter mais informações, consulte [Criando páginas de proteção](creating-guard-pages.md).<br/> Quando uma tentativa de acesso leva o sistema para desligar o status da página de proteção, a proteção de página subjacente assume.<br/> Se ocorrer uma exceção de página de proteção durante um serviço do sistema, o serviço normalmente retornará um indicador de status de falha.<br/> Esse valor não pode ser usado com a **página \_ NoAccess**.<br/> Não há suporte para esse sinalizador na função [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) .<br/>                                                                                                                                                                                                                              |
| <span id="PAGE_NOCACHE"></span><span id="page_nocache"></span><dl> <dt>**Página \_ do 0x200 NoCache**</dt> <dt></dt> </dl>                | Define todas as páginas como não armazenável. Os aplicativos não devem usar esse atributo, exceto quando explicitamente exigidos para um dispositivo. O uso de funções interligadas com memória mapeada com **s \_ NoCache** pode resultar em uma exceção **de \_ \_ instrução inválida** .<br/> O **sinalizador \_ NoCache da página** não pode ser usado com os sinalizadores Page **\_ Guard**, **Page \_ NoAccess** ou **Page \_ WRITECOMBINE** .<br/> O **sinalizador \_ NoCache da página** só pode ser usado ao alocar memória privada com as funções [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc), [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex)ou [**VirtualAllocExNuma**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma) . Para habilitar o acesso de memória não cache para a memória compartilhada, especifique o sinalizador **s \_ NoCache** ao chamar a função [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) .<br/>                                                                                                                                                   |
| <span id="PAGE_WRITECOMBINE"></span><span id="page_writecombine"></span><dl> <dt>**Página \_ do WRITECOMBINE**</dt> <dt>0x400</dt> </dl> | Define todas as páginas que serão combinadas com gravação. <br/> Os aplicativos não devem usar esse atributo, exceto quando explicitamente exigidos para um dispositivo. O uso de funções interligadas com memória mapeada como de gravação combinada pode resultar em uma exceção **de \_ \_ instrução inválida de exceções** . <br/> O sinalizador de **\_ WRITECOMBINE de página** não pode ser especificado com sinalizadores **\_ NoAccess**, **Page \_ Guard** e **Page \_ NoCache** de página. <br/> O **sinalizador \_ WRITECOMBINE de página** só pode ser usado ao alocar memória privada com as funções [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc), [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex)ou [**VirtualAllocExNuma**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma) . Para habilitar o acesso de memória combinada de gravação para a memória compartilhada, especifique o sinalizador **SEC \_ WRITECOMBINE** ao chamar a função [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) .<br/> **Windows Server 2003 e Windows XP:** Não há suporte para esse sinalizador até o Windows Server 2003 com SP1.<br/> |



As constantes a seguir só podem ser usadas com a função [**LoadEnclaveData**](/windows/desktop/api/enclaveapi/nf-enclaveapi-loadenclavedata) quando você especifica um enclave que tem a arquitetura de SGX (software Guard) da Intel.



| Constante                                                                                                                                                                                                  | Descrição                                                                                                                                 |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PAGE_ENCLAVE_THREAD_CONTROL"></span><span id="page_enclave_thread_control"></span><dl> <dt>**controle de thread de página \_ enclave \_ \_**</dt> </dl> | A página contém uma estrutura de controle de thread (TCS).<br/>                                                                              |
| <span id="PAGE_ENCLAVE_UNVALIDATED"></span><span id="page_enclave_unvalidated"></span><dl> <dt>**PÁGINA \_ enclave não \_ validada**</dt> </dl>           | O conteúdo da página que você fornece é excluído da medição com a instrução EEXTEND do modelo de programação SGX da Intel.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                   |
| parâmetro<br/>                   | <dl> <dt>WinNT. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga)
</dt> <dt>

[Proteção de memória](memory-protection.md)
</dt> <dt>

[**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)
</dt> <dt>

[**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex)
</dt> <dt>

[**LoadEnclaveData**](/windows/desktop/api/enclaveapi/nf-enclaveapi-loadenclavedata)
</dt> </dl>

 

 
