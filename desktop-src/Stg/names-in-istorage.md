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
# <a name="names-in-istorage"></a>Nomes em IStorage

Um conjunto de propriedades é identificado com um identificador de formato (FMTID) na interface [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) . Na interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) , um conjunto de propriedades é nomeado com uma cadeia de caracteres Unicode terminada em nulo com um comprimento máximo de 32 caracteres. Para habilitar a interoperabilidade, é necessário estabelecer um mapeamento entre um FMTID e uma cadeia de caracteres Unicode terminada em nulo correspondente.

## <a name="converting-a-property-set-from-a-fmtid-to-a-string-name"></a>Convertendo um conjunto de propriedades de um FMTID para um nome de cadeia de caracteres

Ao converter de um FMTID para um nome de cadeia de caracteres Unicode correspondente, primeiro verifique se FMTID é um valor bem conhecido, listado na tabela a seguir. Nesse caso, use o nome de cadeia de caracteres bem conhecido correspondente.

| FMTID                                                                                | Nome da cadeia de caracteres                       | Semântico                                                         |
|--------------------------------------------------------------------------------------|-----------------------------------|------------------------------------------------------------------|
| F29F85E0-4FF9-1068-AB91-08002B27B3D9                                                 | " \\ 005SummaryInformation"         | Informações de resumo da COM2                                         |
| D5CDD502-2E9C-101B-9397-08002B2CF9AE D5CDD505-2E9C-101B-9397-08002B2CF9AE<br/> | " \\ 005DocumentSummaryInformation" | Informações de resumo do documento do Office e propriedades definidas pelo usuário. |



 

> [!Note]  
> O conjunto de propriedades **DocumentSummaryInformation** e **UserDefined** é exclusivo, pois ele contém duas seções. Várias seções não são permitidas em nenhum outro conjunto de propriedades. Para obter mais informações, consulte [formato de conjunto de propriedades serializadas de armazenamento estruturado](structured-storage-serialized-property-set-format.md)e [os conjuntos de propriedades DocumentSummaryInformation e UserDefined](the-documentsummaryinformation-and-userdefined-property-sets.md). A primeira seção foi definida como parte de COM; o segundo foi definido por Microsoft Office.

 

Se o FMTID não for um valor conhecido, use o procedimento a seguir para forma algorítmica formar um nome de cadeia de caracteres.

**Para forma algorítmica formate um nome de cadeia de caracteres**

1.  Converta o FMTID em uma ordem de byte little-endian, se necessário.
2.  Pegue os 128 bits do FMTID e considere-os como uma cadeia de caracteres de bit longo concatenando cada um dos bytes juntos. O primeiro bit do valor de 128 bits é o bit menos significativo do primeiro byte na memória do FMTID; o último bit do valor de 128 bits é o bit mais significativo do último byte na memória do FMTID. Estenda esses 128 bits para 130 bits, adicionando dois bits zero ao final.
3.  Divida os 130 bits em grupos de cinco bits; Haverá 26 grupos desse tipo. Considere cada grupo como um inteiro com precedência de bits invertido. Por exemplo, o primeiro dos 128 bits é o bit menos significativo do primeiro grupo de cinco bits; o quinto dos 128 bits é o bit mais significativo do primeiro grupo.
4.  Mapeie cada um desses inteiros como um índice na matriz de 32 caracteres: ABCDEFGHIJKLMNOPQRSTUVWXYZ012345. Isso produz uma sequência de 26 caracteres Unicode que usa apenas caracteres maiúsculos e numerais. As considerações diferenciar maiúsculas e minúsculas não se aplicam, fazendo com que cada caractere seja exclusivo em qualquer localidade.
5.  Crie a cadeia de caracteres final concatenando a cadeia de caracteres " \\ 005" na frente desses 26 caracteres, com um comprimento total de 27 caracteres.

O código de exemplo a seguir mostra como mapear de um FMTID para uma cadeia de caracteres de propriedade.


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



## <a name="converting-a-property-set-from-a-string-name-to-a-fmtid"></a>Convertendo um conjunto de propriedades de um nome de cadeia de caracteres para um FMTID

Os conversores de nomes de cadeias de caracteres de propriedade em GUIDs devem aceitar letras minúsculas como sinônimos com suas contrapartes em maiúsculas.

O código de exemplo a seguir mostra como mapear de uma cadeia de caracteres de propriedade para um FMTID.


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



Ao tentar abrir um conjunto de propriedades existente, em [IPropertySetStorage:: Open](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open), a (raiz) FMTID é convertida em uma cadeia de caracteres, conforme descrito acima. Se existir um elemento da [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) desse nome, ele será usado. Caso contrário, a abertura falhará.

Ao criar um novo conjunto de propriedades, o mapeamento acima determina o nome da cadeia de caracteres usada.

 

 





