---
title: Gerenciamento de dados
description: Este tópico discute como os objetos de memória passam dados de um aplicativo para outro.
ms.assetid: 32919f27-4699-4831-8837-c5160b1daf4e
keywords:
- Interface do usuário do Windows, troca dinâmica de dados (DDE)
- Troca dinâmica de dados (DDE), gerenciamento de dados
- DDE (troca dinâmica de dados), gerenciamento de dados
- troca de dados, troca dinâmica de dados (DDE)
- Interface do usuário do Windows, biblioteca de gerenciamento de troca dinâmica de dados (DDEML)
- DDEML (biblioteca de gerenciamento de troca dinâmica de dados), gerenciamento de dados
- DDEML (biblioteca de gerenciamento de troca dinâmica de dados), gerenciamento de dados
- Data Exchange, biblioteca de gerenciamento de troca dinâmica de dados (DDEML)
- Troca dinâmica de dados (DDE), objetos
- DDE (troca dinâmica de dados), objetos
- DDEML (biblioteca de gerenciamento de troca dinâmica de dados), objetos
- DDEML (troca dinâmica de dados biblioteca de gerenciamento), objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc5178f636cf4b75111d4fc48e17fd144400a91
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364460"
---
# <a name="data-management"></a><span data-ttu-id="4dde8-115">Gerenciamento de dados</span><span class="sxs-lookup"><span data-stu-id="4dde8-115">Data Management</span></span>

<span data-ttu-id="4dde8-116">Como troca dinâmica de dados (DDE) usa objetos de memória para passar dados de um aplicativo para outro, a troca dinâmica de dados biblioteca de gerenciamento (DDEML) fornece um conjunto de funções que os aplicativos DDE podem usar para criar e gerenciar objetos DDE.</span><span class="sxs-lookup"><span data-stu-id="4dde8-116">Because Dynamic Data Exchange (DDE) uses memory objects to pass data from one application to another, the Dynamic Data Exchange Management Library (DDEML) provides a set of functions that DDE applications can use to create and manage DDE objects.</span></span>

<span data-ttu-id="4dde8-117">Todas as transações que envolvem a troca de dados exigem que o aplicativo forneça os dados para criar um buffer local contendo os dados e, em seguida, chamar a função [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) .</span><span class="sxs-lookup"><span data-stu-id="4dde8-117">All transactions that involve the exchange of data require the application supplying the data to create a local buffer containing the data and then to call the [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) function.</span></span> <span data-ttu-id="4dde8-118">Essa função aloca um objeto DDE, copia os dados do buffer para o objeto e retorna um identificador de dados.</span><span class="sxs-lookup"><span data-stu-id="4dde8-118">This function allocates a DDE object, copies the data from the buffer to the object, and returns a data handle.</span></span> <span data-ttu-id="4dde8-119">Um identificador de dados é um valor **DWORD** que o ddeml usa para fornecer acesso aos dados no objeto DDE.</span><span class="sxs-lookup"><span data-stu-id="4dde8-119">A data handle is a **DWORD** value that the DDEML uses to provide access to data in the DDE object.</span></span> <span data-ttu-id="4dde8-120">Para compartilhar os dados em um objeto DDE, um aplicativo passa o identificador de dados para o DDEML, e o DDEML passa o identificador para a função de retorno de chamada DDE do aplicativo que está recebendo a transação de dados.</span><span class="sxs-lookup"><span data-stu-id="4dde8-120">To share the data in a DDE object, an application passes the data handle to the DDEML, and the DDEML passes the handle to the DDE callback function of the application that is receiving the data transaction.</span></span>

<span data-ttu-id="4dde8-121">O exemplo a seguir mostra como criar um objeto DDE e obter um identificador para o objeto.</span><span class="sxs-lookup"><span data-stu-id="4dde8-121">The following example shows how to create a DDE object and obtain a handle to the object.</span></span> <span data-ttu-id="4dde8-122">Durante a transação [**XTYP \_ ADVREQ**](xtyp-advreq.md) , a função de retorno de chamada converte a hora atual em uma cadeia de caracteres ASCII, copia a cadeia de caracteres em um buffer local e, em seguida, cria um objeto DDE que contém a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="4dde8-122">During the [**XTYP\_ADVREQ**](xtyp-advreq.md) transaction, the callback function converts the current time to an ASCII string, copies the string to a local buffer, and then creates a DDE object that contains the string.</span></span> <span data-ttu-id="4dde8-123">A função de retorno de chamada retorna o identificador para o objeto DDE (HDDEDATA) para o DDEML, que passa o identificador para o aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="4dde8-123">The callback function returns the handle to the DDE object (HDDEDATA) to the DDEML, which passes the handle to the client application.</span></span>


