---
title: Enumerar arquivos e diretórios
description: Descreve como um provedor ProjFS participa da enumeração de diretório.
ms.assetid: <GUID-GOES-HERE>
ms.date: 09/25/2018
ms.topic: article
ms.openlocfilehash: 606b379e206cdbc64726e0ea97aed34e00f5253ecbffb7f8b7d42469b0cbb5fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792809"
---
# <a name="enumerating-files-and-directories"></a>Enumerar arquivos e diretórios

Quando um provedor cria pela primeira vez uma raiz de virtualização, ele está vazio no sistema local.  Ou seja, nenhum dos itens no armazenamento de dados de backup ainda foi armazenado em cache no disco.  À medida que cada item é aberto, ele é armazenado em cache, mas até que um item seja aberto, ele só existe no armazenamento de dados de backup.

Como os itens não abertos não têm presença local, a enumeração de diretório normal não revelaria sua existência ao usuário.  Portanto, o provedor deve participar da enumeração de diretório retornando informações para ProjFS sobre os itens em seu armazenamento de dados de backup.  O ProjFS mescla as informações do provedor com o que está no sistema de arquivos local para apresentar ao usuário uma lista unificada do conteúdo de um diretório.

## <a name="directory-enumeration-callbacks"></a>Retornos de chamada de enumeração de diretório

Para participar da enumeração de diretório, o provedor deve implementar os retornos de chamada **[PRJ_START_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb)**, **[PRJ_GET_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb)** e **[PRJ_END_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_end_directory_enumeration_cb)** .  Quando um diretório na raiz de virtualização do provedor é enumerado, o ProjFS executa as seguintes ações:

1. ProjFS chama o retorno de chamada de **PRJ_START_DIRECTORY_ENUMERATION_CB** do provedor para iniciar uma sessão de enumeração.

    Como parte do processamento desse retorno de chamada, o provedor deve se preparar para executar a enumeração.  Por exemplo, ele deve alocar qualquer memória que possa precisar acompanhar o progresso da enumeração em seu armazenamento de dados de backup.

    ProjFS identifica o diretório que está sendo enumerado no membro **FilePathName** do parâmetro _callbackdata_ do retorno de chamada.  Isso é especificado como um caminho relativo à raiz de virtualização.  Por exemplo, se a raiz de virtualização estiver localizada em `C:\virtRoot` , e o diretório que está sendo enumerado for `C:\virtRoot\dir1\dir2` , o membro **FilePathName** conterá `dir1\dir2` .  O provedor se preparará para enumerar esse caminho em seu armazenamento de dados de backup.  Dependendo dos recursos do armazenamento de backup de um provedor, pode fazer sentido executar a enumeração de armazenamento de backup no retorno de chamada de **PRJ_START_DIRECTORY_ENUMERATION_CB** .

    Como várias enumerações podem ocorrer em paralelo no mesmo diretório, cada retorno de chamada de enumeração tem um argumento _enumerationid_ para permitir que o provedor associe as invocações de retorno de chamada em uma única sessão de enumeração.

    Se o provedor retornar S_OK do **PRJ_START_DIRECTORY_ENUMERATION_CB** retorno de chamada, ele deverá manter todas as informações de sessão de enumeração que ele tiver até que ProjFS invoque o retorno de chamada **PRJ_END_DIRECTORY_ENUMERATION_CB** com o mesmo valor para _enumerationid_.  Se o provedor retornar um erro de **PRJ_START_DIRECTORY_ENUMERATION_CB**, ProjFS não invocará o retorno de chamada **PRJ_END_DIRECTORY_ENUMERATION_CB** para essa _enumerationid_.

