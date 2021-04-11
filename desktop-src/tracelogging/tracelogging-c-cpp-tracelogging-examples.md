---
title: Exemplos de Tracelogging C/C++
description: Este tópico contém exemplos de Tracelogging C/C++.
ms.assetid: FB0A29B9-D1F7-4F13-AA75-5963A0699F7A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 727aa0f46abb9dcffa1d71dac0880c401003cff5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363871"
---
# <a name="cc-tracelogging-examples"></a><span data-ttu-id="ed7fe-103">Exemplos de Tracelogging C/C++</span><span class="sxs-lookup"><span data-stu-id="ed7fe-103">C/C++ Tracelogging Examples</span></span>

<span data-ttu-id="ed7fe-104">Este tópico contém exemplos de Tracelogging C/C++.</span><span class="sxs-lookup"><span data-stu-id="ed7fe-104">This topic contains C/C++ Tracelogging examples.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ed7fe-105">Vincule advapi32. lib ao compilar esses exemplos.</span><span class="sxs-lookup"><span data-stu-id="ed7fe-105">Link advapi32.lib when compiling these examples.</span></span>

 

-   [<span data-ttu-id="ed7fe-106">Tipos de dados intrínsecos de log</span><span class="sxs-lookup"><span data-stu-id="ed7fe-106">Log intrinsic data types</span></span>](#log-intrinsic-data-types)
-   [<span data-ttu-id="ed7fe-107">Campos de evento de nome</span><span class="sxs-lookup"><span data-stu-id="ed7fe-107">Name event fields</span></span>](#name-event-fields)
-   [<span data-ttu-id="ed7fe-108">Nível de detalhes de eventos de log</span><span class="sxs-lookup"><span data-stu-id="ed7fe-108">Log events verbosity level</span></span>](#log-event-verbosity-level)
-   [<span data-ttu-id="ed7fe-109">Palavras-chave de eventos de log</span><span class="sxs-lookup"><span data-stu-id="ed7fe-109">Log events keywords</span></span>](#log-event-keywords)
-   [<span data-ttu-id="ed7fe-110">Dados de evento de matriz de log</span><span class="sxs-lookup"><span data-stu-id="ed7fe-110">Log array event data</span></span>](#log-array-event-data)
-   [<span data-ttu-id="ed7fe-111">Dados de evento de estrutura de log</span><span class="sxs-lookup"><span data-stu-id="ed7fe-111">Log structure event data</span></span>](#log-structure-event-data)

### <a name="log-intrinsic-data-types"></a><span data-ttu-id="ed7fe-112">Tipos de dados intrínsecos de log</span><span class="sxs-lookup"><span data-stu-id="ed7fe-112">Log intrinsic data types</span></span>

<span data-ttu-id="ed7fe-113">Este exemplo mostra como registrar em log os tipos de dados intrínsecos, como inteiros, Boolianos e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="ed7fe-113">This example shows how to log intrinsic data types such as integers, booleans, and so on.</span></span>


```C++
void TraceLoggingSample::BasicDataTypes()
{
    UINT8 u8 = 200;
    INT32 i32 = -2000000000;
    UINT32 u32 = 4000000000;
    INT64 i64 = 9000000000000000000;
    float f32 = 3.14f;
    BOOL b = TRUE;
    bool bcpp = true;

    /*
    The following four "NumericValues" events are equivalent (except where noted) ...
    */

    TraceLoggingWrite(
        g_hMyComponentProvider,
        "NumericValues",
        TraceLoggingUInt8(u8, "UINT8"),
        TraceLoggingInt32(i32, "INT32"),
        TraceLoggingUInt32(u32, "UINT32"),
        TraceLoggingHexUInt32(u32, "UINT32"),
        TraceLoggingInt64(i64, "INT64"),
        TraceLoggingFloat32(f32, "float"),
        TraceLoggingBool(b, "BOOL"),
        TraceLoggingBoolean(bcpp, "bool (C++)")
        );

    /*
    same as ...
    */

    TraceLoggingWrite(
        g_hMyComponentProvider,
        "NumericValues",
        TraceLoggingUInt8(200, "UINT8"),
        TraceLoggingInt32(-2000000000, "INT32"),
        TraceLoggingUInt32(4000000000, "UINT32"),
        TraceLoggingHexUInt32(4000000000, "UINT32"),
        TraceLoggingInt64(9000000000000000000, "INT64"),
        TraceLoggingFloat32(3.14f, "float"),
        TraceLoggingBool(TRUE, "BOOL"),
        TraceLoggingBoolean(true, "bool (C++)")
        );

    /*
    same as ...
    */

#ifdef __cplusplus

    /*
    TraceLoggingValue() automatically determines the value type (C++ only)
    */

    TraceLoggingWrite(
        g_hMyComponentProvider,
        "NumericValues",
        TraceLoggingValue(u8, "UINT8"),
        TraceLoggingValue(i32, "INT32"),
        TraceLoggingValue(u32, "UINT32"),
        TraceLoggingValue(u32, "UINT32"),
        TraceLoggingValue(i64, "INT64"),
        TraceLoggingValue(f32, "float"),
        TraceLoggingValue(b, "BOOL"),         // This will be evaluated as INT32, not as BOOL
        TraceLoggingValue(bcpp, "bool (C++)") 
        );

    TraceLoggingWrite(
        g_hMyComponentProvider,
        "NumericValues",
        TraceLoggingValue((BYTE)200, "UINT8"),
        TraceLoggingValue(-2000000000, "INT32"),
        TraceLoggingValue(4000000000, "UINT32"),
        TraceLoggingValue(4000000000, "UINT32"),    // This one won't show up as hex. TraceLoggingValue will use default out types
        TraceLoggingValue(9000000000000000000, "INT64"),
        TraceLoggingValue(3.14f, "float"),
        TraceLoggingValue((BOOL)TRUE, "BOOL"),      // This will be evaluated as INT32, not as BOOL
        TraceLoggingValue((bool)true, "bool (C++)") 
        );

#endif


    /*
    Strings and chars
    */

    TraceLoggingWrite(
        g_hMyComponentProvider,
        "Strings and Chars",
        TraceLoggingString("String1", "String (char)"),
        TraceLoggingWideString(L"LString2", "String (wide char)"),
        TraceLoggingChar('A', "Single char")
        );


    /*
    Other types
    */

    /*
    NOTE: In C, a GUID, FILETIME, or SYSTEMTIME value parameter must be an l-value.
    */

    INT_PTR iptr = 1234;
    UINT_PTR uptr = 4321;
    FILETIME ft;
    SYSTEMTIME st;
    SID const sid1 = { SID_REVISION, 1, 5, { 6 } };
    static const GUID s_TestGuid = { 0x3970f9cf, 0x2c0c, 0x4f11, { 0xb1, 0xcc, 0xe3, 0xa1, 0xe9, 0x95, 0x88, 0x33 } };

    GetSystemTime(&st);
    GetSystemTimeAsFileTime(&ft);

    TraceLoggingWrite(
        g_hMyComponentProvider,
        "Other Types",
        TraceLoggingGuid(s_TestGuid, "GUID"),
        TraceLoggingSystemTime(st, "Current Time (FILETIME)"),
        TraceLoggingPointer((LPCVOID)&iptr, "void*"),
        TraceLoggingSid(&sid1, "SID")
        TraceLoggingIntPtr(iptr, "INT_PTR"),
        TraceLoggingUIntPtr(uptr, "UINT_PTR")
        );
}
```



### <a name="name-event-fields"></a><span data-ttu-id="ed7fe-114">Campos de evento de nome</span><span class="sxs-lookup"><span data-stu-id="ed7fe-114">Name event fields</span></span>

<span data-ttu-id="ed7fe-115">O exemplo mostra como nomear os campos de evento.</span><span class="sxs-lookup"><span data-stu-id="ed7fe-115">The example shows how to name event fields.</span></span>


```C++
void TraceLoggingSample::NamingData()
{
    UINT32 Cat = 0xCA7;

    /*
    Each of the following four events are equivalent:
    */

    /*
    TraceLogging uses the symbol to automatically name the field "Cat"
    and assign it the value contained in the variable Cat (0xCA7).
    */

    TraceLoggingWrite(
        g_hMyComponentProvider,
        "Cat1",
        TraceLoggingUInt32(Cat) 
        );

    TraceLoggingWrite(
        g_hMyComponentProvider,
        "Cat2",
        TraceLoggingValue(Cat)  
        );


    /*
    Use a different symbol for the value of the event's "Cat" field.  
    */
    
    UINT32 Tiger = Cat;
    
    /*
    Now we need to explicitly name the datum or we will have events with a 
    different field name ("Tiger").
    */

    TraceLoggingWrite(
        g_hMyComponentProvider,
        "Tiger",
        TraceLoggingUInt32(Tiger, "Cat")
        );

    TraceLoggingWrite(
        g_hMyComponentProvider,
        "Cat3",
        TraceLoggingValue(Tiger, "Cat")
        );
};
```



### <a name="log-event-verbosity-level"></a><span data-ttu-id="ed7fe-116">Nível de detalhes do evento de log</span><span class="sxs-lookup"><span data-stu-id="ed7fe-116">Log event verbosity level</span></span>

<span data-ttu-id="ed7fe-117">Este exemplo mostra como registrar em log eventos por nível de detalhes.</span><span class="sxs-lookup"><span data-stu-id="ed7fe-117">This example shows how to log events by verbosity level.</span></span>


```C++
#include <winmeta.h> // for WINEVENT_LEVEL_* definitions
void TraceLoggingSample::LevelsAndKeywords()
{
    /*
    Verbosity levels and event keywords must be compile-time constants.

    TraceLoggingLevel accepts values 0-255
    TraceLoggingKeyword accepts values 0 to UINT64_MAX

    See winmeta.h for predefined verbosity levels and reserved keyword values.
    */

    PCWSTR MyName = L"Joe";
    INT16 MyRank = 99;
    ULONG MySerialNumber = 12345;

    /*
    The following is only logged when session verbosity level is 
    WINEVENT_LEVEL_VERBOSE (5) or higher ...  
    */

    TraceLoggingWrite(
        g_hMyComponentProvider,
        "Levels",
        TraceLoggingLevel(WINEVENT_LEVEL_VERBOSE),
        TraceLoggingWideString(MyName, "Name"),
        TraceLoggingInt16(MyRank, "Rank"),
        TraceLoggingUInt32(MySerialNumber, "Serial Number")
        );

    /*
    TraceLoggingWrite will not complain if TraceLoggingLevel is invoked more than once.  
    However, only the last level will be used.  
    The following event is only logged at WINEVENT_LEVEL_VERBOSE or higher...
    */

    TraceLoggingWrite(
        g_hMyComponentProvider,
        "Levels",
        TraceLoggingLevel(WINEVENT_LEVEL_CRITICAL),
        TraceLoggingLevel(WINEVENT_LEVEL_VERBOSE),
        TraceLoggingWideString(MyName, "Name"),
        TraceLoggingInt16(MyRank, "Rank"),
        TraceLoggingUInt32(MySerialNumber, "Serial Number")
        );
}
```



### <a name="log-event-keywords"></a><span data-ttu-id="ed7fe-118">Palavras-chave de evento de log</span><span class="sxs-lookup"><span data-stu-id="ed7fe-118">Log event keywords</span></span>

<span data-ttu-id="ed7fe-119">Este exemplo ilustra como definir palavras-chave de evento.</span><span class="sxs-lookup"><span data-stu-id="ed7fe-119">This example illustrates how to set event keywords.</span></span> <span data-ttu-id="ed7fe-120">A filtragem de eventos pode ser feita por nível e palavra-chave.</span><span class="sxs-lookup"><span data-stu-id="ed7fe-120">Event filtering can be done by level and keyword.</span></span> <span data-ttu-id="ed7fe-121">Por exemplo, eventos de conclusão de cenário ou eventos de falha podem ser agrupados em palavras-chave separadas para que você possa filtrar facilmente esses eventos.</span><span class="sxs-lookup"><span data-stu-id="ed7fe-121">For example, scenario completion events or failure events might be grouped under separate keywords so that you can easily filter those events.</span></span>


```C++
void TraceLoggingSample::CombineKeywords()
{
    /*
    Keywords can be combined using multiple TraceLoggingKeyword() macros ...
    */

    #define MY_PROVIDER_KEYWORD_BLUE    0x1
    #define MY_PROVIDER_KEYWORD_YELLOW  0x2
    #define MY_PROVIDER_KEYWORD_GREEN   (MY_PROVIDER_KEYWORD_BLUE | MY_PROVIDER_KEYWORD_YELLOW) 

    PCWSTR Status = L"Feeling a bit green";

    /*
    These events are equivalent...
    */

    TraceLoggingWrite(
        g_hProvider,
        "Keywords",
        TraceLoggingKeyword(MY_PROVIDER_KEYWORD_GREEN),
        TraceLoggingValue(Status, "Current Status")
        );

    TraceLoggingWrite(
        g_hProvider,
        "Keywords",
        TraceLoggingKeyword(MY_PROVIDER_KEYWORD_BLUE | MY_PROVIDER_KEYWORD_YELLOW),
        TraceLoggingValue(Status, "Current Status")
        );

    TraceLoggingWrite(
        g_hProvider,
        "Keywords",
        TraceLoggingKeyword(MY_PROVIDER_KEYWORD_BLUE),
        TraceLoggingKeyword(MY_PROVIDER_KEYWORD_YELLOW),
        TraceLoggingValue(Status, "Current Status")
        );
}
```



### <a name="log-array-event-data"></a><span data-ttu-id="ed7fe-122">Dados de evento de matriz de log</span><span class="sxs-lookup"><span data-stu-id="ed7fe-122">Log array event data</span></span>

<span data-ttu-id="ed7fe-123">Este exemplo mostra como registrar matrizes como dados de evento.</span><span class="sxs-lookup"><span data-stu-id="ed7fe-123">This example shows how to log arrays as event data.</span></span>


```C++
void TraceLoggingSample::Arrays()
{
    INT32 IntValsFixed[5] = {20, 21, 22, 23, 24};
    UINT cIntVals = 5;
    INT32* IntValsVar = new INT32[cIntVals];

    VERIFY_IS_NOT_NULL(IntValsVar);
    memcpy(IntValsVar, IntValsFixed, sizeof(IntValsFixed));


    /*
    Variable size arrays
    */

    TraceLoggingWrite(
        g_hMyComponentProvider,
        "Variable Size Arrays",
        TraceLoggingInt32Array(IntValsVar, (UINT16)cIntVals, "Variable size int array"), 
        TraceLoggingInt32Array(IntValsVar, 5, "Variable size int array")  
        );


    /*
    Fixed size arrays

    Fixed size array macros use the "FixedArray" suffix.
    The absence of the suffix indicates a variable sized array.
    */

    TraceLoggingWrite(
        g_hMyComponentProvider,
        "Constant Size Arrays", 
        TraceLoggingInt32FixedArray(IntValsFixed, _countof(IntValsFixed), "Constant size int array")      
        );

    delete [] IntValsVar;
}
```



### <a name="log-structure-event-data"></a><span data-ttu-id="ed7fe-124">Dados de evento de estrutura de log</span><span class="sxs-lookup"><span data-stu-id="ed7fe-124">Log structure event data</span></span>

<span data-ttu-id="ed7fe-125">Este exemplo mostra como registrar em log dados de eventos de estrutura.</span><span class="sxs-lookup"><span data-stu-id="ed7fe-125">This example shows how to log structure event data.</span></span>


```C++
void TraceLoggingSample::Structs()
{
    WIN32_FIND_DATA FindData;
    HANDLE hFind = FindFirstFile(".", &FindData);

    VERIFY_IS_TRUE(hFind != INVALID_HANDLE_VALUE);

    /*
    TraceLoggingStruct defines a group of related fields in an event.
    The first parameter, which must be a compile-time constant, indicates
    the number of subsequent fields that are to be considered part of the 
    struct.
    */

    TraceLoggingWrite(
        g_hMyComponentProvider,
        "FindFirstFile",
        TraceLoggingStruct(5, "FileData"),                           
            TraceLoggingString(FindData.cFileName, "Name"),   
            TraceLoggingUInt32(FindData.dwFileAttributes, "Attributes"),              
            TraceLoggingFileTime(FindData.ftCreationTime, "CreateTime"),              
            TraceLoggingUInt32(FindData.nFileSizeHigh, "SizeHigh"),              
            TraceLoggingUInt32(FindData.nFileSizeLow, "SizeLow"),
        TraceLoggingPointer(hFind, "Result")
        );

    /*
    ... or ...
    */

#define LogWin32FindData(fd) \
    TraceLoggingStruct(5, "FileData"), \
    TraceLoggingString(((fd).cFileName), "Name"), \
    TraceLoggingUInt32(((fd).dwFileAttributes), "Attributes"), \
    TraceLoggingFileTime(((fd).ftCreationTime), "CreateTime"), \
    TraceLoggingUInt32(((fd).nFileSizeHigh), "SizeHigh"), \
    TraceLoggingUInt32(((fd).nFileSizeLow), "SizeLow")

    TraceLoggingWrite(
        g_hMyComponentProvider,
        "FindFirstFile",
        LogWin32FindData(FindData),
        TraceLoggingPointer(hFind, "Result")
        );

    FindClose(hFind);
}
```



### <a name="how-to-fix-tracelogging-cc-build-errors"></a><span data-ttu-id="ed7fe-126">Como corrigir erros de compilação do TraceLogging C/C++</span><span class="sxs-lookup"><span data-stu-id="ed7fe-126">How to fix TraceLogging C/C++ build errors</span></span>

<span data-ttu-id="ed7fe-127">Erro de compilação</span><span class="sxs-lookup"><span data-stu-id="ed7fe-127">Build Error</span></span>

``` syntax
Linker error:
Error   2       error LNK2001: unresolved external symbol __imp__EventSetInformation@20 App.xaml.obj    PrintPreview
Error   3       error LNK2001: unresolved external symbol __imp__EventRegister@16       App.xaml.obj    PrintPreview
```

<span data-ttu-id="ed7fe-128">Fix</span><span class="sxs-lookup"><span data-stu-id="ed7fe-128">Fix</span></span>

<span data-ttu-id="ed7fe-129">Corrija esse erro vinculando advapi32. lib em seu projeto.</span><span class="sxs-lookup"><span data-stu-id="ed7fe-129">Fix this error by linking advapi32.lib in your project.</span></span>

 

 




