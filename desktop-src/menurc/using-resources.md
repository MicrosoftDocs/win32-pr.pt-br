---
title: Usando recursos
description: Esta seção contém código relacionado a tarefas de programação de recursos.
ms.assetid: 73678045-1518-46cd-ab55-5d272852ba73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9e4f42f908bc2ee63cfa273a5251b0bd8d9bf86
ms.sourcegitcommit: b01ad017c152c6756f3638623fe335877644d414
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/06/2021
ms.locfileid: "111549868"
---
# <a name="using-resources"></a><span data-ttu-id="98a50-103">Usando recursos</span><span class="sxs-lookup"><span data-stu-id="98a50-103">Using Resources</span></span>

<span data-ttu-id="98a50-104">Esta seção contém trechos de código para as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="98a50-104">This section contains code snippets for the following tasks:</span></span>

-   [<span data-ttu-id="98a50-105">Atualizando recursos</span><span class="sxs-lookup"><span data-stu-id="98a50-105">Updating Resources</span></span>](#updating-resources)
-   [<span data-ttu-id="98a50-106">Criando uma lista de recursos</span><span class="sxs-lookup"><span data-stu-id="98a50-106">Creating a Resource List</span></span>](#creating-a-resource-list)

## <a name="updating-resources"></a><span data-ttu-id="98a50-107">Atualizando recursos</span><span class="sxs-lookup"><span data-stu-id="98a50-107">Updating Resources</span></span>

<span data-ttu-id="98a50-108">O exemplo a seguir copia um recurso de caixa de diálogo de um arquivo executável, Hand.exe, para outro Foot.exe, seguindo estas etapas:</span><span class="sxs-lookup"><span data-stu-id="98a50-108">The following example copies a dialog box resource from one executable file, Hand.exe, to another, Foot.exe, by following these steps:</span></span>

1.  <span data-ttu-id="98a50-109">Use a função [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) para carregar o arquivo executável Hand.exe.</span><span class="sxs-lookup"><span data-stu-id="98a50-109">Use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) function to load the executable file Hand.exe.</span></span>
2.  <span data-ttu-id="98a50-110">Use as funções [**FindResource**](/windows/desktop/api/Winbase/nf-winbase-findresourcea) e [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) para localizar e carregar o recurso de caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="98a50-110">Use the [**FindResource**](/windows/desktop/api/Winbase/nf-winbase-findresourcea) and [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) functions to locate and load the dialog box resource.</span></span>
3.  <span data-ttu-id="98a50-111">Use a função [**LockResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-lockresource) para recuperar um ponteiro para os dados de recurso da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="98a50-111">Use the [**LockResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-lockresource) function to retrieve a pointer to the dialog box resource data.</span></span>
4.  <span data-ttu-id="98a50-112">Use a função [**BeginUpdateResource**](/windows/desktop/api/Winbase/nf-winbase-beginupdateresourcea) para abrir um identificador de atualização para Foot.exe.</span><span class="sxs-lookup"><span data-stu-id="98a50-112">Use the [**BeginUpdateResource**](/windows/desktop/api/Winbase/nf-winbase-beginupdateresourcea) function to open an update handle to Foot.exe.</span></span>
5.  <span data-ttu-id="98a50-113">Use a função [**UpdateResource**](/windows/desktop/api/Winbase/nf-winbase-updateresourcea) para copiar o recurso da caixa de diálogo de Hand.exe para Foot.exe.</span><span class="sxs-lookup"><span data-stu-id="98a50-113">Use the [**UpdateResource**](/windows/desktop/api/Winbase/nf-winbase-updateresourcea) function to copy the dialog box resource from Hand.exe to Foot.exe.</span></span>
6.  <span data-ttu-id="98a50-114">Use a função [**EndUpdateResource**](/windows/desktop/api/Winbase/nf-winbase-endupdateresourcea) para concluir a atualização.</span><span class="sxs-lookup"><span data-stu-id="98a50-114">Use the [**EndUpdateResource**](/windows/desktop/api/Winbase/nf-winbase-endupdateresourcea) function to complete the update.</span></span>

<span data-ttu-id="98a50-115">O código a seguir implementa essas etapas.</span><span class="sxs-lookup"><span data-stu-id="98a50-115">The following code implements these steps.</span></span>

<span data-ttu-id="98a50-116">**Aviso de segurança:** O uso incorreto de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) pode comprometer a segurança do seu aplicativo carregando a dll errada.</span><span class="sxs-lookup"><span data-stu-id="98a50-116">**Security Warning:** Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="98a50-117">Consulte a documentação de **LoadLibrary** para obter informações sobre como carregar DLLs corretamente com diferentes versões do Windows.</span><span class="sxs-lookup"><span data-stu-id="98a50-117">Refer to the **LoadLibrary** documentation for information on how to correctly load DLLs with different versions of Windows.</span></span>


