---
title: Nomes em IStorage
description: Um conjunto de propriedades é identificado com um identificador de formato (FMTID) na interface IPropertySetStorage.
ms.assetid: 5f8eba37-c589-413e-9971-7ecb01dc6734
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cef9417f2f5fad7fd17dcc3d431f1d3565a3843
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498818"
---
# <a name="names-in-istorage"></a><span data-ttu-id="0a6b6-103">Nomes em IStorage</span><span class="sxs-lookup"><span data-stu-id="0a6b6-103">Names in IStorage</span></span>

<span data-ttu-id="0a6b6-104">Um conjunto de propriedades é identificado com um identificador de formato (FMTID) na interface [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) .</span><span class="sxs-lookup"><span data-stu-id="0a6b6-104">A property set is identified with a format identifier (FMTID) in the [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) interface.</span></span> <span data-ttu-id="0a6b6-105">Na interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) , um conjunto de propriedades é nomeado com uma cadeia de caracteres Unicode terminada em nulo com um comprimento máximo de 32 caracteres.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-105">In the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface, a property set is named with a null-terminated Unicode string with a maximum length of 32 characters.</span></span> <span data-ttu-id="0a6b6-106">Para habilitar a interoperabilidade, é necessário estabelecer um mapeamento entre um FMTID e uma cadeia de caracteres Unicode terminada em nulo correspondente.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-106">To enable interoperability, a mapping between an FMTID and a corresponding null-terminated Unicode string must be established.</span></span>

## <a name="converting-a-property-set-from-a-fmtid-to-a-string-name"></a><span data-ttu-id="0a6b6-107">Convertendo um conjunto de propriedades de um FMTID para um nome de cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="0a6b6-107">Converting a property set from a FMTID to a string name</span></span>

<span data-ttu-id="0a6b6-108">Ao converter de um FMTID para um nome de cadeia de caracteres Unicode correspondente, primeiro verifique se FMTID é um valor bem conhecido, listado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-108">When converting from an FMTID to a corresponding Unicode string name, first verify that the FMTID is a well-known value, listed in the following table.</span></span> <span data-ttu-id="0a6b6-109">Nesse caso, use o nome de cadeia de caracteres bem conhecido correspondente.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-109">If so, then use the corresponding well-known string name.</span></span>

| <span data-ttu-id="0a6b6-110">FMTID</span><span class="sxs-lookup"><span data-stu-id="0a6b6-110">FMTID</span></span>                                                                                | <span data-ttu-id="0a6b6-111">Nome da cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="0a6b6-111">String name</span></span>                       | <span data-ttu-id="0a6b6-112">Semântico</span><span class="sxs-lookup"><span data-stu-id="0a6b6-112">Semantic</span></span>                                                         |
|--------------------------------------------------------------------------------------|-----------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="0a6b6-113">F29F85E0-4FF9-1068-AB91-08002B27B3D9</span><span class="sxs-lookup"><span data-stu-id="0a6b6-113">F29F85E0-4FF9-1068-AB91-08002B27B3D9</span></span>                                                 | <span data-ttu-id="0a6b6-114">" \\ 005SummaryInformation"</span><span class="sxs-lookup"><span data-stu-id="0a6b6-114">"\\005SummaryInformation"</span></span>         | <span data-ttu-id="0a6b6-115">Informações de resumo da COM2</span><span class="sxs-lookup"><span data-stu-id="0a6b6-115">COM2 summary information</span></span>                                         |
| <span data-ttu-id="0a6b6-116">D5CDD502-2E9C-101B-9397-08002B2CF9AE D5CDD505-2E9C-101B-9397-08002B2CF9AE</span><span class="sxs-lookup"><span data-stu-id="0a6b6-116">D5CDD502-2E9C-101B-9397-08002B2CF9AE D5CDD505-2E9C-101B-9397-08002B2CF9AE</span></span><br/> | <span data-ttu-id="0a6b6-117">" \\ 005DocumentSummaryInformation"</span><span class="sxs-lookup"><span data-stu-id="0a6b6-117">"\\005DocumentSummaryInformation"</span></span> | <span data-ttu-id="0a6b6-118">Informações de resumo do documento do Office e propriedades definidas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-118">Office document summary information and user-defined properties.</span></span> |



 