```
typedef struct tagTIME 
{ 
    INT     hour;   // 0 - 11 hours for analog clock 
    INT     hour12; // 12-hour format 
    INT     hour24; // 24-hour format 
    INT     minute; 
    INT     second; 
    INT     ampm;   // 0 - AM , 1 - PM 
} TIME; 
 
HDDEDATA EXPENTRY DdeCallback(uType, uFmt, hconv, hsz1, hsz2, 
    hdata, dwData1, dwData2) 
UINT uType; 
UINT uFmt; 
HCONV hconv; 
HSZ hsz1; 
HSZ hsz2; 
HDDEDATA hdata; 
DWORD dwData1; 
DWORD dwData2; 
{ 
 
    CHAR szBuf[32];
    HRESULT hResult;
    size_t * pcch;
    HRESULT hResult; 
 
    switch (uType) 
    { 
    case XTYP_ADVREQ: 
        if ((hsz1 == hszTime && hsz2 == hszNow) && 
                (uFmt == CF_TEXT)) 
        { 
            // Copy the formatted string to a buffer. 
 
            itoa(tmTime.hour, szBuf, 10);
            hResult = StringCchCat(szBuf, 32/sizeof(TCHAR), ":"); 
            if (FAILED(hResult))
            {
            // TO DO: Write error handler.
                return;
            }
            if (tmTime.minute < 10)
                hResult = StringCchCat(szBuf, 32/sizeof(TCHAR), "0"); 
                if (FAILED(hResult)
            {
            // TO DO: Write error handler.
                return;
            } 
            hResult = StringCchLength(szBuf, 32/sizeof(TCHAR), pcch);
            if (FAILED(hResult))
            {
            // TO DO: Write error handler.
                return;
            }
            itoa(tmTime.minute, &szBuf[*pcch], 10);
            hResult = StringCchCat(szBuf, 32/sizeof(TCHAR), ":"); 
            if (FAILED(hResult)
            {
            // TO DO: Write error handler.
                return;
            }
            if (tmTime.second < 10) 
                hResult = StringCchCat(szBuf, 32/sizeof(TCHAR), "0"); 
            if (FAILED(hResult)
            {
            // TO DO: Write error handler.
                return;
            }
            hResult = StringCchLength(szBuf, 32/sizeof(TCHAR), pcch);
            if (FAILED(hResult))
            {
            // TO DO: Write error handler.
                return;
            }
            itoa(tmTime.second, &szBuf[*pcch], 10);
            hResult = StringCchLength(szBuf, 32/sizeof(TCHAR), pcch);
            if (FAILED(hResult))
            {
            // TO DO: Write error handler.
                return;
            } 
            szBuf[*pcch] = '\0'; 
 
            // Create a global object and return its data handle. 
            hResult = StringCchLength(szBuf, 32/sizeof(TCHAR), pcch);
            if (FAILED(hResult))
            {
            // TO DO: Write error handler.
                return;
            }
            return (DdeCreateDataHandle( 
                idInst, 
                (LPBYTE) szBuf,     // instance identifier 
                *pcch + 1,          // source buffer length 
                0,                  // offset from beginning 
                hszNow,             // item name string 
                CF_TEXT,            // clipboard format 
                0));                // no creation flags 
        } else return (HDDEDATA) NULL; 
 
    // Process other transactions. 
    } 
} 
```



<span data-ttu-id="4dde8-124">O aplicativo receptor Obtém um ponteiro para o objeto DDE passando o identificador de dados para a função [**DdeAccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata) .</span><span class="sxs-lookup"><span data-stu-id="4dde8-124">The receiving application obtains a pointer to the DDE object by passing the data handle to the [**DdeAccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata) function.</span></span> <span data-ttu-id="4dde8-125">O ponteiro retornado por **DdeAccessData** fornece acesso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="4dde8-125">The pointer returned by **DdeAccessData** provides read-only access.</span></span> <span data-ttu-id="4dde8-126">O aplicativo deve usar o ponteiro para revisar os dados e, em seguida, chamar a função [**DdeUnaccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeunaccessdata) para invalidar o ponteiro.</span><span class="sxs-lookup"><span data-stu-id="4dde8-126">The application should use the pointer to review the data and then call the [**DdeUnaccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeunaccessdata) function to invalidate the pointer.</span></span> <span data-ttu-id="4dde8-127">O aplicativo pode copiar os dados para um buffer local usando a função [**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) .</span><span class="sxs-lookup"><span data-stu-id="4dde8-127">The application can copy the data to a local buffer by using the [**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) function.</span></span>