```C++
HGLOBAL hResLoad;   // handle to loaded resource
HMODULE hExe;       // handle to existing .EXE file
HRSRC hRes;         // handle/ptr. to res. info. in hExe
HANDLE hUpdateRes;  // update resource handle
LPVOID lpResLock;   // pointer to resource data
BOOL result;
#define IDD_HAND_ABOUTBOX   103
#define IDD_FOOT_ABOUTBOX   110

// Load the .EXE file that contains the dialog box you want to copy.
hExe = LoadLibrary(TEXT("hand.exe"));
if (hExe == NULL)
{
    ErrorHandler(TEXT("Could not load exe."));
    return;
}

// Locate the dialog box resource in the .EXE file.
hRes = FindResource(hExe, MAKEINTRESOURCE(IDD_HAND_ABOUTBOX), RT_DIALOG);
if (hRes == NULL)
{
    ErrorHandler(TEXT("Could not locate dialog box."));
    return;
}

// Load the dialog box into global memory.
hResLoad = LoadResource(hExe, hRes);
if (hResLoad == NULL)
{
    ErrorHandler(TEXT("Could not load dialog box."));
    return;
}

// Lock the dialog box into global memory.
lpResLock = LockResource(hResLoad);
if (lpResLock == NULL)
{
    ErrorHandler(TEXT("Could not lock dialog box."));
    return;
}

// Open the file to which you want to add the dialog box resource.
hUpdateRes = BeginUpdateResource(TEXT("foot.exe"), FALSE);
if (hUpdateRes == NULL)
{
    ErrorHandler(TEXT("Could not open file for writing."));
    return;
}

// Add the dialog box resource to the update list.
result = UpdateResource(hUpdateRes,    // update resource handle
    RT_DIALOG,                         // change dialog box resource
    MAKEINTRESOURCE(IDD_FOOT_ABOUTBOX),         // dialog box id
    MAKELANGID(LANG_NEUTRAL, SUBLANG_NEUTRAL),  // neutral language
    lpResLock,                         // ptr to resource info
    SizeofResource(hExe, hRes));       // size of resource info

if (result == FALSE)
{
    ErrorHandler(TEXT("Could not add resource."));
    return;
}

// Write changes to FOOT.EXE and then close it.
if (!EndUpdateResource(hUpdateRes, FALSE))
{
    ErrorHandler(TEXT("Could not write changes to file."));
    return;
}

// Clean up.
if (!FreeLibrary(hExe))
{
    ErrorHandler(TEXT("Could not free executable."));
    return;
}
```



## <a name="creating-a-resource-list"></a><span data-ttu-id="98a50-118">Criando uma lista de recursos</span><span class="sxs-lookup"><span data-stu-id="98a50-118">Creating a Resource List</span></span>

<span data-ttu-id="98a50-119">O exemplo a seguir cria uma lista de todos os recursos no arquivo de Hand.exe.</span><span class="sxs-lookup"><span data-stu-id="98a50-119">The following example creates a list of every resource in the Hand.exe file.</span></span> <span data-ttu-id="98a50-120">A lista é gravada no arquivo de Resinfo.txt.</span><span class="sxs-lookup"><span data-stu-id="98a50-120">The list is written to the Resinfo.txt file.</span></span>