> [!Note]  
> <span data-ttu-id="0a6b6-119">O conjunto de propriedades **DocumentSummaryInformation** e **UserDefined** é exclusivo, pois ele contém duas seções.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-119">The **DocumentSummaryInformation** and **UserDefined** property set is unique in that it contains two sections.</span></span> <span data-ttu-id="0a6b6-120">Várias seções não são permitidas em nenhum outro conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-120">Multiple sections are not permitted in any other property set.</span></span> <span data-ttu-id="0a6b6-121">Para obter mais informações, consulte [formato de conjunto de propriedades serializadas de armazenamento estruturado](structured-storage-serialized-property-set-format.md)e [os conjuntos de propriedades DocumentSummaryInformation e UserDefined](the-documentsummaryinformation-and-userdefined-property-sets.md).</span><span class="sxs-lookup"><span data-stu-id="0a6b6-121">For more information, see [Structured Storage Serialized Property Set Format](structured-storage-serialized-property-set-format.md), and [The DocumentSummaryInformation and UserDefined Property Sets](the-documentsummaryinformation-and-userdefined-property-sets.md).</span></span> <span data-ttu-id="0a6b6-122">A primeira seção foi definida como parte de COM; o segundo foi definido por Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-122">The first section was defined as part of COM; the second was defined by Microsoft Office.</span></span>

 

<span data-ttu-id="0a6b6-123">Se o FMTID não for um valor conhecido, use o procedimento a seguir para forma algorítmica formar um nome de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-123">If the FMTID is not a well-known value, then use the following procedure to algorithmically form a string name.</span></span>

<span data-ttu-id="0a6b6-124">**Para forma algorítmica formate um nome de cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0a6b6-124">**To algorithmically form a string name**</span></span>

1.  <span data-ttu-id="0a6b6-125">Converta o FMTID em uma ordem de byte little-endian, se necessário.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-125">Convert the FMTID to little-endian byte order, if necessary.</span></span>
2.  <span data-ttu-id="0a6b6-126">Pegue os 128 bits do FMTID e considere-os como uma cadeia de caracteres de bit longo concatenando cada um dos bytes juntos.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-126">Take the 128 bits of the FMTID and consider them as one long bit string by concatenating each of the bytes together.</span></span> <span data-ttu-id="0a6b6-127">O primeiro bit do valor de 128 bits é o bit menos significativo do primeiro byte na memória do FMTID; o último bit do valor de 128 bits é o bit mais significativo do último byte na memória do FMTID.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-127">The first bit of the 128 bit value is the least significant bit of the first byte in memory of the FMTID; the last bit of the 128 bit value is the most significant bit of the last byte in memory of the FMTID.</span></span> <span data-ttu-id="0a6b6-128">Estenda esses 128 bits para 130 bits, adicionando dois bits zero ao final.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-128">Extend these 128 bits to 130 bits by adding two zero bits to the end.</span></span>
3.  <span data-ttu-id="0a6b6-129">Divida os 130 bits em grupos de cinco bits; Haverá 26 grupos desse tipo.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-129">Divide the 130 bits into groups of five bits; there will be 26 such groups.</span></span> <span data-ttu-id="0a6b6-130">Considere cada grupo como um inteiro com precedência de bits invertido.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-130">Consider each group as an integer with reversed bit precedence.</span></span> <span data-ttu-id="0a6b6-131">Por exemplo, o primeiro dos 128 bits é o bit menos significativo do primeiro grupo de cinco bits; o quinto dos 128 bits é o bit mais significativo do primeiro grupo.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-131">For example, the first of the 128 bits is the least significant bit of the first group of five bits; the fifth of the 128 bits is the most significant bit of the first group.</span></span>
4.  <span data-ttu-id="0a6b6-132">Mapeie cada um desses inteiros como um índice na matriz de 32 caracteres: ABCDEFGHIJKLMNOPQRSTUVWXYZ012345.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-132">Map each of these integers as an index into the array of thirty-two characters: ABCDEFGHIJKLMNOPQRSTUVWXYZ012345.</span></span> <span data-ttu-id="0a6b6-133">Isso produz uma sequência de 26 caracteres Unicode que usa apenas caracteres maiúsculos e numerais.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-133">This yields a sequence of 26 Unicode characters that uses only uppercase characters and numerals.</span></span> <span data-ttu-id="0a6b6-134">As considerações diferenciar maiúsculas e minúsculas não se aplicam, fazendo com que cada caractere seja exclusivo em qualquer localidade.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-134">Case sensitive and case insensitive considerations do not apply, causing each character to be unique in any locale.</span></span>
5.  <span data-ttu-id="0a6b6-135">Crie a cadeia de caracteres final concatenando a cadeia de caracteres " \\ 005" na frente desses 26 caracteres, com um comprimento total de 27 caracteres.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-135">Create the final string by concatenating the string "\\005" onto the front of these 26 characters, for a total length of 27 characters.</span></span>