<span data-ttu-id="4dde8-128">O exemplo a seguir obtém um ponteiro para o objeto DDE identificado pelo parâmetro *hData* , copia o conteúdo para um buffer local e, em seguida, invalida o ponteiro.</span><span class="sxs-lookup"><span data-stu-id="4dde8-128">The following example obtains a pointer to the DDE object identified by the *hData* parameter, copies the contents to a local buffer, and then invalidates the pointer.</span></span>


```
HDDEDATA hdata; 
LPBYTE lpszAdviseData; 
DWORD cbDataLen; 
DWORD i; 
char szData[32]; 
 
// 
case XTYP_ADVDATA: 
    lpszAdviseData = DdeAccessData(hdata, &cbDataLen); 
    for (i = 0; i < cbDataLen; i++) 
        szData[i] = *lpszAdviseData++; 
    DdeUnaccessData(hdata); 
    return (HDDEDATA) TRUE; 
//
```



<span data-ttu-id="4dde8-129">Normalmente, quando um aplicativo que criou um identificador de dados passa esse identificador para o DDEML, o identificador torna-se inválido no aplicativo de criação.</span><span class="sxs-lookup"><span data-stu-id="4dde8-129">Usually, when an application that created a data handle passes that handle to the DDEML, the handle becomes invalid in the creating application.</span></span> <span data-ttu-id="4dde8-130">Essa situação não será um problema se o aplicativo precisar compartilhar dados com apenas um único aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4dde8-130">This situation is not a problem if the application must share data with only a single application.</span></span> <span data-ttu-id="4dde8-131">Se um aplicativo precisar compartilhar os mesmos dados com vários aplicativos, no entanto, o aplicativo de criação deverá especificar o \_ sinalizador HDATA APPOWNED no [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle).</span><span class="sxs-lookup"><span data-stu-id="4dde8-131">If an application must share the same data with multiple applications, however, the creating application should specify the HDATA\_APPOWNED flag in [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle).</span></span> <span data-ttu-id="4dde8-132">Isso fornece a propriedade do objeto DDE para o aplicativo de criação e impede que o DDEML invalide o identificador de dados.</span><span class="sxs-lookup"><span data-stu-id="4dde8-132">Doing so gives ownership of the DDE object to the creating application and prevents the DDEML from invalidating the data handle.</span></span> <span data-ttu-id="4dde8-133">O aplicativo pode passar o identificador de dados a qualquer número de vezes depois de chamar **DdeCreateDataHandle** apenas uma vez.</span><span class="sxs-lookup"><span data-stu-id="4dde8-133">The application can then pass the data handle any number of times after calling **DdeCreateDataHandle** only once.</span></span>

<span data-ttu-id="4dde8-134">Se um aplicativo especificar o \_ sinalizador HDATA APPOWNED no parâmetro *AfCmd* de [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle), ele deverá chamar a função [**DdeFreeDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddefreedatahandle) para liberar o identificador de memória, independentemente de ter passado o identificador para o ddeml.</span><span class="sxs-lookup"><span data-stu-id="4dde8-134">If an application specifies the HDATA\_APPOWNED flag in the *afCmd* parameter of [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle), it must call the [**DdeFreeDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddefreedatahandle) function to free the memory handle, regardless of whether it passed the handle to the DDEML.</span></span> <span data-ttu-id="4dde8-135">Antes de ser encerrado, um aplicativo deve chamar **DdeFreeDataHandle** para liberar qualquer identificador de dados que ele criou, mas não passou para o ddeml.</span><span class="sxs-lookup"><span data-stu-id="4dde8-135">Before it terminates, an application must call **DdeFreeDataHandle** to free any data handle that it created but did not pass to the DDEML.</span></span>

<span data-ttu-id="4dde8-136">Um aplicativo que ainda não passou o identificador para um objeto DDE para o DDEML pode adicionar dados ao objeto ou substituir dados no objeto usando a função [**DdeAddData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeadddata) .</span><span class="sxs-lookup"><span data-stu-id="4dde8-136">An application that has not yet passed the handle to a DDE object to the DDEML can add data to the object or overwrite data in the object by using the [**DdeAddData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeadddata) function.</span></span> <span data-ttu-id="4dde8-137">Normalmente, um aplicativo usa **DdeAddData** para preencher um objeto DDE não inicializado.</span><span class="sxs-lookup"><span data-stu-id="4dde8-137">Typically, an application uses **DdeAddData** to fill an uninitialized DDE object.</span></span> <span data-ttu-id="4dde8-138">Depois que um aplicativo passa um identificador de dados para o DDEML, o objeto DDE identificado pelo identificador não pode ser alterado; Ele só pode ser liberado.</span><span class="sxs-lookup"><span data-stu-id="4dde8-138">After an application passes a data handle to the DDEML, the DDE object identified by the handle cannot be changed; it can only be freed.</span></span>

 

 




