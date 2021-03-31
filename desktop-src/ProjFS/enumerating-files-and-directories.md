---
title: Enumerar arquivos e diretórios
description: Descreve como um provedor ProjFS participa da enumeração de diretório.
ms.assetid: <GUID-GOES-HERE>
ms.date: 09/25/2018
ms.topic: article
ms.openlocfilehash: e0712ceb927388b090a84a89f80f0e2d3a1befbb
ms.sourcegitcommit: 80d74c0bf4fc402865a1ad223480abe1ce4d1115
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2020
ms.locfileid: "103640271"
---
# <a name="enumerating-files-and-directories"></a><span data-ttu-id="9605f-103">Enumerar arquivos e diretórios</span><span class="sxs-lookup"><span data-stu-id="9605f-103">Enumerating Files and Directories</span></span>

<span data-ttu-id="9605f-104">Quando um provedor cria pela primeira vez uma raiz de virtualização, ele está vazio no sistema local.</span><span class="sxs-lookup"><span data-stu-id="9605f-104">When a provider first creates a virtualization root it is empty on the local system.</span></span>  <span data-ttu-id="9605f-105">Ou seja, nenhum dos itens no armazenamento de dados de backup ainda foi armazenado em cache no disco.</span><span class="sxs-lookup"><span data-stu-id="9605f-105">That is, none of the items in the backing data store have yet been cached to disk.</span></span>  <span data-ttu-id="9605f-106">À medida que cada item é aberto, ele é armazenado em cache, mas até que um item seja aberto, ele só existe no armazenamento de dados de backup.</span><span class="sxs-lookup"><span data-stu-id="9605f-106">As each item is opened it is cached, but until an item is opened it only exists in the backing data store.</span></span>

<span data-ttu-id="9605f-107">Como os itens não abertos não têm presença local, a enumeração de diretório normal não revelaria sua existência ao usuário.</span><span class="sxs-lookup"><span data-stu-id="9605f-107">Since unopened items have no local presence, normal directory enumeration would not reveal their existence to the user.</span></span>  <span data-ttu-id="9605f-108">Portanto, o provedor deve participar da enumeração de diretório retornando informações para ProjFS sobre os itens em seu armazenamento de dados de backup.</span><span class="sxs-lookup"><span data-stu-id="9605f-108">Therefore the provider must participate in directory enumeration by returning information to ProjFS about items in its backing data store.</span></span>  <span data-ttu-id="9605f-109">O ProjFS mescla as informações do provedor com o que está no sistema de arquivos local para apresentar ao usuário uma lista unificada do conteúdo de um diretório.</span><span class="sxs-lookup"><span data-stu-id="9605f-109">ProjFS merges the information from the provider with what is on the local file system to present to the user a unified list of the contents of a directory.</span></span>

## <a name="directory-enumeration-callbacks"></a><span data-ttu-id="9605f-110">Retornos de chamada de enumeração de diretório</span><span class="sxs-lookup"><span data-stu-id="9605f-110">Directory Enumeration Callbacks</span></span>

<span data-ttu-id="9605f-111">Para participar da enumeração de diretório, o provedor deve implementar os retornos de chamada **[PRJ_START_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb)**, **[PRJ_GET_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb)** e **[PRJ_END_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_end_directory_enumeration_cb)** .</span><span class="sxs-lookup"><span data-stu-id="9605f-111">To participate in directory enumeration the provider must implement the **[PRJ_START_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb)**, **[PRJ_GET_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb)**, and **[PRJ_END_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_end_directory_enumeration_cb)** callbacks.</span></span>  <span data-ttu-id="9605f-112">Quando um diretório na raiz de virtualização do provedor é enumerado, o ProjFS executa as seguintes ações:</span><span class="sxs-lookup"><span data-stu-id="9605f-112">When a directory under the provider's virtualization root gets enumerated, ProjFS performs the following actions:</span></span>