<span data-ttu-id="0a6b6-136">O código de exemplo a seguir mostra como mapear de um FMTID para uma cadeia de caracteres de propriedade.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-136">The following example code shows how to map from an FMTID to a property string.</span></span>


```C++
#define CBIT_BYTE        8
#define CBIT_CHARMASK    5
#define CCH_MAP          (1 << CBIT_CHARMASK)    // 32
#define CHARMASK         (CCH_MAP - 1)           // 0x1f
 
CHAR awcMap[CCH_MAP + 1] = "abcdefghijklmnopqrstuvwxyz012345";
 
WCHAR MapChar(ULONG I) {
    return((WCHAR) awcMap[i & CHARMASK]);
    }
 
VOID GuidToPropertyStringName(GUID *pguid, WCHAR awcname[]) {
    BYTE *pb = (BYTE *) pguid;
    BYTE *pbEnd = pb + sizeof(*pguid);
    ULONG cbitRemain = CBIT_BYTE;
    WCHAR *pwc = awcname;
 
    *pwc++ = ((WCHAR) 0x0005);
    while (pb < pbEnd) {
        ULONG i = *pb >> (CBIT_BYTE - cbitRemain);
        if (cbitRemain >= CBIT_CHARMASK) {
            *pwc = MapChar(i);
            if (cbitRemain == CBIT_BYTE && 
                                    *pwc >= L'a' && *pwc <= L'z')
                {
                *pwc += (WCHAR) (L'A' - L'a');
                }
            pwc++;
            cbitRemain -= CBIT_CHARMASK;
            if (cbitRemain == 0) {
                pb++;
                cbitRemain = CBIT_BYTE;
                }
            }
        else {
            if (++pb < pbEnd) {
                i |= *pb << cbitRemain;
                }
            *pwc++ = MapChar(i);
            cbitRemain += CBIT_BYTE - CBIT_CHARMASK;
            }
        }
    *pwc = L'\0';
    }
```



## <a name="converting-a-property-set-from-a-string-name-to-a-fmtid"></a><span data-ttu-id="0a6b6-137">Convertendo um conjunto de propriedades de um nome de cadeia de caracteres para um FMTID</span><span class="sxs-lookup"><span data-stu-id="0a6b6-137">Converting a property set from a string name to a FMTID</span></span>

<span data-ttu-id="0a6b6-138">Os conversores de nomes de cadeias de caracteres de propriedade em GUIDs devem aceitar letras minúsculas como sinônimos com suas contrapartes em maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-138">Converters of property string names to GUIDs should accept lowercase letters as synonymous with their uppercase counterparts.</span></span>

<span data-ttu-id="0a6b6-139">O código de exemplo a seguir mostra como mapear de uma cadeia de caracteres de propriedade para um FMTID.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-139">The following example code shows how to map from a property string to an FMTID.</span></span>