<span data-ttu-id="98a50-121">O código demonstra como carregar o arquivo executável, criar um arquivo no qual gravar informações de recursos e chamar a função [**EnumResourceTypes**](/windows/desktop/api/Winbase/nf-winbase-enumresourcetypesa) para enviar cada tipo de recurso encontrado no módulo para a função de retorno de chamada definida pelo aplicativo `EnumTypesFunc` .</span><span class="sxs-lookup"><span data-stu-id="98a50-121">The code demonstrates how to load the executable file, create a file in which to write resource information, and call the [**EnumResourceTypes**](/windows/desktop/api/Winbase/nf-winbase-enumresourcetypesa) function to send each resource type found in the module to the application-defined callback function `EnumTypesFunc`.</span></span> <span data-ttu-id="98a50-122">Consulte [*EnumResTypeProc*](/windows/win32/api/libloaderapi/nc-libloaderapi-enumrestypeproca) para obter informações sobre as funções de retorno de chamada desse tipo.</span><span class="sxs-lookup"><span data-stu-id="98a50-122">See [*EnumResTypeProc*](/windows/win32/api/libloaderapi/nc-libloaderapi-enumrestypeproca) for information on callback functions of this type.</span></span> <span data-ttu-id="98a50-123">Essa função de retorno de chamada usa a função [**EnumResourceNames**](/windows/desktop/api/libloaderapi/nf-libloaderapi-enumresourcenamesa) para passar o nome de cada recurso dentro do tipo especificado para outra função de retorno de chamada definida pelo aplicativo, `EnumNamesFunc` .</span><span class="sxs-lookup"><span data-stu-id="98a50-123">This callback function uses the [**EnumResourceNames**](/windows/desktop/api/libloaderapi/nf-libloaderapi-enumresourcenamesa) function to pass the name of every resource within the specified type to another application-defined callback function, `EnumNamesFunc`.</span></span> <span data-ttu-id="98a50-124">Consulte [*EnumResNameProc*](/windows/win32/api/libloaderapi/nc-libloaderapi-enumresnameproca) para obter informações sobre as funções de retorno de chamada desse tipo.</span><span class="sxs-lookup"><span data-stu-id="98a50-124">See [*EnumResNameProc*](/windows/win32/api/libloaderapi/nc-libloaderapi-enumresnameproca) for information on callback functions of this type.</span></span> <span data-ttu-id="98a50-125">`EnumNamesFunc` usa a função [**EnumResourceLanguages**](/windows/desktop/api/Winbase/nf-winbase-enumresourcelanguagesa) para passar o idioma de cada recurso do tipo e do nome especificados para uma terceira função de retorno de chamada, `EnumLangsFunc` .</span><span class="sxs-lookup"><span data-stu-id="98a50-125">`EnumNamesFunc` uses the [**EnumResourceLanguages**](/windows/desktop/api/Winbase/nf-winbase-enumresourcelanguagesa) function to pass the language of every resource of the specified type and name to a third callback function, `EnumLangsFunc`.</span></span> <span data-ttu-id="98a50-126">Consulte [*EnumResLangProc*](/previous-versions/windows/desktop/legacy/ms648033(v=vs.85)) para obter informações sobre as funções de retorno de chamada desse tipo.</span><span class="sxs-lookup"><span data-stu-id="98a50-126">See [*EnumResLangProc*](/previous-versions/windows/desktop/legacy/ms648033(v=vs.85)) for information on callback functions of this type.</span></span> <span data-ttu-id="98a50-127">`EnumLangsFunc` grava informações sobre o recurso do tipo, nome e idioma especificados no arquivo de Resinfo.txt.</span><span class="sxs-lookup"><span data-stu-id="98a50-127">`EnumLangsFunc` writes information about the resource of the specified type, name, and language to the Resinfo.txt file.</span></span>

