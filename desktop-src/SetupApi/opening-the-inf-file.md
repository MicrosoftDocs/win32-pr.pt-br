---
description: Você deve usar a função SetupOpenInfFile para abrir o arquivo INF antes de poder recuperar informações dele ou acrescentar outros arquivos INF a ele.
ms.assetid: ba4d511a-ad19-4619-a10a-cafef789821b
title: Abrindo o arquivo INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d8493fda983f2942705b97ea243f6cb95e91c15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828689"
---
# <a name="opening-the-inf-file"></a>Abrindo o arquivo INF

Você deve usar a função [**SetupOpenInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) para abrir o arquivo inf antes de poder recuperar informações dele ou acrescentar outros arquivos INF a ele.

O seguinte abre um arquivo INF usando [**SetupOpenInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) e retorna um identificador, MyInf, para o arquivo inf aberto. O parâmetro *InfClass* de **SetupOpenInfFile** é especificado como **NULL** para indicar que a classe do arquivo inf deve ser ignorada.


```C++
HINF MyInf;                //variable to hold the INF handle
UINT ErrorLine;            //variable to hold errors returned
BOOL test=0;                 //variable to receive function success
 
MyInf = SetupOpenInfFile (
      szInfFileName,       //the filename of the inf file to open
      NULL,                //optional class information
      INF_STYLE_WIN4,      //the inf style
      &ErrorLine           //line number of the syntax error
);
```



Depois que um arquivo INF é aberto, você pode chamar a função [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) para acrescentar um arquivo ao arquivo inf aberto. Para acrescentar vários arquivos, repita esse processo. Se você chamar a função **SetupOpenAppendInfFile** e o nome de arquivo passado para ela for **NULL**, a função pesquisará a seção versão do arquivo inf aberto (e todos os arquivos INF anexados) de uma chave de layoutfile. Se a função encontrar uma chave, ela acrescentará o arquivo especificado por essa chave (geralmente o LAYOUT. INF). Quando vários arquivos INF tiverem sido combinados, o **SetupOpenAppendInfFile** começará com o último arquivo inf acrescentado quando procurar uma seção de versão.

 

 