1. ProjFS chama o retorno de chamada de **PRJ_GET_DIRECTORY_ENUMERATION_CB** do provedor uma ou mais vezes para obter o conteúdo do diretório do provedor.

    Em resposta a esse retorno de chamada, o provedor retorna uma lista classificada de itens de seu armazenamento de dados de backup.

    O retorno de chamada pode fornecer uma expressão de pesquisa em seu parâmetro _searchexception_ que o provedor usa para fazer o escopo dos resultados da enumeração.  Se _searchtable_ for NULL, o provedor retornará todas as entradas no diretório que está sendo enumerado.  Se não for nulo, o provedor poderá usar **[PrjDoesNameContainWildCards](/windows/win32/api/projectedfslib/nf-projectedfslib-prjdoesnamecontainwildcards)** para determinar se há curingas na expressão.  Se houver, o provedor usará **[PrjFileNameMatch](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamematch)** para determinar se uma entrada no diretório corresponde à expressão de pesquisa.

    O provedor deve capturar o valor de _searchion_ na primeira invocação deste retorno de chamada.  Ele usa o valor capturado em qualquer invocação subseqüente do retorno de chamada na mesma sessão de enumeração, a menos que PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN seja definido no campo **flags** do parâmetro _callbackdata_ do retorno de chamada.  Nesse caso, ele deve recapturar o valor de _searchexception_.

    Se não houver entradas correspondentes em seu repositório de backup, o provedor simplesmente retornará S_OK do retorno de chamada.  Caso contrário, o provedor formata cada entrada correspondente de seu armazenamento de backup em uma estrutura de **[PRJ_FILE_BASIC_INFO](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_file_basic_info)** e, em seguida, usa **[PrjFillDirEntryBuffer](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer)** para preencher o buffer fornecido pelo parâmetro _dirEntryBufferHandle_ do retorno de chamada.  O provedor continua adicionando entradas até ter adicionado todos eles ou até que **PrjFillDirEntryBuffer** retorne HRESULT_FROM_WIN32 (ERROR_INSUFFICIENT_BUFFER).  Em seguida, o provedor retorna S_OK do retorno de chamada.  Observe que o provedor deve adicionar as entradas ao buffer _dirEntryBufferHandle_ na ordem de classificação correta.  O provedor deve usar **[PrjFileNameCompare](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamecompare)** para determinar a ordem de classificação correta.

    > O provedor deve fornecer um valor para o membro **IsDirectory** de **PRJ_FILE_BASIC_INFO**.  Se **IsDirectory** for false, o provedor também deverá fornecer um valor para o membro **filesize** .
    >
    > Se o provedor não fornecer valores para os membros **CreationTime**, **LastAccessTime**, **LastWriteTime** e **changetime** , ProjFS usará a hora atual do sistema.
    >
    > ProjFS usará qualquer FILE_ATTRIBUTE sinalizar os conjuntos de provedores no membro **FileAttributes** , exceto por FILE_ATTRIBUTE_DIRECTORY; ele definirá o valor correto para FILE_ATTRIBUTE_DIRECTORY no membro **FileAttributes** , de acordo com o valor fornecido do membro **IsDirectory** .

    Se **PrjFillDirEntryBuffer** retornar HRESULT_FROM_WIN32 (ERROR_INSUFFICIENT_BUFFER) antes que o provedor fique sem entradas para adicionar a ele, o provedor deverá manter o controle da entrada que estava tentando adicionar quando recebeu o erro.  Na próxima vez que o ProjFS chamar o retorno de chamada **PRJ_GET_DIRECTORY_ENUMERATION_CB** para a mesma sessão de enumeração, o provedor deverá retomar a adição de entradas ao buffer _dirEntryBufferHandle_ com a entrada que estava tentando adicionar.

    > Se o repositório de backup der suporte a links simbólicos, o provedor deverá usar **[PrjFillDirEntryBuffer2](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer2)** para preencher o buffer fornecido pelo parâmetro _dirEntryBufferHandle_ do retorno de chamada.  O **PrjFillDirEntryBuffer2** dá suporte a uma entrada de buffer extra que permite que o provedor especifique que a entrada de enumeração é um link simbólico e qual é o seu destino.  Caso contrário, ele se comporta conforme descrito acima para **PrjFillDirEntryBuffer**.  O exemplo a seguir usa **PrjFillDirEntryBuffer2** para ilustrar o suporte para links simbólicos.
    >
    > observe que **PrjFillDirEntryBuffer2** tem suporte a partir de Windows 10, versão 2004.  Um provedor deve investigar a existência de **PrjFillDirEntryBuffer2**, por exemplo, usando **[GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)**.

    ```C++
    typedef struct MY_ENUM_ENTRY MY_ENUM_ENTRY;

    typedef struct MY_ENUM_ENTRY {
        MY_ENUM_ENTRY* Next;
        PWSTR Name;
        BOOLEAN IsDirectory;
        INT64 FileSize;
        BOOLEAN IsSymlink;
        PWSTR SymlinkTarget;
    } MY_ENUM_ENTRY;

    typedef struct MY_ENUM_SESSION {
        GUID EnumerationId;
        PWSTR SearchExpression;
        USHORT SearchExpressionMaxLen;
        BOOLEAN SearchExpressionCaptured;
        MY_ENUM_ENTRY* EnumHead;
        MY_ENUM_ENTRY* LastEnumEntry;
        BOOLEAN EnumCompleted;
    } MY_ENUM_SESSION;

    HRESULT
    MyGetEnumCallback(
        _In_ const PRJ_CALLBACK_DATA* callbackData,
        _In_ const GUID* enumerationId,
        _In_opt_z_ PCWSTR searchExpression,
        _In_ PRJ_DIR_ENTRY_BUFFER_HANDLE dirEntryBufferHandle
        )
    {
        // MyGetEnumSession is a routine the provider might implement to find
        // information about the enumeration session that it first stored
        // when processing its PRJ_START_DIRECTORY_ENUMERATION_CB callback.
        //
        // In this example the PRJ_START_DIRECTORY_ENUMERATION_CB callback has
        // already retrieved a list of the items in the backing store located at
        // callbackData->FilePathName, sorted them using PrjFileNameCompare()
        // to determine collation order, and stored the list in session->EnumHead.
        MY_ENUM_SESSION* session = NULL;
        session = MyGetEnumSession(enumerationId);

        if (session == NULL)
        {
            return HRESULT_FROM_WIN32(ERROR_INVALID_PARAMETER);
        }

        if (!session->SearchExpressionCaptured ||
            (callbackData->Flags & PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN))
        {
            if (searchExpression != NULL)
            {
                if (wcsncpy_s(session->SearchExpression,
                              session->SearchExpressionMaxLen,
                              searchExpression,
                              wcslen(searchExpression)))
                {
                    // Failed to copy the search expression; perhaps the provider
                    // could try reallocating session->SearchExpression.
                }
            }
            else
            {
                if (wcsncpy_s(session->SearchExpression,
                              session->SearchExpressionMaxLen,
                              "*",
                              1))
                {
                    // Failed to copy the search expression; perhaps the provider
                    // could try reallocating session->SearchExpression.
                }
            }
            session->SearchExpressionCaptured = TRUE;
        }

        MY_ENUM_ENTRY* enumHead = NULL;

        // We have to start the enumeration from the beginning if we aren't
        // continuing an existing session or if the caller is requesting a restart.
        if (((session->LastEnumEntry == NULL) &&
             !session->EnumCompleted) ||
            (callbackData->Flags & PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN))
        {
            // Ensure that if the caller is requesting a restart we reset our
            // bookmark of how far we got in the enumeration.
            session->LastEnumEntry = NULL;

            // In case we're restarting ensure we don't think we're done.
            session->EnumCompleted = FALSE;

            // We need to start considering items from the beginning of the list
            // retrieved from the backing store.
            enumHead = session->EnumHead;
        }
        else
        {
            // We are resuming an existing enumeration session.  Note that
            // session->LastEnumEntry may be NULL.  That is okay; it means
            // we got all the entries the last time this callback was invoked.
            // Returning S_OK without adding any new entries to the
            // dirEntryBufferHandle buffer signals ProjFS that the enumeration
            // has returned everything it can.
            enumHead = session->LastEnumEntry;
        }

        if (enumHead == NULL)
        {
            // There are no items to return.  Remember that we've returned everything
            // we can.
            session->EnumCompleted = TRUE;
        }
        else
        {
            MY_ENUM_ENTRY* thisEntry = enumHead;
            while (thisEntry != NULL)
            {
                // We'll insert the entry into the return buffer if it matches
                // the search expression captured for this enumeration session.
                if (PrjFileNameMatch(thisEntry->Name, session->SearchExpression))
                {
                    PRJ_FILE_BASIC_INFO fileBasicInfo = {};
                    fileBasicInfo.IsDirectory = thisEntry->IsDirectory;
                    fileBasicInfo.FileSize = thisEntry->FileSize;

                    // If our backing store says this is really a symbolic link,
                    // set up to tell ProjFS that it is a symlink and what its
                    // target is.
                    PRJ_EXTENDED_INFO extraInfo = {};
                    if (thisEntry->IsSymlink)
                    {
                        extraInfo.InfoType = PRJ_EXT_INFO_SYMLINK;
                        extraInfo.Symlink.TargetName = thisEntry->SymlinkTarget;
                    }

                    // Format the entry for return to ProjFS.
                    HRESULT fillResult = PrjFillDirEntryBuffer2(dirEntryBufferHandle,
                                                                thisEntry->Name,
                                                                &fileBasicInfo,
                                                                thisEntry->IsSymlink ? &extraInfo : NULL);

                    if (fillResult == HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER))
                    {
                        // We couldn't add this entry to the buffer; remember where we left
                        // off for the next time we're called for this enumeration session.
                        session->LastEnumEntry = thisEntry;
                        return S_OK;
                    }
                }

                thisEntry = thisEntry->Next;
            }

            // We reached the end of the list of entries; remember that we've returned
            // everything we can.
            session->EnumCompleted = TRUE;
        }

        return S_OK;
    }
    ```

1. ProjFS chama o retorno de chamada de **PRJ_END_DIRECTORY_ENUMERATION_CB** do provedor para encerrar a sessão de enumeração.

    O provedor deve executar qualquer limpeza que precise fazer para encerrar a sessão de enumeração, como desalocar a memória alocada como parte do **PRJ_START_DIRECTORY_ENUMERATION_CB** de processamento.