<span data-ttu-id="98a50-128">Observe que *lpszType* em [*ENUMRESTYPEPROC*](/windows/win32/api/libloaderapi/nc-libloaderapi-enumrestypeproca) é uma ID de recurso ou um ponteiro para uma cadeia de caracteres (que contém uma ID de recurso ou nome de tipo); *lpszType* e *lpszName* em [*EnumResNameProc*](/windows/win32/api/libloaderapi/nc-libloaderapi-enumresnameproca) e [*EnumResLangProc*](/previous-versions/windows/desktop/legacy/ms648033(v=vs.85)) são semelhantes.</span><span class="sxs-lookup"><span data-stu-id="98a50-128">Note that the *lpszType* in [*EnumResTypeProc*](/windows/win32/api/libloaderapi/nc-libloaderapi-enumrestypeproca) is either a resource ID or a pointer to a string (containing a resource ID or type name); *lpszType* and *lpszName* in [*EnumResNameProc*](/windows/win32/api/libloaderapi/nc-libloaderapi-enumresnameproca) and [*EnumResLangProc*](/previous-versions/windows/desktop/legacy/ms648033(v=vs.85)) are similar.</span></span> <span data-ttu-id="98a50-129">Para carregar um recurso enumerado, basta chamar a função apropriada.</span><span class="sxs-lookup"><span data-stu-id="98a50-129">To load an enumerated resource, just call the appropriate function.</span></span> <span data-ttu-id="98a50-130">Por exemplo, se um recurso de menu **( \_ menu RT**) tiver sido enumerado, passe *lpszName* para [**LoadMenu**](/windows/desktop/api/Winuser/nf-winuser-loadmenua).</span><span class="sxs-lookup"><span data-stu-id="98a50-130">For example, if a menu resource (**RT\_MENU**) was enumerated, then pass *lpszName* to [**LoadMenu**](/windows/desktop/api/Winuser/nf-winuser-loadmenua).</span></span> <span data-ttu-id="98a50-131">Para recursos personalizados, passe *lpszType* e *lpszName* para [**FindResource**](/windows/desktop/api/Winbase/nf-winbase-findresourcea).</span><span class="sxs-lookup"><span data-stu-id="98a50-131">For custom resources, pass *lpszType* and *lpszName* to [**FindResource**](/windows/desktop/api/Winbase/nf-winbase-findresourcea).</span></span>

<span data-ttu-id="98a50-132">O código de [recursos de atualização](#updating-resources) segue um padrão semelhante para um recurso de caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="98a50-132">The [Updating Resources](#updating-resources) code follows a similar pattern for a dialog box resource.</span></span>

<span data-ttu-id="98a50-133">**Aviso de segurança:** O uso incorreto de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) pode comprometer a segurança do seu aplicativo carregando a dll errada.</span><span class="sxs-lookup"><span data-stu-id="98a50-133">**Security Warning:** Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="98a50-134">Consulte a documentação de **LoadLibrary** para obter informações sobre como carregar DLLs corretamente com diferentes versões do Windows.</span><span class="sxs-lookup"><span data-stu-id="98a50-134">Refer to the **LoadLibrary** documentation for information on how to correctly load DLLs with different versions of Windows.</span></span>


```C++
HANDLE g_hFile;   // global handle to resource info file
// Declare callback functions.
BOOL EnumTypesFunc(
       HMODULE hModule,
       LPTSTR lpType,
       LONG lParam);
   
BOOL EnumNamesFunc(
       HMODULE hModule,
       LPCTSTR lpType,
       LPTSTR lpName,
       LONG lParam);
   
BOOL EnumLangsFunc(
       HMODULE hModule,
       LPCTSTR lpType,
       LPCTSTR lpName,
       WORD wLang,
       LONG lParam);
```