1. <span data-ttu-id="9605f-113">ProjFS chama o retorno de chamada de **PRJ_START_DIRECTORY_ENUMERATION_CB** do provedor para iniciar uma sessão de enumeração.</span><span class="sxs-lookup"><span data-stu-id="9605f-113">ProjFS calls the provider's **PRJ_START_DIRECTORY_ENUMERATION_CB** callback to start an enumeration session.</span></span>

    <span data-ttu-id="9605f-114">Como parte do processamento desse retorno de chamada, o provedor deve se preparar para executar a enumeração.</span><span class="sxs-lookup"><span data-stu-id="9605f-114">As part of processing this callback the provider should prepare to perform the enumeration.</span></span>  <span data-ttu-id="9605f-115">Por exemplo, ele deve alocar qualquer memória que possa precisar acompanhar o progresso da enumeração em seu armazenamento de dados de backup.</span><span class="sxs-lookup"><span data-stu-id="9605f-115">For example, it should allocate any memory it may need to track the progress of the enumeration in its backing data store.</span></span>

    <span data-ttu-id="9605f-116">ProjFS identifica o diretório que está sendo enumerado no membro **FilePathName** do parâmetro _callbackdata_ do retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="9605f-116">ProjFS identifies the directory being enumerated in the **FilePathName** member of the callback's _callbackData_ parameter.</span></span>  <span data-ttu-id="9605f-117">Isso é especificado como um caminho relativo à raiz de virtualização.</span><span class="sxs-lookup"><span data-stu-id="9605f-117">This is specified as a path relative to the virtualization root.</span></span>  <span data-ttu-id="9605f-118">Por exemplo, se a raiz de virtualização estiver localizada em `C:\virtRoot` , e o diretório que está sendo enumerado for `C:\virtRoot\dir1\dir2` , o membro **FilePathName** conterá `dir1\dir2` .</span><span class="sxs-lookup"><span data-stu-id="9605f-118">For example, if the virtualization root is located at `C:\virtRoot`, and the directory being enumerated is `C:\virtRoot\dir1\dir2`, the **FilePathName** member will contain `dir1\dir2`.</span></span>  <span data-ttu-id="9605f-119">O provedor se preparará para enumerar esse caminho em seu armazenamento de dados de backup.</span><span class="sxs-lookup"><span data-stu-id="9605f-119">The provider will prepare to enumerate that path in its backing data store.</span></span>  <span data-ttu-id="9605f-120">Dependendo dos recursos do armazenamento de backup de um provedor, pode fazer sentido executar a enumeração de armazenamento de backup no retorno de chamada de **PRJ_START_DIRECTORY_ENUMERATION_CB** .</span><span class="sxs-lookup"><span data-stu-id="9605f-120">Depending on the capabilities of a provider's backing store it may make sense to perform the backing store enumeration in the **PRJ_START_DIRECTORY_ENUMERATION_CB** callback.</span></span>

    <span data-ttu-id="9605f-121">Como várias enumerações podem ocorrer em paralelo no mesmo diretório, cada retorno de chamada de enumeração tem um argumento _enumerationid_ para permitir que o provedor associe as invocações de retorno de chamada em uma única sessão de enumeração.</span><span class="sxs-lookup"><span data-stu-id="9605f-121">Because multiple enumerations may occur in parallel in the same directory, each enumeration callback has an _enumerationId_ argument to enable the provider to associate the callback invocations into a single enumeration session.</span></span>

    <span data-ttu-id="9605f-122">Se o provedor retornar S_OK do **PRJ_START_DIRECTORY_ENUMERATION_CB** retorno de chamada, ele deverá manter todas as informações de sessão de enumeração que ele tiver até que ProjFS invoque o retorno de chamada **PRJ_END_DIRECTORY_ENUMERATION_CB** com o mesmo valor para _enumerationid_.</span><span class="sxs-lookup"><span data-stu-id="9605f-122">If the provider returns S_OK from the **PRJ_START_DIRECTORY_ENUMERATION_CB** callback, it must maintain any enumeration session information it has until ProjFS invokes the **PRJ_END_DIRECTORY_ENUMERATION_CB** callback with the same value for _enumerationId_.</span></span>  <span data-ttu-id="9605f-123">Se o provedor retornar um erro de **PRJ_START_DIRECTORY_ENUMERATION_CB**, ProjFS não invocará o retorno de chamada **PRJ_END_DIRECTORY_ENUMERATION_CB** para essa _enumerationid_.</span><span class="sxs-lookup"><span data-stu-id="9605f-123">If the provider returns an error from **PRJ_START_DIRECTORY_ENUMERATION_CB**, ProjFS will not invoke the **PRJ_END_DIRECTORY_ENUMERATION_CB** callback for that _enumerationId_.</span></span>