```C++
#include "stdafx.h"
#define _INC_OLE
#include <windows.h>
#include <stdlib.h>
#include <stdio.h>
#include <string.h>
#include <ctype.h>
#define CBIT_CHARMASK 5
#define CBIT_BYTE     8
#define CBIT_GUID    (CBIT_BYTE * sizeof(GUID))
#define CWC_PROPSET  (1 + (CBIT_GUID + CBIT_CHARMASK-1)/CBIT_CHARMASK)
#define WC_PROPSET0  ((WCHAR) 0x0005)
#define CCH_MAP      (1 << CBIT_CHARMASK)        // 32
#define CHARMASK     (CCH_MAP - 1)            // 0x1f
CHAR awcMap[CCH_MAP + 1] = "abcdefghijklmnopqrstuvwxyz012345";
#define CALPHACHARS  ('z' - 'a' + 1)

GUID guidSummary =
{ 0xf29f85e0,0x4ff9, 0x1068,
{ 0xab, 0x91, 0x08, 0x00, 0x2b, 0x27, 0xb3, 0xd9 } };

WCHAR wszSummary[] = L"SummaryInformation";

GUID guidDocumentSummary =
    { 0xd5cdd502,
      0x2e9c, 0x101b,
      { 0x93, 0x97, 0x08, 0x00, 0x2b, 0x2c, 0xf9, 0xae } };

WCHAR wszDocumentSummary[] = L"DocumentSummaryInformation";
__inline WCHAR

MapChar(IN ULONG i)
{
    return((WCHAR) awcMap[i & CHARMASK]);
}

ULONG PropertySetNameToGuid(
    IN ULONG cwcname,
    IN WCHAR const awcname[],
    OUT GUID *pguid)
{
    ULONG Status = ERROR_INVALID_PARAMETER;
    WCHAR const *pwc = awcname;

    if (pwc[0] == WC_PROPSET0)
    {
        //Note: cwcname includes the WC_PROPSET0, and
        //sizeof(wsz...) includes the trailing L'\0', but
        //the comparison excludes both the leading
        //WC_PROPSET0 and the trailing L'\0'.
        if (cwcname == sizeof(wszSummary)/sizeof(WCHAR) &&
            wcsnicmp(&pwc[1], wszSummary, cwcname - 1) == 0)
        {
            *pguid = guidSummary;
            return(NO_ERROR);
        }
        if (cwcname == CWC_PROPSET)
        {
            ULONG cbit;
            BYTE *pb = (BYTE *) pguid - 1;
            ZeroMemory(pguid, sizeof(*pguid));
            for (cbit = 0; cbit < CBIT_GUID; cbit += 
            CBIT_CHARMASK)
            {
                ULONG cbitUsed = cbit % CBIT_BYTE;
                ULONG cbitStored;
                WCHAR wc;
                if (cbitUsed == 0)
                {
                    pb++;
                }
                wc = *++pwc - L'A';        //assume uppercase
                if (wc > CALPHACHARS)
                {
                    wc += (WCHAR) (L'A' - L'a'); //try lowercase
                    if (wc > CALPHACHARS)
                    {
                        wc += L'a' - L'0' + CALPHACHARS; 
                        if (wc > CHARMASK)
                        {
                            goto fail;       //invalid character
                        }
                    }
                }
                *pb |= (BYTE) (wc << cbitUsed);
                cbitStored = min(CBIT_BYTE - cbitUsed, 
                CBIT_CHARMASK);

                //If the translated bits will not fit in the 
                //current byte
                if (cbitStored < CBIT_CHARMASK)
                {
                    wc >>= CBIT_BYTE - cbitUsed;
                    if (cbit + cbitStored == CBIT_GUID)
                    {
                       if (wc != 0)
                       {
                           goto fail;        //extra bits
                       }
                       break;
                    }
                    pb++;
                    *pb |= (BYTE) wc;
                }
           }
           Status = NO_ERROR;
      }
    }
fail:
    return(Status);
}
```



<span data-ttu-id="0a6b6-140">Ao tentar abrir um conjunto de propriedades existente, em [IPropertySetStorage:: Open](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open), a (raiz) FMTID é convertida em uma cadeia de caracteres, conforme descrito acima.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-140">When attempting to open an existing property set, in [IPropertySetStorage::Open](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open), the (root) FMTID is converted to a string as described above.</span></span> <span data-ttu-id="0a6b6-141">Se existir um elemento da [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) desse nome, ele será usado.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-141">If an element of the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) of that name exists, it is used.</span></span> <span data-ttu-id="0a6b6-142">Caso contrário, a abertura falhará.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-142">Otherwise, the open fails.</span></span>

<span data-ttu-id="0a6b6-143">Ao criar um novo conjunto de propriedades, o mapeamento acima determina o nome da cadeia de caracteres usada.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-143">When creating a new property set, the above mapping determines the string name used.</span></span>

 

 