```C++
HMODULE hExe;        // handle to .EXE file
TCHAR szBuffer[80];  // print buffer for info file
DWORD cbWritten;     // number of bytes written to resource info file
size_t cbString;     // length of string in szBuffer
HRESULT hResult;

// Load the .EXE whose resources you want to list.
hExe = LoadLibrary(TEXT("hand.exe"));
if (hExe == NULL)
{
    // Add code to fail as securely as possible.
    return;
}

// Create a file to contain the resource info.
g_hFile = CreateFile(TEXT("resinfo.txt"),   // name of file
    GENERIC_READ | GENERIC_WRITE,      // access mode
    0,                                 // share mode
    (LPSECURITY_ATTRIBUTES) NULL,      // default security
    CREATE_ALWAYS,                     // create flags
    FILE_ATTRIBUTE_NORMAL,             // file attributes
    (HANDLE) NULL);                    // no template
if (g_hFile == INVALID_HANDLE_VALUE)
{
    ErrorHandler(TEXT("Could not open file."));
    return;
}

// Find all of the loaded file's resources.
hResult = StringCchPrintf(szBuffer, sizeof(szBuffer)/sizeof(TCHAR),
    TEXT("The file contains the following resources:\r\n\r\n"));
if (FAILED(hResult))
{
    // Add code to fail as securely as possible.
    return;
}

hResult = StringCchLength(szBuffer, sizeof(szBuffer)/sizeof(TCHAR), &cbString);
if (FAILED(hResult))
{
    // Add code to fail as securely as possible.
    return;
}

WriteFile(g_hFile,       // file to hold resource info
    szBuffer,            // what to write to the file
    (DWORD) cbString,    // number of bytes in szBuffer
    &cbWritten,          // number of bytes written
    NULL);               // no overlapped I/O

EnumResourceTypes(hExe,              // module handle
    (ENUMRESTYPEPROC)EnumTypesFunc,  // callback function
    0);                              // extra parameter

// Unload the executable file whose resources were
// enumerated and close the file created to contain
// the resource information.
FreeLibrary(hExe);
CloseHandle(g_hFile);
```