1. <span data-ttu-id="9605f-124">ProjFS chama o retorno de chamada de **PRJ_GET_DIRECTORY_ENUMERATION_CB** do provedor uma ou mais vezes para obter o conteúdo do diretório do provedor.</span><span class="sxs-lookup"><span data-stu-id="9605f-124">ProjFS calls the provider's **PRJ_GET_DIRECTORY_ENUMERATION_CB** callback one or more times to get the directory contents from the provider.</span></span>

    <span data-ttu-id="9605f-125">Em resposta a esse retorno de chamada, o provedor retorna uma lista classificada de itens de seu armazenamento de dados de backup.</span><span class="sxs-lookup"><span data-stu-id="9605f-125">In response to this callback the provider returns a sorted list of items from its backing data store.</span></span>

    <span data-ttu-id="9605f-126">O retorno de chamada pode fornecer uma expressão de pesquisa em seu parâmetro _searchexception_ que o provedor usa para fazer o escopo dos resultados da enumeração.</span><span class="sxs-lookup"><span data-stu-id="9605f-126">The callback may provide a search expression in its _searchExpression_ parameter that the provider uses to scope the results of the enumeration.</span></span>  <span data-ttu-id="9605f-127">Se _searchtable_ for NULL, o provedor retornará todas as entradas no diretório que está sendo enumerado.</span><span class="sxs-lookup"><span data-stu-id="9605f-127">If _searchExpression_ is NULL, the provider returns all the entries in the directory being enumerated.</span></span>  <span data-ttu-id="9605f-128">Se não for nulo, o provedor poderá usar **[PrjDoesNameContainWildCards](/windows/win32/api/projectedfslib/nf-projectedfslib-prjdoesnamecontainwildcards)** para determinar se há curingas na expressão.</span><span class="sxs-lookup"><span data-stu-id="9605f-128">If it is non-NULL, the provider can use **[PrjDoesNameContainWildCards](/windows/win32/api/projectedfslib/nf-projectedfslib-prjdoesnamecontainwildcards)** to determine whether there are wildcards in the expression.</span></span>  <span data-ttu-id="9605f-129">Se houver, o provedor usará **[PrjFileNameMatch](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamematch)** para determinar se uma entrada no diretório corresponde à expressão de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="9605f-129">If there are, the provider uses **[PrjFileNameMatch](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamematch)** to determine whether an entry in the directory matches the search expression.</span></span>

    <span data-ttu-id="9605f-130">O provedor deve capturar o valor de _searchion_ na primeira invocação deste retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="9605f-130">The provider should capture the value of _searchExpression_ on the first invocation of this callback.</span></span>  <span data-ttu-id="9605f-131">Ele usa o valor capturado em qualquer invocação subseqüente do retorno de chamada na mesma sessão de enumeração, a menos que PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN seja definido no campo **flags** do parâmetro _callbackdata_ do retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="9605f-131">It uses the captured value on any subsequent invocation of the callback in the same enumeration session, unless PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN is set in the **Flags** field of the callback's _callbackData_ parameter.</span></span>  <span data-ttu-id="9605f-132">Nesse caso, ele deve recapturar o valor de _searchexception_.</span><span class="sxs-lookup"><span data-stu-id="9605f-132">In that case it should recapture the value of _searchExpression_.</span></span>

    <span data-ttu-id="9605f-133">Se não houver entradas correspondentes em seu repositório de backup, o provedor simplesmente retornará S_OK do retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="9605f-133">If there are no matching entries in its backing store, the provider simply returns S_OK from the callback.</span></span>  <span data-ttu-id="9605f-134">Caso contrário, o provedor formata cada entrada correspondente de seu armazenamento de backup em uma estrutura de **[PRJ_FILE_BASIC_INFO](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_file_basic_info)** e, em seguida, usa **[PrjFillDirEntryBuffer](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer)** para preencher o buffer fornecido pelo parâmetro _dirEntryBufferHandle_ do retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="9605f-134">Otherwise the provider formats each matching entry from its backing store into a **[PRJ_FILE_BASIC_INFO](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_file_basic_info)** structure, and then uses **[PrjFillDirEntryBuffer](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer)** to fill the buffer provided by the callback's _dirEntryBufferHandle_ parameter.</span></span>  <span data-ttu-id="9605f-135">O provedor continua adicionando entradas até ter adicionado todos eles ou até que **PrjFillDirEntryBuffer** retorne HRESULT_FROM_WIN32 (ERROR_INSUFFICIENT_BUFFER).</span><span class="sxs-lookup"><span data-stu-id="9605f-135">The provider keeps adding entries until it has added them all or until **PrjFillDirEntryBuffer** returns HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER).</span></span>  <span data-ttu-id="9605f-136">Em seguida, o provedor retorna S_OK do retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="9605f-136">Then the provider returns S_OK from the callback.</span></span>  <span data-ttu-id="9605f-137">Observe que o provedor deve adicionar as entradas ao buffer _dirEntryBufferHandle_ na ordem de classificação correta.</span><span class="sxs-lookup"><span data-stu-id="9605f-137">Note that the provider must add the entries to the _dirEntryBufferHandle_ buffer in the correct sort order.</span></span>  <span data-ttu-id="9605f-138">O provedor deve usar **[PrjFileNameCompare](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamecompare)** para determinar a ordem de classificação correta.</span><span class="sxs-lookup"><span data-stu-id="9605f-138">The provider should use **[PrjFileNameCompare](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamecompare)** to determine the correct sort order.</span></span>

    > <span data-ttu-id="9605f-139">O provedor deve fornecer um valor para o membro **IsDirectory** de **PRJ_FILE_BASIC_INFO**.</span><span class="sxs-lookup"><span data-stu-id="9605f-139">The provider must supply a value for the **IsDirectory** member of **PRJ_FILE_BASIC_INFO**.</span></span>  <span data-ttu-id="9605f-140">Se **IsDirectory** for false, o provedor também deverá fornecer um valor para o membro **filesize** .</span><span class="sxs-lookup"><span data-stu-id="9605f-140">If **IsDirectory** is FALSE, the provider must also supply a value for the **FileSize** member.</span></span>
    >
    > <span data-ttu-id="9605f-141">Se o provedor não fornecer valores para os membros **CreationTime**, **LastAccessTime**, **LastWriteTime** e **changetime** , ProjFS usará a hora atual do sistema.</span><span class="sxs-lookup"><span data-stu-id="9605f-141">If the provider does not supply values for the **CreationTime**, **LastAccessTime**, **LastWriteTime**, and **ChangeTime** members, ProjFS will use the current system time.</span></span>
    >
    > <span data-ttu-id="9605f-142">ProjFS usará qualquer FILE_ATTRIBUTE sinalizar os conjuntos de provedores no membro **FileAttributes** , exceto por FILE_ATTRIBUTE_DIRECTORY; ele definirá o valor correto para FILE_ATTRIBUTE_DIRECTORY no membro **FileAttributes** , de acordo com o valor fornecido do membro **IsDirectory** .</span><span class="sxs-lookup"><span data-stu-id="9605f-142">ProjFS will use whatever FILE_ATTRIBUTE flags the provider sets in the **FileAttributes** member except for FILE_ATTRIBUTE_DIRECTORY; it will set the correct value for FILE_ATTRIBUTE_DIRECTORY in the **FileAttributes** member according to the supplied value of the **IsDirectory** member.</span></span>

    <span data-ttu-id="9605f-143">Se **PrjFillDirEntryBuffer** retornar HRESULT_FROM_WIN32 (ERROR_INSUFFICIENT_BUFFER) antes que o provedor fique sem entradas para adicionar a ele, o provedor deverá manter o controle da entrada que estava tentando adicionar quando recebeu o erro.</span><span class="sxs-lookup"><span data-stu-id="9605f-143">If **PrjFillDirEntryBuffer** returns HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER) before the provider runs out of entries to add to it, the provider must keep track of the entry it was trying to add when it received the error.</span></span>  <span data-ttu-id="9605f-144">Na próxima vez que o ProjFS chamar o retorno de chamada **PRJ_GET_DIRECTORY_ENUMERATION_CB** para a mesma sessão de enumeração, o provedor deverá retomar a adição de entradas ao buffer _dirEntryBufferHandle_ com a entrada que estava tentando adicionar.</span><span class="sxs-lookup"><span data-stu-id="9605f-144">The next time ProjFS calls the **PRJ_GET_DIRECTORY_ENUMERATION_CB** callback for the same enumeration session, the provider must resume adding entries to the _dirEntryBufferHandle_ buffer with the entry it was trying to add.</span></span>

    > <span data-ttu-id="9605f-145">Se o repositório de backup der suporte a links simbólicos, o provedor deverá usar **[PrjFillDirEntryBuffer2](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer2)** para preencher o buffer fornecido pelo parâmetro _dirEntryBufferHandle_ do retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="9605f-145">If the backing store supports symbolic links, the provider must use **[PrjFillDirEntryBuffer2](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer2)** to fill the buffer provided by the callback's _dirEntryBufferHandle_ parameter.</span></span>  <span data-ttu-id="9605f-146">O **PrjFillDirEntryBuffer2** dá suporte a uma entrada de buffer extra que permite que o provedor especifique que a entrada de enumeração é um link simbólico e qual é o seu destino.</span><span class="sxs-lookup"><span data-stu-id="9605f-146">**PrjFillDirEntryBuffer2** supports an extra buffer input that allows the provider to specify that the enumeration entry is a symbolic link and what its target is.</span></span>  <span data-ttu-id="9605f-147">Caso contrário, ele se comporta conforme descrito acima para **PrjFillDirEntryBuffer**.</span><span class="sxs-lookup"><span data-stu-id="9605f-147">It otherwise behaves as described above for **PrjFillDirEntryBuffer**.</span></span>  <span data-ttu-id="9605f-148">O exemplo a seguir usa **PrjFillDirEntryBuffer2** para ilustrar o suporte para links simbólicos.</span><span class="sxs-lookup"><span data-stu-id="9605f-148">The following sample uses **PrjFillDirEntryBuffer2** to illustrate support for symbolic links.</span></span>
    >
    > <span data-ttu-id="9605f-149">Observe que o **PrjFillDirEntryBuffer2** tem suporte a partir do Windows 10, versão 2004.</span><span class="sxs-lookup"><span data-stu-id="9605f-149">Note that **PrjFillDirEntryBuffer2** is supported as of Windows 10, version 2004.</span></span>  <span data-ttu-id="9605f-150">Um provedor deve investigar a existência de **PrjFillDirEntryBuffer2**, por exemplo, usando **[GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)**.</span><span class="sxs-lookup"><span data-stu-id="9605f-150">A provider should probe for the existence of **PrjFillDirEntryBuffer2**, for instance by using **[GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)**.</span></span>

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

1. <span data-ttu-id="9605f-151">ProjFS chama o retorno de chamada de **PRJ_END_DIRECTORY_ENUMERATION_CB** do provedor para encerrar a sessão de enumeração.</span><span class="sxs-lookup"><span data-stu-id="9605f-151">ProjFS calls the provider's **PRJ_END_DIRECTORY_ENUMERATION_CB** callback to end the enumeration session.</span></span>

    <span data-ttu-id="9605f-152">O provedor deve executar qualquer limpeza que precise fazer para encerrar a sessão de enumeração, como desalocar a memória alocada como parte do **PRJ_START_DIRECTORY_ENUMERATION_CB** de processamento.</span><span class="sxs-lookup"><span data-stu-id="9605f-152">The provider should perform any cleanup it needs to do to end the enumeration session, such as deallocate memory allocated as part of processing **PRJ_START_DIRECTORY_ENUMERATION_CB**.</span></span>
