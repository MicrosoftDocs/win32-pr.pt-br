---
description: Depois que o arquivo INF for aberto, você poderá coletar informações dele para criar a interface do usuário ou para direcionar o processo de instalação. As funções de instalação fornecem vários níveis de funcionalidade para a coleta de informações de um arquivo INF.
ms.assetid: 3ef2768b-8c73-4258-937c-77a40963ffe4
title: Extraindo informações de arquivo do arquivo INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be4b404f44ca7d1d92fe0ce8eab08b73012ff144
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827329"
---
# <a name="extracting-file-information-from-the-inf-file"></a>Extraindo informações de arquivo do arquivo INF

Depois que o arquivo INF for aberto, você poderá coletar informações dele para criar a interface do usuário ou para direcionar o processo de instalação. As funções de instalação fornecem vários níveis de funcionalidade para a coleta de informações de um arquivo INF.



| Para coletar informações...                | Usar estas funções...                                                        |
|---------------------------------------|-----------------------------------------------------------------------------|
| Sobre o arquivo INF                    | [**SetupGetInfInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinfinformationa)                    |
|                                       | [**SetupQueryInfFileInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinffileinformationa)        |
|                                       | [**SetupQueryInfVersionInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinfversioninformationa). |
| Sobre arquivos de origem e de destino         | [**SetupGetSourceFileLocation**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourcefilelocationa)            |
|                                       | [**SetupGetSourceFileSize**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourcefilesizea)                    |
|                                       | [**SetupGetTargetPath**](/windows/desktop/api/Setupapi/nf-setupapi-setupgettargetpatha)                            |
|                                       | [**SetupGetSourceInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa)                            |
| De uma linha de um arquivo INF            | [**SetupGetLineText**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinetexta)                                |
|                                       | [**SetupFindNextLine**](/windows/desktop/api/Setupapi/nf-setupapi-setupfindnextline)                              |
|                                       | [**SetupFindNextMatchLine**](/windows/desktop/api/Setupapi/nf-setupapi-setupfindnextmatchlinea)                    |
|                                       | [**SetupGetLineByIndex**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinebyindexa)                          |
|                                       | [**SetupFindFirstLine**](/windows/desktop/api/Setupapi/nf-setupapi-setupfindfirstlinea)                            |
| De um campo de uma linha em um arquivo INF | [**SetupGetStringField**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetstringfielda)                          |
|                                       | [**SetupGetIntField**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetintfield)                                |
|                                       | [**SetupGetBinaryField**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetbinaryfield)                          |
|                                       | [**SetupGetMultiSzField**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetmultiszfielda)                        |



 

O exemplo a seguir usa a função [**SetupGetSourceInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa) para recuperar a Descrição legível por humanos de uma mídia de origem de um arquivo inf.


```C++
#include <windows.h>
#include <setupapi.h>

BOOL test;  
HINF MyInf;
UINT SourceId;
PTSTR Buffer;
DWORD MaxBufSize;
DWORD BufSize;

int main()  
{ 

test = SetupGetSourceInfo (
     MyInf,   //Handle to the INF file to access                
     SourceId, //Id of the source media                 
     SRCINFO_DESCRIPTION, //which information to retrieve     
     Buffer, //a pointer to the buffer to receive the information                     
     MaxBufSize,  //the size allocated for the buffer 
     &BufSize    //buffer size actually needed
);
  
return 0;
}
```



No exemplo, MyInf é o identificador para o arquivo INF aberto. SourceID é o identificador de uma mídia de origem específica. O valor SRCINFO \_ Descrição especifica que a função [**SetupGetSourceInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa) deve recuperar a descrição da mídia de origem. O buffer aponta para uma cadeia de caracteres que receberá a descrição, MaxBufSize indica os recursos alocados para o buffer e BufSize indica os recursos necessários para armazenar o buffer.

Se BufSize for maior que MaxBufSize, a função retornará **false** e uma chamada subsequente para [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará um \_ buffer insuficiente de erro \_ .

 

 