```C++
//    FUNCTION: EnumTypesFunc(HANDLE, LPSTR, LONG)
//
//    PURPOSE:  Resource type callback
BOOL EnumTypesFunc(
        HMODULE hModule,  // module handle
        LPTSTR lpType,    // address of resource type
        LONG lParam)      // extra parameter, could be
                          // used for error checking
{
    TCHAR szBuffer[80];  // print buffer for info file
    DWORD cbWritten;     // number of bytes written to resource info file
    size_t cbString;
    HRESULT hResult;

    // Write the resource type to a resource information file.
    // The type may be a string or an unsigned decimal
    // integer, so test before printing.
    if (!IS_INTRESOURCE(lpType))
    {
        hResult = StringCchPrintf(szBuffer, sizeof(szBuffer)/sizeof(TCHAR), TEXT("Type: %s\r\n"), lpType);
        if (FAILED(hResult))
        {
            // Add code to fail as securely as possible.
            return FALSE;
        }
    }
    else
    {
        hResult = StringCchPrintf(szBuffer, sizeof(szBuffer)/sizeof(TCHAR), TEXT("Type: %u\r\n"), (USHORT)lpType);
        if (FAILED(hResult))
        {
            // Add code to fail as securely as possible.
            return FALSE;
        }
    }

    hResult = StringCchLength(szBuffer, sizeof(szBuffer)/sizeof(TCHAR), &cbString);
    if (FAILED(hResult))
    {
        // Add code to fail as securely as possible.
        return FALSE;
    }

    WriteFile(g_hFile, szBuffer, (DWORD) cbString, &cbWritten, NULL);
    // Find the names of all resources of type lpType.
    EnumResourceNames(hModule,
        lpType,
        (ENUMRESNAMEPROC)EnumNamesFunc,
        0);

    return TRUE;
}

//    FUNCTION: EnumNamesFunc(HANDLE, LPSTR, LPSTR, LONG)
//
//    PURPOSE:  Resource name callback
BOOL EnumNamesFunc(
        HMODULE hModule,  // module handle
        LPCTSTR lpType,   // address of resource type
        LPTSTR lpName,    // address of resource name
        LONG lParam)      // extra parameter, could be
                          // used for error checking
{
    TCHAR szBuffer[80];  // print buffer for info file
    DWORD cbWritten;     // number of bytes written to resource info file
    size_t cbString;
    HRESULT hResult;

    // Write the resource name to a resource information file.
    // The name may be a string or an unsigned decimal
    // integer, so test before printing.
    if (!IS_INTRESOURCE(lpName))
    {
        hResult = StringCchPrintf(szBuffer, sizeof(szBuffer)/sizeof(TCHAR), TEXT("\tName: %s\r\n"), lpName);
        if (FAILED(hResult))
        {
            // Add code to fail as securely as possible.
            return FALSE;
        }
    }
    else
    {
        hResult = StringCchPrintf(szBuffer, sizeof(szBuffer)/sizeof(TCHAR), TEXT("\tName: %u\r\n"), (USHORT)lpName);
        if (FAILED(hResult))
        {
            // Add code to fail as securely as possible.
            return FALSE;
        }
    }

    hResult = StringCchLength(szBuffer, sizeof(szBuffer)/sizeof(TCHAR), &cbString);
    if (FAILED(hResult))
    {
        // Add code to fail as securely as possible.
        return FALSE;
    }
   
    WriteFile(g_hFile, szBuffer, (DWORD) cbString, &cbWritten, NULL);
    // Find the languages of all resources of type
    // lpType and name lpName.
    EnumResourceLanguages(hModule,
        lpType,
        lpName,
        (ENUMRESLANGPROC)EnumLangsFunc,
        0);

    return TRUE;
}

//    FUNCTION: EnumLangsFunc(HANDLE, LPSTR, LPSTR, WORD, LONG)
//
//    PURPOSE:  Resource language callback
BOOL EnumLangsFunc(
        HMODULE hModule, // module handle
        LPCTSTR lpType,  // address of resource type
        LPCTSTR lpName,  // address of resource name
        WORD wLang,      // resource language
        LONG lParam)     // extra parameter, could be
                         // used for error checking
{
    HRSRC hResInfo;
    TCHAR szBuffer[80];  // print buffer for info file
    DWORD cbWritten;     // number of bytes written to resource info file
    size_t cbString;
    HRESULT hResult;

    hResInfo = FindResourceEx(hModule, lpType, lpName, wLang);
    // Write the resource language to the resource information file.
    hResult = StringCchPrintf(szBuffer, sizeof(szBuffer)/sizeof(TCHAR), TEXT("\t\tLanguage: %u\r\n"), (USHORT) wLang);
    if (FAILED(hResult))
    {
        // Add code to fail as securely as possible.
        return FALSE;
    }

    hResult = StringCchLength(szBuffer, sizeof(szBuffer)/sizeof(TCHAR), &cbString);
    if (FAILED(hResult))
    {
        // Add code to fail as securely as possible.
        return FALSE;
    }

    WriteFile(g_hFile, szBuffer, (DWORD) cbString, &cbWritten, NULL); 
    // Write the resource handle and size to buffer.
    hResult = StringCchPrintf(szBuffer,
        sizeof(szBuffer)/sizeof(TCHAR),
        TEXT("\t\thResInfo == %lx,  Size == %lu\r\n\r\n"),
        hResInfo,
        SizeofResource(hModule, hResInfo));
    if (FAILED(hResult))
    {
        // Add code to fail as securely as possible.
        return FALSE;
    }

    hResult = StringCchLength(szBuffer, sizeof(szBuffer)/sizeof(TCHAR), &cbString);
    if (FAILED(hResult))
    {
        // Add code to fail as securely as possible.
        return FALSE;
    }

    WriteFile(g_hFile, szBuffer, (DWORD)cbString, &cbWritten, NULL);
    return TRUE;
}
```



 

 